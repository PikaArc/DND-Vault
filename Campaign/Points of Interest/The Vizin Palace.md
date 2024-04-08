---
tags:
  - "#Location"
  - "#POI"
art: z_Assets/Misc/PlaceholderImage.png
publish: true
location:
  - "[[Osfelin]]"
owner:
  - "[[Salanae Vizin]]"
  - "[[Erefis Vizin]]"
poitype:
  - Temple
aliases:
  - The House of the Vizin Family
pronounced: Vee-zin Palace
organization:
  - "[[Vizin Family]]"
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
>> **Pronounced** |  `INPUT[textArea:pronounced]`
>> **Aliases** | `INPUT[list:aliases]` |
>> **Type** | `INPUT[POIType][inlineListSuggester:poitype]` |
>> **Dominion** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):dominion]` |
>> **Owners** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):owner]` |
>> **Assistant** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):assistant]` |
>> **Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{poitype}][text]` |
> **Dominion** | `VIEW[{dominion}][link]` |
> **Owners** | `VIEW[{owner}][link]` |
> **Assistant** | `VIEW[{assistant}][link]` |
> **Organization** | `VIEW[{organization}][link]` |
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
> defaultZoom: 2
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

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview 

The Vizin Palace stands as the majestic residence of the royal family in Osfelin, serving as the seat of power and authority in the city. Situated in the prestigious Silverlight District, the palace is a symbol of the Vizin family's wealth, status, and influence. With its grand architecture, lush gardens, and opulent furnishings, the Vizin Palace is a testament to the splendor of the Feywild.

## Current Events

In the wake of Princess Fanlyn Vizin's mysterious disappearance, the Vizin Palace is gripped by sorrow and uncertainty. King Erefis and Queen Salanae are consumed by grief, their once joyous halls now filled with an air of melancholy. Courtiers whisper of dark omens and hidden dangers, fearing that the princess's absence may signal the beginning of darker times ahead.

## History

The history of the Vizin Palace is intertwined with that of the royal family, stretching back through generations of fey nobility. Built upon the foundations of an ancient fortress, the palace has stood for centuries as a symbol of strength and resilience. Over the years, it has been expanded and renovated, with each ruler leaving their mark on its grand halls and elegant chambers.

The palace has borne witness to triumphs and tragedies alike, from grand celebrations and royal weddings to fey wars and magical upheavals. Throughout it all, the Vizin family has remained steadfast in their dedication to the city and its inhabitants, their legacy enduring through the ages.

Today, the Vizin Palace stands as a beacon of hope and stability in a world filled with uncertainty, its gleaming towers and shimmering spires a reminder of the enduring strength of the royal family. As the heart of Osfelin, the palace serves as a sanctuary for its rulers and a symbol of unity for its people, a testament to the power of love, loyalty, and the bonds that bind them together.

## Notes

