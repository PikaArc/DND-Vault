---
tags:
  - "#Location"
  - "#Settlement"
art: z_Assets/Locations/Osfelin.jpg
publish: true
leader:
  - "[[Erefis Vizin]]"
  - "[[Salanae Vizin]]"
ruler:
  - "[[Salanae Vizin]]"
  - "[[Erefis Vizin]]"
settlementtype: Small City
defence: Formidable
---

> [!metadata|metadata]- Metadata 
>> [!metadata|metadataoption]- System
>> #### System
>>  |
>> ---|---|
>> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
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
>> **Type** | `INPUT[SettlementType][:settlementtype]` |
>> **Terrain** | `INPUT[Terrain][inlineListSuggester:terrain]` |
>> **Defences** | `INPUT[Defence][:defence]`
>> **Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>
>> [!metadata|metadataoption]- Demographics
>> #### Demographics
>>  |
>> ---|---|
>> **Dominion** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):dominion]` |
>> **Rulers** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):ruler]` |
>> **Leaders** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):leader]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Government Type** | `INPUT[GovernmentType][inlineListSuggester:governmenttype]` |
>> **Population** |  `INPUT[textArea:population]`
>
>> [!metadata|metadataoption]- Commerce
>> #### Commerce
>>  |
>> ---|---|
>> **Imports** | `INPUT[Goods][inlineListSuggester:import]` |
>> **Exports** | `INPUT[Goods][inlineListSuggester:export]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{settlementtype}][text]` |
> **Terrain** | `VIEW[{terrain}][text]` |
> **Defences** | `VIEW[{defence}]` |
> **Location** | `VIEW[{location}][link]` |
> ###### Demographics
>  |
> ---|---|
> **Rulers** | `VIEW[{ruler}][link]` |
> **Leaders** | `VIEW[{leader}][link]` |
> **Dominion** | `VIEW[{dominion}][link]` |
> **Government Type** | `VIEW[{governmenttype}][text]` |
> **Population** | `VIEW[{population}][text]` |
> ###### Commerce
>  |
> ---|---|
> **Imports** | `VIEW[{import}][text]` |
> **Exports** | `VIEW[{export}][text]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[Osfelin.jpg]]
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

> [!metadata|district]- Districts
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(location, this.file.link) AND contains(tags, "District")
> SORT districttype ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(location), ", ") AS "Location", join(link(organization), ", ") AS "Organization(s)"
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

Osfelin, the jewel of the Feywild, is a city steeped in magic and mystery. Nestled deep within an enchanted forest, its streets and bridges are woven from spells, leading travelers through a landscape of mystical rivers, verdant forests, and lush gardens. The city is home to a diverse array of inhabitants, including kitsunes, feys, elves, and other enchanting creatures.

At the heart of Osfelin lies the royal family, the Vizin Family, with King Erefis Vizin and Queen Salanae Vizin reigning over the realm. Their rule is absolute, and the city's inhabitants revere them as benevolent rulers.

Commerce thrives within Osfelin, with shops offering rare arcane ingredients, enchanted artifacts, and other mystical wares. The city's economy revolves around a unique form of magical currency, exchanged through spells and enchantments.

## Current Events

Tensions in Osfelin have surged following the sudden disappearance of Princess Fanlyn Vizin, the beloved daughter of King Erefis and Queen Salanae. The princess had ventured alone on a seemingly routine fetch mission into the enchanted forest surrounding the city. Despite her skills and familiarity with the Feywild, as days turned into weeks, there has been no trace of her return.

Whispers and speculations ripple through Osfelin like the winds through the trees. Some speculate that Princess Fanlyn may have stumbled upon a hidden danger within the forest, while others fear she may have fallen victim to dark magic or malevolent creatures lurking in the Feywild's depths.

The royal court is thrown into disarray, with King Erefis and Queen Salanae sparing no effort to find their missing daughter. Search parties scour the forest, guided by skilled trackers and powerful magic, yet each passing day brings no sign of Princess Fanlyn's whereabouts.

As anxiety grips the city, tensions between rival factions escalate, each seeking to exploit the princess's disappearance for their own gain. With the fate of Princess Fanlyn hanging in the balance, Osfelin teeters on the edge of turmoil, its once serene streets now shadowed by uncertainty and fear.

## History

Osfelin's history is shrouded in legend and myth, with tales of ancient fey lords and magical beings woven into its very fabric. The city's origins date back millennia, to a time when the Feywild was young and untamed.

Legend has it that Osfelin was founded by a powerful archfey known as the Dreamweaver, who wove the city into existence with threads of pure magic. Over the centuries, it grew into a thriving metropolis, its streets teeming with life and its gardens blooming with beauty.

Throughout its history, Osfelin has weathered countless challenges, from fey wars and invasions to natural disasters and magical cataclysms. Yet, through it all, the city has endured, standing as a testament to the resilience and strength of the fey who call it home.

## Notes

- The Vizin family's lineage is said to be blessed by the Feywild itself, granting them unparalleled magical abilities and wisdom.
- Osfelin's enchanted forest is home to a myriad of mystical creatures, from playful sprites and mischievous nymphs to ancient treants and powerful druids.
- The city's architecture is a blend of natural beauty and arcane craftsmanship, with buildings adorned with intricate carvings and shimmering enchantments.
- Travelers seeking adventure often flock to Osfelin in search of fame, fortune, and the thrill of exploring the untamed wilds of the Feywild.