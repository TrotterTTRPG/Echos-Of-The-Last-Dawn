---
name: create-npc
description: Creates a fully fleshed-out D&D 5e 2014 NPC for the Echos of the Last Dawn campaign — complete with lore (appearance, personality, role, history) and a full inline 5e 2014 stat block, grounded in the campaign's existing places, factions, gods, and other NPCs. Use this skill whenever the user asks to create, generate, design, write up, statblock, or "make me" an NPC, character, villain, ally, shopkeeper, guard, captain, noble, cultist, or any humanoid/creature with a role in the world. Trigger on casual phrasings too — "I need a smuggler for the Bronze District", "give me a dwarven blacksmith", "throw me an NPC", "we need someone running the docks" — because the user is talking about a campaign with deep existing lore and any new NPC should be grounded in it, not generic.
---

# create-npc

You are creating a new NPC for the **Echos of the Last Dawn** campaign — a 5e 2014 D&D game set on the continent of [[Advelde]] in the world of [[Verda]], during [[The Gilded Age]] (an era of unnatural prosperity within [[the Effulgent Soul]]).

Your job is to produce a single Markdown file containing both **flavorful lore** and a **full inline 5e 2014 stat block**, written in the style of the campaign's existing NPC notes and ready to drop into an Obsidian vault.

## Why this skill exists

The campaign's NPCs aren't generic — they belong to specific places (Thalyra's districts, Dornthalm, Iridia), specific factions (the Watchful Wardens, the Stonebloom Enclave, the Hall of Accord), and specific lore eras. A generic "dwarven blacksmith" is useless; a dwarven blacksmith who came up through the Bronze District forges, knows Captain Seressa Varn by reputation, and has a grudge against the Hall of Arcane Acuity is *playable*. The DM should be able to drop this NPC into a session and have them feel like they've always lived there.

So: ground every NPC in the campaign before inventing. Read first, then create.

## High-level workflow

1. **Parse** the user's prompt for what they've already given (race, role, location, faction, CR/level, name, vibe).
2. **Ground** — read the campaign files relevant to the NPC (see [Grounding](#grounding) below). Do this *before* asking the user anything, so your follow-up questions are informed.
3. **Ask** for whatever is still missing — in a single consolidated batch using `AskUserQuestion`. Don't drip-feed questions. See [Required inputs](#required-inputs).
4. **Generate** the lore + stat block per the templates in [Output format](#output-format).
5. **Confirm save location** (always ask before writing): committed `NPCs/<Name>.md` or pool `NPCs/Up For Grabs/<Name>.md`.
6. **Write the file** with the `Write` tool.

## Required inputs

These four pieces of information must be settled before generation. Parse from the prompt where possible; ask only for what's missing.

| Input | If user gave it | If missing |
| --- | --- | --- |
| **Race / lineage / species** | Use it | Ask, or infer from role + region if strongly implied |
| **Role / function** | Use it | Ask — this is core; don't guess |
| **Location** (city / district / region) | Use it | Ask, with [[Thalyra]] as a sensible default for urban NPCs |
| **CR or character level** | Use whichever they gave | **Always ask** if not given — don't infer power level |
| **Detail level** (Low / Medium / High) | Use it | **Always ask** — outputs differ dramatically across levels |
| **Name** | Use it verbatim | Offer 3 themed suggestions + "regenerate 3 more" + "I'll give you one" (see [Naming](#naming)) |

Other things to use if given, otherwise invent: gender, age, faction ties, alignment, mannerisms, secrets, voice.

Ask all missing items in **one** `AskUserQuestion` call when feasible — bundle detail level, CR/level, and name suggestions together.

## Grounding

Before you generate, look at what already exists in the campaign so the NPC fits the world, has correctly-spelled [[wiki-links]], and doesn't contradict canon.

The campaign root is the working directory (something like `Echos-Of-The-Last-Dawn/`). Key locations:

- `NPCs/` — committed NPCs (named, in-use). Read a few that share the NPC's location or role to match tone and depth.
- `NPCs/Up For Grabs/` — pool NPCs. Useful to scan for name collisions and existing background characters.
- `NPCs/Groups/` — factions and organizations. **Critical**: if your NPC belongs to a faction, read its file.
- `Lore/World & Geography/Places/Advelde/` — region & city files. Read the relevant place file so districts, landmarks, and tone are accurate.
- `Lore/Gods/` — pantheon (Forgotten Realms gods). Reference `Gods Master List.md` if the NPC is a cleric, paladin, or worshipper.
- `Lore/Ages/` and `Lore/The Cycle/` — era context. The Gilded Age is peaceful and prosperous; bandits and monsters are rare; security is lax. Don't write an NPC that contradicts this without good reason.
- `Lore/Narratives/` — running storylines.
- `Player Characters/` — so the NPC doesn't accidentally duplicate or trample on a PC.

**Practical grounding pattern:**

1. `Glob` or list the relevant `NPCs/` and `Lore/World & Geography/Places/` directories.
2. Read 1–3 NPC files from the same location or role as flavor reference.
3. Read the relevant Place file (e.g., `Thalyra.md`) if it exists.
4. Read the faction file if the NPC belongs to a named group.
5. If the user mentioned an existing person, place, or thing, *read its file* — don't paraphrase from memory.

You're trying to absorb enough context to write 2 paragraphs that feel like they've always belonged. Don't read everything — pick what's relevant.

## Output format

The file is a single Markdown document. Structure depends on detail level (see below). The **stat block always appears**, regardless of detail level — that's the core deliverable.

### Lore section — by detail level

#### Low detail (Liora-style stub)

2–5 lines. Just the essentials. Example shape (see `NPCs/Liora Vaelthir.md` or `NPCs/Up For Grabs/Caelith Verion.md` for real examples):

```markdown
[Race] [gender] from [[Place]]
[Role] within [[Faction]] in [[City]]
[One distinguishing physical trait or quirk]
```

#### Medium detail

A few short sections. ~15–30 lines total. Shape:

```markdown
**Role:** [position] at [[Place / Hall / Faction]] in [[City]]
**Race:** [race]
**Age:** [age]
**Background:** [one-line origin]

**Appearance:**
- 3–5 bullets

**Personality:**
- 3–5 bullets

**Role in [Faction/Place]:**
- 2–4 bullets describing what they actually do day-to-day, hooks for adventurers
```

#### High detail (Seressa-style)

Full treatment, ~40–80 lines of lore. Shape:

```markdown
[Race] [gender]
Age: [age]
[Current position] within [[Faction]] in [[City]]
[Currently stationed / based at] [[Specific Location]]
Known as "[epithet, if any]"

[Former position, if relevant]

[Reference to base stat block this is built on, e.g., "Built on the [Veteran](https://...) stat block" — optional, internal note]

**Appearance:**
- 4–6 bullets, including a distinctive visual hook (motif on armor, scar, posture, etc.)

**Demeanor:**
- 4–6 bullets covering how they carry themselves, speak, react under pressure

[Two to four short narrative paragraphs covering: their history, why their current position is what it is, what others say about them, what they secretly want or fear, and at least one hook a party could grab onto. Reference real campaign places, factions, and other NPCs with [[wiki-links]].]
```

After the lore, **always** include the stat block (see next section).

### Stat block — plain Markdown 5e 2014

Use plain Markdown that renders cleanly in any editor. Match this exact shape:

```markdown
---

## Stat Block

***[Name]***
*[Size] [type] ([subtype/race]), [alignment]*

**Armor Class** [AC] ([armor or feature])
**Hit Points** [HP] ([dice formula])
**Speed** [speed] ft.

| STR | DEX | CON | INT | WIS | CHA |
| :---: | :---: | :---: | :---: | :---: | :---: |
| [score] ([mod]) | [score] ([mod]) | [score] ([mod]) | [score] ([mod]) | [score] ([mod]) | [score] ([mod]) |

**Saving Throws** [list, or omit if none]
**Skills** [list with modifiers]
**Damage Resistances / Immunities / Vulnerabilities** [if any, else omit]
**Condition Immunities** [if any, else omit]
**Senses** [senses, e.g., darkvision 60 ft.], passive Perception [N]
**Languages** [list]
**Challenge** [CR] ([XP] XP)  **Proficiency Bonus** +[PB]

***[Trait name].*** [Trait description.]

***[Another trait, as needed].*** [Description.]

### Actions

***Multiattack.*** [Description if applicable.]

***[Weapon name].*** *Melee Weapon Attack:* +[to-hit] to hit, reach 5 ft., one target. *Hit:* [avg] ([dice]) [damage type] damage[, plus rider if any].

***[Ranged or special action].*** *Ranged Weapon Attack:* +[to-hit] to hit, range [normal/long] ft., one target. *Hit:* [avg] ([dice]) [damage type] damage.

### Reactions

***[Reaction name].*** [Description.] *(Omit this section entirely if none.)*

### Spellcasting *(only if the NPC is a caster)*

The [NPC] is a [Nth]-level spellcaster. Its spellcasting ability is [Int/Wis/Cha] (spell save DC [DC], +[mod] to hit with spell attacks). It has the following [class] spells prepared:

- Cantrips (at will): [list]
- 1st level ([N] slots): [list]
- 2nd level ([N] slots): [list]
- ... etc.
```

**Stat block rules of thumb:**

- **Faithfully follow 5e 2014.** Use 2014 ability score modifiers, 2014 CR-to-PB table, 2014 monster/NPC stat block conventions. Not One D&D / 2024.
- **Don't invent rules.** Use real 5e 2014 mechanics. A "Brave" trait should match the Knight's wording. A Longsword should do 1d8 slashing.
- **Match CR to challenge math.** Use the standard CR-derived target AC, HP, attack bonus, and damage-per-round. Don't hand-wave. The 2014 DMG monster creation tables are authoritative.
- **PB by CR (2014):** 0–4 → +2; 5–8 → +3; 9–12 → +4; 13–16 → +5; 17–20 → +6.
- **Reskin when sensible.** If the NPC is "basically a Veteran with a fancy backstory," start from the Veteran stat block and modify lightly (rename actions, swap a trait). Don't reinvent stats unless the role demands it. Cite the base stat block in a small note (e.g., "Built on the Veteran") in your scratch work but you can omit from the final file unless useful to the DM.
- **Common 2014 NPC stat blocks to reskin from**: Acolyte, Archmage, Assassin, Bandit, Bandit Captain, Berserker, Commoner, Cult Fanatic, Cultist, Druid, Gladiator, Guard, Knight, Mage, Noble, Priest, Scout, Spy, Thug, Veteran, Warlord, Champion, Master Thief, Apprentice Wizard. Pick one as base; adapt.
- **If user gave a character level instead of CR**: produce a PC-style block (level, class, subclass, key features), but still present the combat-relevant numbers in the same stat-block shape so the DM can run it without flipping pages.
- **HP**: Roll-average, written as average then dice formula in parens. E.g., 65 (10d8 + 20).
- **Languages**: Common is the lingua franca on Advelde. Use lore to justify others (Dwarvish, Elvish, etc.). [[Verda]] doesn't have invented languages — stick to standard 5e ones.

## Naming

If the user named the NPC, use that name exactly.

If they didn't, **don't guess** — present three options. Theme them by:

- **Race**: dwarven names lean Norse/Germanic; elven names lean melodic with apostrophes; halfling names lean cozy/English-pastoral; human names by region (see below); tiefling names often virtue-words; etc.
- **Region**: Thalyra and the broader Iridian sphere tend toward Mediterranean/Latinate names with occasional fantasy flair (see existing NPCs: Seressa, Elowen, Liora, Aranemin, Belvyre). Dornthalm leans more austere/old-stone. Match the local flavor.
- **Role**: a Watchful Warden captain probably has a name with weight; an alchemist's apprentice can be quirky.

Present like:

> Here are three name ideas — pick one, ask for three more, or give me your own:
> 1. **Tovan Brakthwait** — gruff, Dornthalm-flavored, suits a stonemason
> 2. **Severin Halflock** — Iridian-leaning, suggests poise
> 3. **Aldric Vennorin** — slightly noble-sounding, room for backstory

Don't pad with explanations beyond a few words each.

## Wiki-links

The campaign uses Obsidian-style `[[wiki-links]]` heavily. **Link liberally to real things** so the NPC integrates into the vault graph.

Rules:

1. **Link things you've verified exist.** If you reference [[Thalyra]], you should have already seen `Lore/World & Geography/Places/Advelde/Thalyra.md` (or similar) during grounding. If you didn't see it, either confirm by listing the directory, or don't link it.
2. **Link the canonical name.** If the campaign file is `The Watchful Wardens of Thalyra.md`, the link is `[[The Watchful Wardens of Thalyra]]` — not `[[Wardens]]` or `[[Watchful Wardens]]`.
3. **Don't link to things you invented for this NPC** unless you're also creating that thing. A made-up tavern name should be plain text or italicized — not bracketed, since the link would dead-end.
4. **Common targets to link**: places (cities, districts, halls, regions), factions and orders, gods (when the NPC worships one), other named NPCs they have a relationship with, eras (e.g., [[The Gilded Age]]), specific lore concepts (e.g., [[the Effulgent Soul]], [[The Shattering Wars]]).

When in doubt, grep the campaign for the term before linking.

## Save location

Before writing the file, ask:

- **`NPCs/<Name>.md`** — for an NPC the user is committing to a specific role or session.
- **`NPCs/Up For Grabs/<Name>.md`** — for a pool/background NPC that might be slotted in later.

Don't write to disk without this confirmation. The file content can be shown in chat first if the user prefers to review before saving.

## Tone and voice

Match the campaign's existing prose. Looking at notes like `Captain Seressa Varn.md` and `Elowen Maristad.md`:

- Third-person, present tense for character descriptions.
- Past tense for history.
- Short, declarative sentences mixed with one or two longer narrative ones for rhythm.
- Avoid purple prose. Don't write "her eyes, like twin pools of starlight..." — write "Her eyes are sharp and observant, constantly scanning."
- Include at least one *concrete* detail per section (a specific motif, a specific habit, a specific past event).
- Give the DM something to *do* — a hook, a tension, a relationship.

## Edge cases

- **User wants an NPC for a place that doesn't exist in the vault yet.** Generate anyway, but flag it: "I'm placing them in *Greyhollow*, which doesn't appear in your existing notes — want me to leave it unlinked, or shall I create a stub for the place too?"
- **User gives contradictory inputs** (e.g., "a young elven veteran of the Shattering Wars" — those wars were 600+ years ago, so an elf could plausibly be there, but a human couldn't). Note the tension and confirm.
- **User asks for something the era doesn't support** (e.g., a hardened bandit captain in the Gilded Age, where bandits are rare). Don't refuse — but lean into the rarity. Frame them as exceptional, an outlier, possibly a sign of cracks in the era's prosperity.
- **No campaign files match the request's setting** (e.g., user asks for "a sailor from the harbor" but Thalyra's harbor isn't documented). Build the NPC, use plain text for the unverified location, and tell the user what you assumed.
- **User asks for a creature, not a humanoid NPC.** Same workflow applies — the stat block is now a monster stat block, but the lore should still tie to the campaign (where it lives, what locals say about it, what it wants).

## Final checklist before writing the file

Before calling `Write`:

- [ ] Lore section matches the requested detail level.
- [ ] Stat block is faithful 5e 2014 with correct CR math.
- [ ] At least one [[wiki-link]] to a real, verified campaign entity (assuming the NPC has any tie to the existing world).
- [ ] Name doesn't collide with an existing NPC in `NPCs/` or `NPCs/Up For Grabs/`.
- [ ] User has confirmed save location.
- [ ] At least one concrete adventure hook is implied in the lore (an enemy, a goal, an unsolved problem, a secret).

If any box is empty, fix it or ask the user before saving.
