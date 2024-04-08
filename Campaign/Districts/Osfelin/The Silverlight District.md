---
tags:
  - "#Location"
  - "#District"
art: z_Assets/Misc/PlaceholderImage.png
publish: true
location:
  - "[[Osfelin]]"
districttype:
  - Residential
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

The Silverlight District is a prestigious neighborhood within Osfelin, home to the city's elite. Grand mansions and opulent estates line its streets, their gleaming facades a testament to the wealth and influence of the district's residents. The Silverlight District is where the nobility of Osfelin reside, including members of the royal court and influential fey families.

## Current Events

Tensions run high in the Silverlight District following the disappearance of Princess Fanlyn Vizin. The noble families of Osfelin are on edge, their once peaceful lives disrupted by uncertainty and fear. Rumors swirl among the elite, with whispers of conspiracy and intrigue echoing through the halls of their grand estates.

## History

The Silverlight District has long been the seat of power and privilege in Osfelin, its history intertwined with that of the royal family. Over the centuries, the district has been home to generations of fey nobility, each leaving their mark on its elegant streets and grand architecture. Today, the Silverlight District remains a symbol of wealth and status, a beacon of luxury and opulence in the heart of the city.

## Notes

