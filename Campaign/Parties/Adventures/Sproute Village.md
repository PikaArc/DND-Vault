---
tags:
  - "#Adventure"
art: z_Assets/Misc/PlaceholderImage.png
whichparty: "[[The Ionic Talk]]"
status: ⏳
quicknote: The Party's adventure around the Sproute Village
publish: true
---
> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> **Publish** | `INPUT[toggle:publish]` |
>
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
>> **Aliases** | `INPUT[list:aliases]` |
>> **Quick Notes** |  `INPUT[textArea:quicknote]`
>> **Which Party** | `INPUT[Null][suggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Status** | `INPUT[Status][:status]` |

> [!infobox]
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> #### Adventure Info
>  |
> ---|---|
> **Party** | `VIEW[{whichparty}][link]` |
> **Status** | `VIEW[{status}]` |

# **`=this.file.name`**

> [!metadata|quests]- Quests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes, status AS Status
> FROM "Campaign"
> WHERE econtains(tags, "Quest") AND econtains(adventure, this.file.link)
> SORT file.name ASC

## Overview

Give me a overview of the village
key points are: Small berry field, 7 houses which include an inn and a bar, a bit further away from forests and a kingdom

# Sproute Village

## Overview
Sproute Village is a quaint and cozy settlement, nestled in a small clearing surrounded by open fields and plains. The village is relatively small, consisting of seven houses, an inn, and a bar. The fields nearby are primarily used for growing berries, adding a charming touch to the village's rustic charm.

Although the forest is not far from the village, it is situated at a comfortable distance, providing a measure of security for its inhabitants. A larger kingdom lies further away, but the villagers maintain a friendly relationship with their neighbors.

## Notes