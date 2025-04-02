<%*
const SessionNum = await tp.system.prompt("Session number?")
const fileName = await tp.system.prompt("day?")
await tp.file.rename(fileName)
const session = "Session " + SessionNum 
%>---
title: <% fileName %>
type: "day"
tags:
 - "dnd"
 - "day"
 - <% fileName %>
session: <% session %>
---

<% await tp.file.move("/" + session + "/Days/" + tp.file.title) 
%>

>[!Day of the Week]
> <% fileName %>

>[!Summary]
><% await tp.system.prompt("Summary?", "", false, true) %>

>[!Linked Events]


