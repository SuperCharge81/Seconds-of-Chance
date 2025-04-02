<%*
const FileName = await tp.system.prompt("Location Name?")
await tp.file.rename(FileName)
const Appearance = await tp.system.prompt("Appearance?")
const Summary = await tp.system.prompt("Quick Summary", "", false, true)
%>---
title: <% FileName %>
type: "location"
tags:
  - "dnd"
  - "location"
  - <% FileName %>
appearances:
---
<% await tp.file.move("/content/Locations/" + tp.file.title) %>
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