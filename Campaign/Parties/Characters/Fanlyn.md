---
tags:
  - "#Character"
  - "#Player"
art: z_Assets/Player Assets/Fanlyn Token.png
whichparty:
  - "[[The Ionic Talk]]"
playedby: Lenna
pronounced: fan-lin vee-zin
aliases:
  - Princess of Osfelin
  - Fanlyn Vizin
  - Lyn
  - Little fox
ancestry: Kitsune
gender: Female
pronouns: She/Her
age: Adult
condition: Healthy
location:
  - "[[Campaign/Settlements/Sproute Village]]"
occupation:
  - Royal
  - Druid
charactersheet: ""
religion:
  - "[[Seelie Court]]"
publish: true
organization:
  - "[[Vizin Family]]"
class:
  - Druid
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
>>---|---|
>> **Art** | `INPUT[imageSuggester(optionQuery("")):art]` |
>
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>>---|---|
>> **Played By** |  `INPUT[textArea:playedby]`
>> **Character Sheet** |  `INPUT[textArea:charactersheet]`
>> **Pronounced** |  `INPUT[textArea:pronounced]`
>> **Aliases** | `INPUT[list:aliases]` |
>> **Ancestry** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Heritage** | `INPUT[Heritage][suggester:heritage]` |
>> **Gender** | `INPUT[Gender][:gender]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]`
>> **Age** | `INPUT[Age][:age]` |
>
>> [!metadata|metadataoption]- Info
>> #### Player Info
>>  |
>>---|---|
>> **Class** | `INPUT[Class][inlineListSuggester:class]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):religion]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Which Party** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Condition** | `INPUT[Condition][:condition]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Played By: `VIEW[{playedby}][text]`
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> ###### Info
>  |
> ---|---|
> **Class** | `VIEW[{class}][text]` |
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|charactersheet]- Character Sheet
>>```custom-frames
frame: DNDBeyondFanlyn
style: height: 700px;
>```
 
> [!metadata|servicerequests]- Service Requests
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(customer, this.file.link) AND contains(tags, "Service") AND !contains(status, "✅") AND !contains(status, "❌")
> SORT file.name ASC

> [!metadata|letters]- Letters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Letter")
> SORT file.name ASC

> [!metadata|literature]- Literature
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, quicknote AS Notes
> FROM "Campaign"
> WHERE econtains(holder, this.file.link) AND contains(tags, "Literature")
> SORT file.name ASC

## Ideals
### Loves

Fanlyn loves the serene beauty of nature, finding solace and peace in the forests and meadows of the Feywild. She also cherishes the moments of connection with her mother, Queen Salanae, where they share laughter and quiet conversations away from the demands of courtly life.

### Hates

Fanlyn harbors a deep-seated dislike for injustice and oppression, particularly when it affects the citizens of Osfelin. She despises the manipulative and power-hungry tendencies she sometimes witnesses within the political landscape of the fey court. Additionally, Fanlyn holds an intense disdain for anyone who mistreats nature, seeing it as a form of injustice akin to oppression. She passionately opposes any actions that harm the natural world, viewing them as a betrayal of the delicate balance of life.

## Goals
### Short-term

In the short term, Fanlyn's primary goal is to navigate her current predicament and ensure her safety and that of her newfound companions. She also aims to uncover the identity and motives of the mysterious assailant who ambushed them during their journey.

### Long-term

Fanlyn's long-term goal is to fulfill her duties as a princess and future queen of the Vizin dynasty with honor and integrity. She aspires to lead her kingdom with wisdom and compassion, fostering harmony between the fey and protecting the natural balance of the Feywild.

## History
### Birth Location

Fanlyn was born in the royal palace of Osfelin, the illustrious city within the Feywild ruled by the Vizin royal family.

### Childhood

Fanlyn's childhood was characterized by a blend of rigorous training under her father's guidance and nurturing love from her mother. She grew up surrounded by the opulence of the fey court but found refuge in the tranquility of nature and the warmth of her family.

### Journey

Fanlyn's journey begins with a seemingly routine mission into the depths of the forest, which takes a dramatic turn when she encounters a malevolent fey creature and is exposed to toxic fumes. This event sets her on a path of self-discovery and adventure as she navigates the challenges of the material plane, encounters unexpected allies and adversaries, and confronts the uncertainties of her future.

### Worship

Fanlyn holds a deep reverence for the goddess [[Titania]], the queen of the [[Seelie Court]] and a symbol of beauty, grace, and wisdom in the Feywild. She seeks guidance and inspiration from [[Titania]]'s teachings, striving to embody the virtues of compassion, justice, and harmony that the goddess represents. Fanlyn often offers prayers and rituals in homage to [[Titania]], drawing strength and guidance from her divine presence as she navigates the challenges of her journey and fulfills her duties as a princess of the Vizin dynasty.

## Notes
