<%*
const FileName = await tp.system.prompt("Object name")
const Summary = await tp.system.prompt("Quick Summary", "", false, true)
const Appearance = await tp.system.prompt("Appearance?")
const ObjectType = await tp.system.prompt("Object Type?")
%>---
title: <% FileName %>
tags:
  - "dnd"
  - object
  - <% FileName %>
type: "object"
---
>[!infobox]
>Object Type: <% ObjectType %><br>
>Size: 
# Summary
<% Summary %>

# Description
<% Appearance %>

<% await tp.file.move("/content/Objects/" + tp.file.title) %>