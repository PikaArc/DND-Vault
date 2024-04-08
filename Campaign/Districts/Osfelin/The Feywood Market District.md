---
tags:
  - "#Location"
  - "#District"
art: z_Assets/Misc/PlaceholderImage.png
publish: true
districttype:
  - Financial
location:
  - "[[Osfelin]]"
pronounced: Fay-wood Market District
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> **Publish** | `INPUT[toggle:publish]` |
>
>> [!metadata|metadataoption]- Art
>> #### Art
>>  |
>> ---|---|
> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Info
>> #### Info
>>  |
>> ---|---|
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Type** | `INPUT[DistrictType][inlineListSuggester:districttype]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{districttype}][text]` |
> **Location** | `VIEW[{location}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[PlaceholderImage.png]]
> height: 600px
> width: 640px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 1
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "POI")
> SORT tags DESC, poitype ASC, file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Organization")
> SORT tags DESC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 

The Feywood Market District is the bustling heart of commerce in Osfelin. It spans a vast area within the city, with colorful stalls and enchanting shops lining its winding streets. Here, merchants from across the Feywild gather to sell their wares, offering everything from rare arcane ingredients to exquisite magical artifacts.

## Current Events

Recently, tensions have arisen in the Feywood Market District following a series of mysterious thefts. Valuable magical artifacts and rare ingredients have gone missing from several of the market stalls, leaving merchants on edge and visitors wary. Rumors abound, with some suspecting rival merchants of foul play, while others fear darker forces may be at work.

## History

The Feywood Market District has been a hub of trade and commerce in Osfelin for centuries. Its origins date back to the city's founding, when enterprising merchants flocked to the bustling marketplace to ply their trade. Over the years, the district has grown and expanded, becoming a vibrant center of economic activity where goods from across the Feywild are bought and sold.

## Notes

