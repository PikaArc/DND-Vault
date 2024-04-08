---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/NPC/Salanae Vizin.png
party1relation: Family
aliases:
  - Queen of Osfelin
  - Mother of Fanlyn Vizin
ancestry: Kitsune
gender: Female
pronouns: She/Her
age: Mature Adult
sexuality: Straight
alignment: Chaotic Good
pronounced: suh-luh-nay vee-zin
language:
  - Sylvan
  - Druidic
  - Common
  - Elven
ideals: Salanae values harmony and balance above all else, striving to maintain peace within her family and community. Her compassion and free-spirited nature guide her in fostering understanding and empathy among the fey creatures of the Feywild.
flaws: Despite her nurturing nature, Salanae can sometimes be overly protective, which may inadvertently hinder Fanlyn's independence. She also struggles with self-doubt, occasionally questioning her abilities as a mother and a wife, despite her compassionate demeanor.
fears: Salanae fears the possibility of losing her loved ones, particularly Fanlyn, to the dangers of the Feywild. She also harbors a deep-seated fear of failing to provide the support and guidance that her daughter needs, reflecting her nurturing and compassionate traits.
mannerisms: Salanae has a soothing voice and a gentle touch, often using comforting gestures to reassure those around her. Her free-spirited attitude shines through in her love for nature and her willingness to embrace new experiences, inspiring others to do the same.
occupation:
  - Royal
  - Druid
religion:
  - "[[Seelie Court]]"
condition: Healthy
publish: true
organization:
  - "[[Vizin Family]]"
location:
  - "[[Osfelin]]"
  - "[[The Vizin Palace]]"
ownedlocation:
  - "[[The Vizin Palace]]"
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
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>> ---|---|
>> **Pronounced** |  `INPUT[textArea:pronounced]` |
>> **Aliases** | `INPUT[list:aliases]` |
>> **Ancestry** | `INPUT[Ancestry][suggester:ancestry]` |
>> **Heritage** | `INPUT[Heritage][suggester:heritage]` |
> **Creature Type** | `INPUT[textArea:ancestry]` |
> **Creature Sub-Type** | `INPUT[textArea:heritage]` |
>> **Gender** | `INPUT[Gender][:gender]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
>> **Age** | `INPUT[Age][:age]` |
>> **Sexuality** | `INPUT[Sexuality][:sexuality]` |
>> **Alignment** | `INPUT[Alignment][:alignment]` |
>
>> [!metadata|metadataoption]- NPC Info
>> #### NPC Info
>>  |
>>---|---|
>> **Languages** | `INPUT[Language][inlineListSuggester:language]` |
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
>> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):religion]` |
>> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):ownedlocation]` |
>> **Current Location** | `INPUT[inlineListSuggester(optionQuery(#Location AND !"z_Templates"), useLinks(partial)):location]` |
>> **Condition** | `INPUT[Condition][:condition]` |
>
>> [!metadata|metadataoption]- Party Info
>> #### Party Info
>>  |
>> ---|---|
>> **Traveling With** | `INPUT[inlineListSuggester(optionQuery(#Party AND !"z_Templates"), useLinks(partial)):whichparty]` |
>> **Party 1 Relation** | `INPUT[Party1Relation][:party1relation]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Ancestry** | `VIEW[{ancestry}]` |
> **Heritage** | `VIEW[{heritage}]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> **Sexuality** | `VIEW[{sexuality}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Languages** | `VIEW[{language}][text]` |
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |


# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

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

## Overview

Queen Salanae Vizin is the gentle counterpart to her husband, King [[Erefis Vizin]], providing a nurturing and supportive presence in [[Fanlyn]]'s life. As a mother, she understands the importance of balancing discipline with compassion, offering [[Fanlyn]] a sanctuary of care and understanding amidst the structured rigors of her daily life. Salanae's warmth and empathy create a safe space for [[Fanlyn]] to express herself and seek solace, especially during moments of emotional turmoil or uncertainty. She cherishes their mother-daughter bond and treasures the simple joys of spending time together, whether it's tending to fey animals or sharing quiet conversations under the Feywild's starlit sky. Salanae is characterized by her compassionate nature, nurturing demeanor, and free-spirited attitude.

> [!column|2 no-title]
>
> 
>> [!metadata|ideals] Ideals
> `VIEW[{ideals}][text]`
>
>> [!metadata|flaws] Flaws
> `VIEW[{flaws}][text]`
> 
>> [!metadata|fear] Fears
> `VIEW[{fears}][text]`
>
>> [!metadata|mannerism] Mannerisms
> `VIEW[{mannerisms}][text]`

## Goals

Salanae's primary goal is to ensure [[Fanlyn]]'s happiness and well-being, embodying her nurturing and compassionate nature. She also seeks to promote harmony and understanding within her kingdom, fostering a sense of community and belonging among its inhabitants.

## Acquaintances

Salanae is well-respected within the Feywild community, known for her compassionate nature and unwavering dedication to her family. She has close ties with other fey leaders who share her values and concerns, forming alliances based on mutual trust and respect.

## Current Events

Recently, Salanae has been involved in organizing a festival to celebrate the changing of the seasons, infusing the event with her free-spirited energy and nurturing spirit to create a memorable experience for all.

## History

Salanae's upbringing in the heart of the Feywild shaped her compassionate and free-spirited nature, instilling in her a deep love for her homeland and its inhabitants. Her marriage to King Erefis brought stability and unity to their kingdom, allowing them to lead with wisdom and compassion.

## Notes

Salanae's compassionate and nurturing presence serves as a guiding light for those around her, fostering a sense of warmth and belonging in the Feywild.



