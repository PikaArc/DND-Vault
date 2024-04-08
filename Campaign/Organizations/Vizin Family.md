---
tags:
  - Organization
art: z_Assets/Misc/PlaceholderImage.png
publish: false
hierarchy: "[[Vizin Family]]"
head:
  - "[[Erefis Vizin]]"
worship:
  - "[[Titania]]"
location:
  - "[[Osfelin]]"
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
> **Type** | `INPUT[OrganizationType][inlineListSuggester:organizationtype]` |
> **Hierarchy** | `INPUT[Null][suggester(optionQuery("Campaign/Organizations/Hierarchies"), useLinks(partial)):hierarchy]` | 
> **Head** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):head]` |
> **Steward** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):steward]` |
> **Parent Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
> **Worship** | `INPUT[inlineListSuggester(optionQuery(#Character AND !"z_Templates"), useLinks(partial)):worship]` |
> **HQ** | `INPUT[Null][suggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):hq]` |
> **Operating Areas** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |

> [!infobox]+
> # `=this.file.name`
> ###### `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
> | |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{organizationtype}][text]` |
> **Hierarchy** | `VIEW[{hierarchy}][link]` |
> **Head** | `VIEW[{head}][link]` |
> **Steward** | `VIEW[{steward}][link]` |
> **Parent Organization** | `VIEW[{organization}][link]` |
> **Worship** | `VIEW[{worship}][link]` |
> **HQ** | `VIEW[{hq}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|geography]- Geography
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Geography") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|county]- County
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(terrain, ", ") AS Terrain, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "County") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences, join(link(dominion), ", ") AS "Dominion"
> FROM "Campaign"
> WHERE contains(tags, "Settlement") AND econtains(organization, this.file.link)
> SORT dominion ASC, file.name ASC

> [!metadata|district]- Districts
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "District") AND econtains(organization, this.file.link)
> SORT districttype ASC, file.name ASC

> [!metadata|location]- Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type, join(link(organization), ", ") AS "Organization(s)"
> FROM "Campaign"
> WHERE contains(tags, "POI") AND econtains(organization, this.file.link)
> SORT poitype ASC, file.name ASC

> [!metadata|organizations]- Child Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE contains(tags, "Organization") AND econtains(organization, this.file.link)
> SORT organizationtype ASC, file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> FROM "Campaign"
> WHERE contains(tags, "Character") AND econtains(organization, this.file.link) AND !contains(condition, "Dead")
> SORT tags DESC, file.name ASC

## Overview

The Vizin family is a prominent lineage within the Seelie Fey Court, known for their mastery of druidic arts and their influence in the enchanting city of Osfelin. Led by patriarch Erefis and matriarch Salanae, the Vizins command respect and admiration from their peers, with their daughter [[Fanlyn]] poised to carry on their esteemed legacy.

## Etymology

The surname "Vizin" is believed to have roots in ancient Fey language, symbolizing "wisdom" and "balance," reflecting the family's deep connection to nature and their role as guardians of the [[Feywilds]] natural order.

## Activities

The Vizins are actively involved in various pursuits that reflect their druidic heritage. From rigorous combat training sessions under Erefis' guidance to nurturing fey animals with Salanae, their activities revolve around honing their skills, maintaining harmony with nature, and upholding their family's esteemed reputation.

## Society
### Beliefs

The Vizin family holds steadfast beliefs in the sanctity of nature and the importance of preserving the balance within the Feywild. They believe in the interconnectedness of all living beings and strive to protect the delicate ecosystem of their enchanted realm.

### Culture

The Vizins embody a blend of tradition and innovation in their culture, drawing from centuries-old druidic practices while embracing new perspectives and techniques to adapt to changing times.

### Religion

While not bound by conventional religious practices, the Vizins hold reverence for the elemental spirits and fey deities that govern the natural world. They pay homage to these entities through rituals and offerings, seeking their blessings for guidance and protection.

## Possessions

The Vizin family possesses a wealth accumulated over generations of druidic mastery, allowing them to indulge in luxuries and maintain a comfortable lifestyle within the opulent city of Osfelin. Their possessions include ancient tomes of druidic knowledge, enchanted artifacts, and a vast estate nestled amidst the verdant landscapes of the Feywild.

## History

The history of the Vizin family is intertwined with the annals of the Seelie Fey Court, with ancestors revered for their contributions to preserving the [[Feywilds]] natural beauty and defending it against threats from darker forces. Each generation of Vizins has upheld this legacy with pride, leaving a lasting imprint on the fabric of Fey society.

## Rumors & Legends

Whispers among Fey circles speak of ancestral legends surrounding the Vizin family, with tales of heroic deeds and mythical encounters weaving a tapestry of intrigue and wonder. Some rumors suggest hidden chambers within their estate containing ancient relics of immense power, while others speak of secret alliances forged with elemental spirits to safeguard the [[Feywilds]] borders.

