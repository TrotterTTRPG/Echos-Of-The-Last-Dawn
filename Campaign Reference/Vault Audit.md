---
tags:
  - campaign-reference
  - dm-only
reviewed: 2026-09-20
through-session: "008"
status: reference
---

# Vault Audit

## Scope and limits

The review inventoried and read file bytes for 615 files outside `.git` before conflict cleanup, including hidden configuration. It examined 350 campaign Markdown notes at that point. Conflict resolution removed two redundant notes, leaving **348 source campaign notes** and **14 empty placeholders**. The new reference folder and root `AGENTS.md` are additional and are not counted in those source totals.

Campaign review covered setting/lore, PC and NPC histories, session records and scenarios, homebrew rules, idea pools, maps, character-sheet data, supporting JSON, and three ODS workbooks. PDFs were read through page text and their populated widget values; ordinary text extraction alone misleadingly omitted character values. A rendered character page, map overview images, and the sewer construct statistics image were inspected visually. This is not a claim of individual visual inspection of every map tile or every PDF page. The Paint.NET layered master was inventoried; its internals were not rendered. External links and linked stat-block pages were not fetched or balance-validated.

The initial attachment inventory contains 158 PNGs, four PDFs, three ODS workbooks, and one PDN master. Many PNGs are reusable cartographic tiles. `desktop.ini` files and plugin code/configuration are support files, not campaign lore. `.trash` contains only a desktop metadata file. The NPC workflow under `.claude` was read as authoring context.

The workbooks contain travel design alternatives and a six-sheet Loot Studios catalog. JSON includes five player-character utility records, three bestiary entries, four spell/condition definitions, eighteen city-event entries, forty camp/travel encounters, and saved/example fight data. Those records were inspected as supporting data; their presence does not establish that an event happened or that an encounter is appropriately balanced.

## Git conflict resolution — 2026-09-20

The pull from main had reached `fa12951`; reapplying local changes created conflicts. At the user's request, the resolution:

- Kept the full upstream session 008 Notes and preserved local potion-making intent and hammer-counterweight detail. Savone's local job lead was already represented in the fuller notes.
- Kept the outline's local removal of the mushroom event, plus upstream bullet formatting and the Savone attribution for Family Heirloom.
- Kept the expanded Electric Woman note in Potential Events; removed the obsolete Ideas copy whose local changes were only blank lines.
- Kept Tracy's Favor in Completed Events and removed the byte-identical untracked Scheduled Events duplicate. This settles duplicate storage, not which optional scene outcomes occurred.
- Preserved the currently valid Obsidian workspace layout. Git has no unmerged entries. The original stash was retained as a recovery copy; conflict files were also copied outside the vault before edits.

The resolution was staged, not committed or pushed. An independently changing Calendarium configuration was left untouched. The reference documents do not modify other source lore, mechanics, or scenario outcomes.

## Link audit

The audit checks local wikilink note/file targets, with Markdown preferred for extensionless names. It does not check heading anchors, block references, remote URLs, or plugin-generated links. **32 distinct target spellings** do not resolve. Some are typos or missing prefixes; others are intentional placeholders or concepts only represented in prose/images. They have not been bulk-renamed or filled with invented lore.

| Unresolved target (literal text) | Appears in |
| --- | --- |
| `Adventurer's Docket` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]] |
| `Aelar Aurielius` | [[Sessions/Completed Events/Delivering the Devil|Delivering the Devil]] |
| `Baby Hookmaw` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]] |
| `Blitz Lizards` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]], [[Lore/Narratives/Old/Hookmaw Egg Stolen|Hookmaw Egg Stolen]], [[NPCs/Up For Grabs/Darric Flamehand|Darric Flamehand]] |
| `Bronze District` | [[NPCs/Up For Grabs/Marin Saltwick|Marin Saltwick]], [[Sessions/Completed Events/Aelar's Companions Make a Bargain|Aelar's Companions Make a Bargain]] |
| `Calhoune Family` | [[Lore/World & Geography/Places/Advelde/Capital - Thalyra/Criminal Underground - Thalyra|Criminal Underground - Thalyra]] |
| `Copper Rhudenem` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]], [[NPCs/Up For Grabs/Brian Willow|Brian Willow]] |
| `Day of Challenging` | [[Lore/Gods/Gods Master List|Gods Master List]], [[Lore/Narratives/Old/Player Summary|Player Summary]] |
| `Effulgent` | [[Lore/The Cycle/The Cycle|The Cycle]] |
| `Fighter 1` | [[Sessions/Completed Events/Hookmaw Jr. Attacks!|Hookmaw Jr. Attacks!]] |
| `Fighter 2` | [[Sessions/Completed Events/Hookmaw Jr. Attacks!|Hookmaw Jr. Attacks!]] |
| `Fighter 3` | [[Sessions/Completed Events/Hookmaw Jr. Attacks!|Hookmaw Jr. Attacks!]] |
| `Fighter 4` | [[Sessions/Completed Events/Hookmaw Jr. Attacks!|Hookmaw Jr. Attacks!]] |
| `Fighter 5` | [[Sessions/Completed Events/Hookmaw Jr. Attacks!|Hookmaw Jr. Attacks!]] |
| `Golden Thistle` | [[Sessions/Session Notes/007/Outline|Outline]] |
| `Henrey` | [[Sessions/Completed Events/Livestock Disappearing|Livestock Disappearing]] |
| `Hookmaw` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]], [[NPCs/Up For Grabs/Darric Flamehand|Darric Flamehand]], [[Sessions/Completed Events/Tour of the Hall of Arcane Acuity|Tour of the Hall of Arcane Acuity]] |
| `hookmaw` | [[Sessions/Completed Events/Tour of the Hall of Arcane Acuity|Tour of the Hall of Arcane Acuity]] |
| `Iron Tankard` | [[Sessions/Completed Events/Aelar's Companions Make a Bargain|Aelar's Companions Make a Bargain]] |
| `Jeremy` | [[Sessions/Completed Events/Delivering the Devil|Delivering the Devil]] |
| `Kai,` | [[NPCs/Kai Yang|Kai Yang]] |
| `lyana Corvess` | [[Lore/World & Geography/Places/Advelde/Capital - Thalyra/Gold District/Hall of Metamagic and Theory|Hall of Metamagic and Theory]] |
| `Rockwood Trees` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]], [[Lore/Narratives/Old/Hookmaw Egg Stolen|Hookmaw Egg Stolen]], [[NPCs/Up For Grabs/Darric Flamehand|Darric Flamehand]] |
| `Sediment Snail` | [[Lore/Narratives/Naight's first days as an Adventurer|Naight's first days as an Adventurer]], [[NPCs/Up For Grabs/Brian Willow|Brian Willow]] |
| `Seressa Varn` | [[Sessions/Completed Events/Aelar's Companions Make a Bargain|Aelar's Companions Make a Bargain]] |
| `Sugarbend` | [[NPCs/Tansy Bellwether|Tansy Bellwether]], [[Sessions/Potential Events/Electric Woman|Electric Woman]], [[Sessions/Potential Events/The Two Truths|The Two Truths]] |
| `Thalyran Magitech` | [[Rules/Custom Items and Spells/Alchemy/Violuma Alchemy|Custom Items]], [[Sessions/Completed Events/Tour of the Hall of Arcane Acuity|Tour of the Hall of Arcane Acuity]] |
| `Tharvayne Family` | [[Lore/World & Geography/Places/Advelde/Capital - Thalyra/Criminal Underground - Thalyra|Criminal Underground - Thalyra]] |
| `The alchemist coughing` | [[Sessions/Completed Events/Hookmaw Jr. Attacks!|Hookmaw Jr. Attacks!]] |
| `The Golden Scepter` | [[Sessions/Completed Events/Chein Po goes to the black market|Chein Po goes to the black market]] |
| `Thelyra` | [[Lore/War/The Great War|The Great War]] |
| `Umbral` | [[Lore/The Cycle/The Cycle|The Cycle]] |

## Ambiguous source targets

No ambiguous note/file targets were found after consolidating the two duplicate notes. Repeated basenames such as Notes and Outline still require full paths when adding links.

## Empty placeholders

- [[Lore/War/The Shattering Wars|The Shattering Wars]]
- [[Lore/World & Geography/Places/Advelde/Advelde|Advelde]]
- [[Lore/World & Geography/Places/Advelde/Capital - Thalyra/Gold District/Lance of the Crown|Lance of the Crown]]
- [[Lore/World & Geography/Places/Advelde/Dornthalm/Library of Luminence|Library of Luminence]]
- [[Lore/World & Geography/Places/Advelde/Dornthalm/Obsidian Stacks|Obsidian Stacks]]
- [[Lore/World & Geography/Places/Advelde/Gray Mountains|Gray Mountains]]
- [[Lore/World & Geography/Places/Advelde/Horn Islands|Horn Islands]]
- [[Lore/World & Geography/Places/Advelde/Kareth's Crossing|Kareth's Crossing]]
- [[Lore/World & Geography/Places/Advelde/Rockmyst Valley|Rockmyst Valley]]
- [[NPCs/Aloria|Aloria]]
- [[NPCs/Edran Voss|Edran Voss]]
- [[NPCs/Hunter Maria|Hunter Maria]]
- [[Sessions/Session Notes/004/Notes|Notes]]
- [[The Moonhelm Family|The Moonhelm Family]]

The new reference links are checked separately to ensure this review adds no unresolved note/file targets. For substantive contradictions rather than navigation defects, see [[Campaign Reference/Open Questions and Continuity|Open Questions and Continuity]].

## Final validation

All 692 wikilinks across the ten new reference notes resolve to local files or notes. Git reports zero unmerged entries, and the Markdown/JSON scan found no conflict markers. The current workspace JSON parses successfully; staged and unstaged Git whitespace checks pass.

SHA-256 comparison with the initial inventory confirms that every other original file is unchanged. The only changed originals are the resolved session 008 Notes and Outline, the workspace layout, and the independently updated Calendarium configuration. The two removed files are the redundant Electric Woman and Scheduled Events Tracy copies described above. No commit or push was made; the recovery stash remains available.

## Follow-up clarification — 2026-09-20

After the initial review and validation above, the DM confirmed that the vault is private to the DMs and that session 008 ended with the party brought to the fairy village and meeting its elder. This was appended to session 008 Notes and reflected in the current state, home, active threads, questions, and root guidance. Player recollections are currently being gathered; no additional scene outcomes were inferred.
