<%*
const FileName = await tp.system.prompt("Object name")
const Summary = await tp.system.prompt("Quick Summary", "", false, true)
const Appearance = await tp.system.prompt("Appearance?","", false, true)
const ObjectType = await tp.system.prompt("Object Type?")
const Size = await tp.system.prompt("Object Size")
%>---
title: <% FileName %>
tags:
  - "dnd"
  - object
  - <% ObjectType %>
type: "object"
---
>[!infobox]
>**Object Type**: <% ObjectType %><br>
>**Size**: <% Size %>
# Summary
<% Summary %>

# Description
<% Appearance %>

<% await tp.file.move("/content/Objects/" + tp.file.title) %>