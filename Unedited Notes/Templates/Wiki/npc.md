<%*
const FileName = await tp.system.prompt("NPC name")
await tp.file.rename(FileName)
const Location = await tp.system.prompt("Current Location?")
const Race = await tp.system.prompt("Race?")
const Gender = await tp.system.prompt("Gender?")
const Height = await tp.system.prompt("Hight?")
const Appearance = await tp.system.prompt("Appearance?")
const Summary = await tp.system.prompt("Quick Summary", "", false, true)
const Organization = await tp.system.prompt("Organization")
%>---
title: <% FileName %>
type: "npc"
tags:
  - "dnd"
  - "npc"
  - <% FileName %>
---
<% await tp.file.move("/content/NPC's/" + tp.file.title) %>
>[!infobox]
>**Organization**: <% Organization %><br>
>**Location**: <% Location %><br>
>**Appearances**: <br>
>**Mentioned in**: <br>
>**Height**: <% Height %><br>
>**Gender**: <% Gender %><br>
>**Race**: <% Race %>
# Summary
<% Summary %>

# Description
<% Appearance %>



# Relationships
## Locations:
### 
## NPC's:
###
## PC's:
###