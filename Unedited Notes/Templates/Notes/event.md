<%*
const SessionNum = await tp.system.prompt("Session number?")
const fileName = await tp.system.prompt("Event Name?")
const day = await tp.system.prompt("day?")
await tp.file.rename(fileName)
const session = "Session " + SessionNum 
%>---
title: <% fileName %>
type: "event"
tags:
 - "dnd"
 - "event"
 - <% fileName %>
session: <% session %>
---
day: <% "[" + day + "](" + "Session%20" + SessionNum + "/Days/" + day + ")" %>
<% await tp.file.move("/" + session + "/Events/" + day + "/" + fileName ) 
%>

Event Name: <% fileName %>

>[!Summary]
><% await tp.system.prompt("Summary?", "", false, true) %>
