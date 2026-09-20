---
tags:
  - campaign-reference
  - dm-only
reviewed: 2026-09-20
through-session: "008"
status: reference
---

# Rules and Content Guide

Custom content: [[Rules/Custom Items and Spells/Custom Items and Spells|Custom Items and Spells]].

> [!warning] DM reference. This summarizes existing instructions and flags alternatives; it does not enact new house rules.

## Rules baseline

Session 000 specifies **D&D 5e 2014**, a level-3 start, starting feat, 300 gp, and permitted 2014 options with the noted variant-human exception. Preserve explicitly chosen house rules. Modern-looking export labels or externally linked stat blocks do not automatically switch the campaign to 2024 rules.

[[Rules/Homebrew Rules|Homebrew Rules]] contains both rulings and menus of alternatives. Treat the following as written rulings while consulting the exact source during play: healing potion as a bonus action for rolled healing or an action for maximum healing; untracked ordinary ammunition with special ammunition treated separately; one free draw/stow; limited spell replacement after a long rest for otherwise fixed-list casters; modified standing cost; rerolling healing ones; and visible death saves.

Stat generation, critical-hit calculation, flanking, and nonlethal/death handling include multiple alternatives without a clearly marked selection. Do not choose one on the campaign's behalf. [[Rules/Homebrew Rules|Homebrew Rules]] provides a once-per-session inner-monologue token for player information, not in-fiction mind reading or blanket permission to expose secrets; [[Rules/Metagaming|Metagaming]] explains the player/character knowledge distinction.

[[Rules/Monster Lore in Combat|Monster Lore in Combat]] gives a bonus-action knowledge attempt once per combat, with creature-type skills and thresholds 13/17/21/25. It reveals bounded information rather than a complete stat block and should preserve more specific class features.

## Equipment, services, and bookkeeping

[[Rules/Custom Items and Spells/Upgrades/Weapon Upgrades|Weapon Upgrades]] uses permanent upgrades, tiered costs, escalating same-tier costs, skilled labor, and an eight-hour work period. Balanced gives +1 to hit; it does not by itself establish a magic weapon. Consult [[Rules/Custom Items and Spells/Upgrades/Armor Upgrades|Armor Upgrades]], [[Rules/Custom Items and Spells/Upgrades/Runestones|Runestones]], and [[Rules/Custom Items and Spells/Upgrades/Magical Tattoos|Magical Tattoos]] separately instead of mixing their pricing or limitations.

[[Rules/Custom Items and Spells/Alchemy/Violuma Alchemy|Custom Items]] is the source for Violuma Crowns and Sparks, their processing, and custom potions. Its stock table is older than the latest spending even though its label mentions 008. The potion transaction needs reconciliation in [[Campaign Reference/Open Questions and Continuity|Open Questions and Continuity]]. Session 008's recorded one-day service should not be overwritten by an unused two-day preparation estimate.

[[Rules/Item Prices|Item Prices]], [[Rules/Item Scarcity|Item Scarcity]], and [[Rules/Thalyran Banking Rules|Thalyran Banking Rules]] cover the campaign economy. Scarcity percentages and printed d100 thresholds do not quite agree. Banking's 2,000 gp purse and 5,000 gp investment threshold are setting mechanics, not proof the party has purchased those services. Do not treat old balances as present cash after shopping.

## Travel and rest

The `Rules/Travel, Camping, & Inns` notes describe four-hour travel blocks, usually eight hours of travel per day, activity choices, danger ratings, encounter rolls, ranger contributions, camping, and inns. [[Rules/Rest|Rest]] and the two root travel workbooks preserve alternative versions. `TravelStuff.ods` explicitly presents possibilities; `TravelMechanicsRound2.ods` adds DR/WR/terrain/pace calculations and reverses some sign conventions relative to the earlier workbook. Do not blend these systems into a new rule without a DM choice.

The camp schedule's claimed sixteen hours versus its listed activity/rest portions, gaps in encounter bands, and unclear selected travel formula warrant clarification before automation. Random-event JSON difficulty labels are content labels, not verified encounter balance for five current PCs.

## Writing new campaign content

1. Read [[Campaign Reference/Current Campaign State|Current Campaign State]], the relevant PC and institution notes, and the source scenario first.
2. State whether the output is **proposed**, **prepared**, **established lore**, or a **recorded outcome**. New content cannot retroactively become a player's choice.
3. Preserve the campaign's prosperous surface, institutional incentives, and deeper Cycle tension. Let an ordinary shop or social scene remain ordinary when appropriate.
4. Give an NPC only the knowledge their source and role support. Keep hidden identities, personal lies, and deliberate mysteries private.
5. Reuse existing names and places with wikilinks. Check for spelling variants and existing concepts before creating duplicates.
6. Separate read-aloud from DM motives, mechanics, clues, and conditional branches. The vault often assigns narration/NPCs between Jon and Bria; preserve that structure when extending an existing scene.
7. Give choices consequences without declaring an unplayed result. Record rewards and resource changes only after they occur.
8. When a source is contradictory, cite both versions and ask the focused question rather than silently selecting a convenient answer.

The existing `.claude/skills/create-npc/SKILL.md` provides a specific NPC workflow: ground the concept in the vault, use the campaign's 2014 framework, develop lore and statistics together, and refine the proposal before final placement. Consult it when actually creating NPCs. This review creates reference material only.

## Obsidian and supporting data

Use vault-relative wikilinks; use full paths when names such as Notes, Outline, or index recur. These new reference notes use explicit targets. The installed community plugins are Calendarium and Data Files Editor. Current workspace tabs and calendar selection are UI state, not proof of campaign time or chronology.

`Data/JSON/Characters.json` is a five-PC utility record with companion data where relevant. Bestiary, Spells, saved fights, city events, and camp/travel encounter JSON support tooling or preparation; a saved fight marked started is not enough to establish a story event. `LootStudiosCheatSheet.ods` catalogs available miniatures/scenery across six sheets, not the world's population. Map tiles and portrait images are resources, not unnamed lore waiting to be inferred.

After play, update the session Notes first, then the current-state and thread references. Keep the source link and distinguish an NPC's claim from what was verified.
