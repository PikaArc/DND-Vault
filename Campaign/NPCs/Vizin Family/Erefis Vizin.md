---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/NPC/Erefis Vizin.jpg
party1relation: Family
ancestry: Kitsune
heritage: 
gender: Male
pronouns: He/Him
age: Mature Adult
sexuality: Straight
alignment: Chaotic Good
condition: Healthy
aliases:
  - King of Osfelin
  - Father of Fanlyn Vizin
  - Formerly known as Erefis Maegi
pronounced: eh-reh-fis vee-zin
publish: true
ideals: Erefis values the preservation of druidic traditions above all else, believing that adherence to these ancient practices is crucial for maintaining balance and harmony in the Feywild. His determination and commitment to excellence drive him to uphold these ideals, serving as a guiding force in his leadership within the Seelie Fey Court.
flaws: Despite his love for Fanlyn and his dedication to their family's legacy, Erefis's strict adherence to tradition can sometimes lead to conflicts with his daughter's desire for independence and exploration. His relentless pursuit of excellence may also result in him being overly critical or demanding, unintentionally putting pressure on [[Fanlyn]] to meet his high expectations.
fears: Erefis fears the possibility of his family's druidic lineage fading into obscurity, unable to withstand the challenges of changing times and evolving landscapes in the Feywild. He also worries about Fanlyn's future and whether she will embrace her role as the next torchbearer of their legacy with the same fervor and dedication as he does.
mannerisms: Erefis carries himself with a sense of solemnity and gravitas, his every movement purposeful and deliberate. His disciplined nature is reflected in his unwavering commitment to his duties and responsibilities as both a king and a father. Despite his stern demeanor, Erefis's love for Fanlyn shines through in moments of quiet tenderness and shared appreciation for their druidic heritage.
religion:
  - "[[Seelie Court]]"
occupation:
  - Royal
  - Druid
language:
  - Common
  - Elven
  - Druidic
  - Sylvan
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

King Erefis Vizin is a prominent figure in the Seelie Fey Court, known for his unwavering dedication to druidic traditions and his relentless pursuit of excellence. As a father, he is deeply invested in ensuring that his daughter, [[Fanlyn]], carries on their family's legacy of druidic mastery. He believes in instilling discipline and pushing boundaries to unlock her full potential, even if it means adhering to strict training regimens. Despite his stern exterior, Erefis harbors a profound love for [[Fanlyn]] and sees her as the future torchbearer of their formidable druidic lineage. Erefis is characterized by his disciplined nature, determination, and commitment to tradition.

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

Erefis's primary goal is to ensure the continuity and prosperity of their family's druidic lineage, grooming [[Fanlyn]] to become a capable and respected druid in her own right. He also seeks to uphold the traditions of the Seelie Fey Court and safeguard the natural balance of the Feywild for future generations.

## Acquaintances

Erefis commands respect and admiration within the Seelie Fey Court, revered for his unwavering dedication to druidic traditions and his commitment to excellence. He maintains close ties with other prominent figures in the Feywild who share his reverence for nature and the importance of preserving its sanctity.

## Current Events

Recently, Erefis has been overseeing the preparations for an important druidic ceremony to honor the changing of the seasons, ensuring that every aspect of the ritual adheres to ancient traditions and customs.

## History 

Erefis's upbringing in the heart of the Feywild instilled in him a deep reverence for nature and the ancient druidic practices that govern their way of life. His ascension to the throne of the Seelie Fey Court marked the beginning of a new era of prosperity and stability, guided by his steadfast commitment to tradition and excellence.

## Notes

Erefis's disciplined and determined nature serves as a beacon of strength and stability in the ever-changing landscape of the Feywild, ensuring that their family's legacy endures for generations to come.




