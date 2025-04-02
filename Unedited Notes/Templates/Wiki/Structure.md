<%*
const FileName = await tp.system.prompt("Structure Name?")
await tp.file.rename(FileName)
const Appearance = await tp.system.prompt("Appearance?")
const Summary = await tp.system.prompt("Quick Summary", "", false, true)
const StructureType = await tp.system.prompt("type of structure?")
const Location = await tp.system.prompt("Location")
%>---
title: <% FileName %>
type: "Structure"
tags:
  - "dnd"
  - "structure"
  - <% StructureType %>
  - <% FileName %>
---
<% await tp.file.move("/content/Structures/" + tp.file.title) %>
>[!infobox]
>Location: <% Location %>
>Appearances:
>Structure type: <% StructureType %>
# Description
<% Appearance %>

# Summary
<% Summary %>

# Relationships
## Locations:
### 
## NPC's:
###
## PC's:
###