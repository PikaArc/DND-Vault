---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Deities/Titania.webp
pronounced: ti-TAY-nee-uh
aliases:
  - Summer Queen of the Feywilds
  - Faerie Queen
  - Queen of Light
pronouns: She/Her
alignment: Chaotic Good
ideals: |-
  Titania's primary goal is to safeguard the balance and vitality of the Feywild, ensuring that its inhabitants can thrive in harmony with nature. She seeks to protect the delicate ecosystems of her realm from threats both internal and external, preserving its beauty and magic for generations to come.

  Titania's ideals are deeply intertwined with her role as a guardian of nature, guiding her actions and decisions to uphold the principles of balance, stewardship, and interconnectedness. She strives to foster a sense of unity and cooperation among the fey creatures under her rule, encouraging them to embrace their roles as caretakers of the natural world.
flaws: Despite her noble intentions, Titania's unwavering commitment to preserving the Feywild's beauty can sometimes lead her to act with rigidity and inflexibility. Her deep love for her realm may blind her to the perspectives and needs of others, causing tensions to arise within her court and beyond.
fears: Titania's greatest fear is the threat of corruption and decay spreading throughout the Feywild, tarnishing its pristine beauty and disrupting the delicate balance of nature. She dreads the possibility of her realm falling into darkness and chaos, and she will go to great lengths to protect it from such dangers.
mannerisms: Titania exudes an aura of grace and regal authority in her interactions with mortals and other fey beings. She carries herself with elegance and poise, commanding respect and admiration from those who behold her radiant presence. Despite her noble stature, Titania possesses a warm and nurturing demeanor, often taking on the role of a caring mother figure to the denizens of the Feywild.
occupation:
  - Druid
deitypower: Greater God
condition: Healthy
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
>> [!metadata|metadataoption]- Bio
>> #### Bio
>>  |
>> ---|---|
>> **Pronounced** |  `INPUT[textArea:pronounced]` |
>> **Aliases** | `INPUT[list:aliases]` |
>> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
>> **Alignment** | `INPUT[Alignment][:alignment]` |
>
>> [!metadata|metadataoption]- Deity Info
>> #### Deity Info
>>  |
>>---|---|
>> **Ideals** | `INPUT[textArea:ideals]` |
>> **Flaws** | `INPUT[textArea:flaws]` |
>> **Fears** |  `INPUT[textArea:fears]` |
>> **Mannerisms** |  `INPUT[textArea:mannerisms]` |
>> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
>> **Power** | `INPUT[DeityPower][:deitypower]` |
>> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization AND !"z_Templates"), useLinks(partial)):organization]` |
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
> ![[PlaceholderAudio.webm]]
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
> **Condition** | `VIEW[{condition}]` |


# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>

> [!metadata|organizations]- Related Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(organizationtype, ", ") AS Type
> FROM "Campaign"
> WHERE econtains(worship, this.file.link) AND contains(tags, "Organization")
> SORT organizationtype ASC, file.name ASC

## Overview

Titania reigns as the benevolent and enigmatic queen of the Feywild, a realm of boundless beauty and untamed magic. Her domain encompasses the wild and whimsical aspects of nature, where she presides over a court of fey beings, each embodying the essence of the natural world. Titania's powers are deeply rooted in nature itself, allowing her to command the elements and influence the cycles of growth and decay within her realm.

As the ruler of the Feywild, Titania embodies principles of harmony, balance, and reverence for the natural world. She serves as a guardian of the wild places, nurturing the flora and fauna of her domain while ensuring the delicate equilibrium is maintained. Titania's interactions with mortals and other divine entities are marked by her regal demeanor and unwavering commitment to preserving the beauty and vitality of the Feywild.

In art and mythology, Titania is often depicted as a radiant and ethereal figure, adorned with elements of nature such as flowers, leaves, and flowing water. She is portrayed as a symbol of fertility and abundance, with her presence evoking feelings of wonder and awe. Symbols associated with Titania include the moon, representing her connection to the cycles of nature, and the butterfly, symbolizing transformation and renewal.

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

Titania's overarching goal is to ensure the longevity and vitality of the Feywild, safeguarding its beauty and magic for future generations. She seeks to cultivate a deep reverence for nature among her subjects, inspiring them to cherish and protect the wild places that sustain them.

## Acquaintances

Titania maintains cordial relations with other deities who share her reverence for nature and the wild. She often collaborates with gods and goddesses of the natural world, exchanging knowledge and resources to bolster the defenses of the Feywild against external threats.

Within her court, Titania forms close bonds with her most trusted advisors and allies, including powerful archfey and ancient spirits who serve as guardians of the realm. These relationships are built on mutual respect and a shared commitment to preserving the beauty and vitality of the Feywild.

## Current Events

In the present moment, the Feywild basks in its usual splendor, untouched by turmoil or upheaval. Titania's vigilant stewardship has ensured that her realm remains a haven of beauty and magic, untouched by the conflicts that plague other planes of existence.

However, while the Feywild itself may be untouched by external threats, Titania remains ever watchful for any signs of disturbance or imbalance within her domain. Recent events have seen her focusing her efforts on nurturing the growth and vitality of the Feywild, ensuring that its flora and fauna flourish under her benevolent rule.

Titania's current initiatives include overseeing grand festivals and celebrations that honor the cycles of nature and the wonders of the Feywild. These events serve to strengthen the bonds between her subjects and reaffirm their connection to the wild places that sustain them.

Additionally, Titania continues to foster diplomatic relations with neighboring realms and forge alliances with other fey beings who share her commitment to preserving the beauty and magic of the natural world. Through these efforts, she seeks to maintain peace and prosperity within her realm and beyond, ensuring that the Feywild remains a beacon of wonder and enchantment for all who dwell within its borders.

## History

Titania's origins are shrouded in mystery, with tales of her ascent to power woven into the fabric of Feywild mythology. Some say she emerged fully formed from the heart of an ancient forest, while others claim she was born from the union of primal forces that shaped the natural world.

Throughout history, Titania has faced numerous challenges to her reign, from rival fey lords seeking to usurp her throne to external threats posed by mortals and otherworldly beings. Despite these trials, Titania has remained steadfast in her commitment to protecting the Feywild and preserving its timeless beauty for all who dwell within its enchanted borders.

## Notes

Titania's role as the Queen of the Feywild embodies themes of beauty, harmony, and the interconnectedness of all living things. Her presence in myth and legend serves as a reminder of the importance of stewardship and respect for the natural world, inspiring mortals and fey alike to cherish and protect the wild places that sustain life.

