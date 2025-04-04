<%*
const FileName = await tp.system.prompt("Organization name?")
const Summary = await tp.system.prompt("Quick Summary", "", false, true)
const Base = await tp.system.prompt("Base of Operations?")
const Leader = await tp.system.prompt("Leader")
const Alignment = await tp.system.prompt("Organization Alignment?")
%>---
title: <% FileName %>
tags:
  - "dnd"
  - organization
  - <% FileName %>
type: "organization"
appearances:
---
# Summary
<% Summary %>

>[!infobox]
>**Base**: <% Base %><br>
>**Leader**: <% Leader %><br>
>**Alignment**: <% Alignment %><br>
>**Organizational Structure**: <br>
>**Appearances**: 


# Relationships
## Known Members
###
## Locations
###
## NPC's
###
## PC's
###
## Structures
###

<% await tp.file.move("/content/Organizations/" + tp.file.title) %>
