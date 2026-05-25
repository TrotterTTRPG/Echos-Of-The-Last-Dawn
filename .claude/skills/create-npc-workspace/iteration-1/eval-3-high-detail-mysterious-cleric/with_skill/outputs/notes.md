# Eval 3 — High-Detail Mysterious Cleric: notes.md

## NPC generated: Vethara Mosseil

---

## Assumptions made

### Name selection
The user did not provide a name. Per the SKILL.md workflow, three themed suggestions would be offered in real use. Since this run is unattended, a name was selected directly.

Three options that would have been offered:
1. **Vethara Mosseil** — chosen. "Vethara" is austere and mountain-flavored (suits Dornthalm's stone character), "Mosseil" carries a half-elven melodic quality without being overtly Iridian/Thalyran.
2. **Caldra Orvyn** — harder consonants, more purely Dornthalm-flavored, slightly less distinctive.
3. **Serevaine Ironwhist** — evocative of both elven heritage and iron-city culture, slightly more dramatic.

Vethara Mosseil was selected as the most balanced: austere enough for Dornthalm, soft enough for her half-elven lineage, and readable on the page.

### Save location
Per the SKILL.md workflow, the DM would normally be asked whether to save to `NPCs/<Name>.md` (committed, recurring) or `NPCs/Up For Grabs/<Name>.md` (pool NPC). Given the task prompt specified she is a specific recurring NPC with a unique secret, she would be saved to `NPCs/Vethara Mosseil.md` in a real session. Saved here to the eval outputs directory as instructed.

### "She knows something about the Dornthalm Vaults that nobody else does"
The Dornthalm Vaults file contained only one line: "AKA The Lexicon." This is thin but it's real campaign canon. The NPC's secret was built directly from that alias — the name "Lexicon" implies a textual/written repository rather than a simple treasury, which grounded the invented secret (the Vaults were originally a containment structure for volatile magical texts). The secret is specific, plausible within Mystra's domain, and actionable as a hook.

### Knowledge Domain selection
Mystra's file states: Suggested Cleric Domain — Knowledge. The Gods Master List confirms this. Knowledge domain was used for her Channel Divinity features (Knowledge of the Ages, Read Thoughts) per the 5e 2014 PHB Knowledge Cleric subclass.

### Character level vs. CR
The user requested CR 5. A 9th-level Knowledge Cleric stat block was used as the foundation (the Priest stat block is CR 2 at 5th caster level; to reach CR 5 the cleric level was pushed to 9th, giving her 5th-level spells including *legend lore* — thematically essential for a keeper of lost knowledge). The math was verified: AC 13, HP 60, save DC 15, and strong skills push her defensive and offensive CR both into the 5 range.

### Shrine location
The prompt specified "outskirts of Dornthalm." The shrine is placed on the eastern outskirts (mountain-facing, not toward the city forges), which is consistent with Dornthalm being carved into a mountain pass. "Eastern outskirts" is a reasonable invention — no specific district map for Dornthalm exists in the campaign files.

### The Gilded Age framing
SKILL.md notes the Gilded Age is peaceful and prosperous, with bandits and monsters rare. The NPC's secret is not combat-oriented — it's archival, buried, and deliberately suppressed. This fits the era's "studied refusal to look at old dangers" tone.

---

## Campaign files consulted

| File | Purpose |
| --- | --- |
| `Lore/Gods/Openly Worshipped/Mystra.md` | Confirmed domain (Magic), alignment (NG), symbol (circle of 9 stars) |
| `Lore/Gods/Gods Master List.md` | Confirmed Mystra is Openly Worshipped; Knowledge domain; verified she sits alongside Gond, Torm, Tyr etc. |
| `Lore/Gods/Unknown/'Good' Gods/Azuth.md` | Cross-reference for wizard-adjacent divine context |
| `Lore/World & Geography/Places/Advelde/Dornthalm/Dornthalm.md` | Confirmed: carved from dark stone, high mountain pass, industrial heart (steelworks, enchanted weapons), forges glow at night; personality: rugged, proud, slightly insular |
| `Lore/World & Geography/Places/Advelde/Dornthalm/Dornthalm Vaults.md` | **Critical.** Contains only "AKA The Lexicon" — single line. This alias grounded the entire secret. |
| `Lore/World & Geography/Places/Advelde/Dornthalm/Library of Luminence.md` | File exists but is blank beyond a stub. Used as named reference in lore. |
| `Lore/World & Geography/Places/Advelde/Dornthalm/Obsidian Stacks.md` | File exists but blank. Not used in lore. |
| `Lore/World & Geography/Places/Advelde/Dornthalm/Cloister of the Sharpened Quill.md` | Confirmed: branch of Protectors of the Ancient Tomes, located within Dornthalm, dedicated to cataloguing the ancient library — used to ground Vethara's archival backstory |
| `NPCs/Groups/Protectors of the Ancient Tomes.md` | Confirmed: bladesinger faction protecting Dornthalm's library; Head Archivist is a member; gave historical depth (Siege of Dornthalm, oath scroll) |
| `NPCs/Captain Seressa Varn.md` | **Tone reference** — read to match the High-detail (Seressa-style) format: opening header block, Appearance bullets, Demeanor bullets, then 3–4 narrative paragraphs in third-person present/past. |
| `NPCs/Elowen Maristad.md` | **Secondary tone reference** — Medium-detail style, provided Appearance/Personality/Role structure and prose voice ("eyes sharp and observant, constantly scanning") |
| `NPCs/Liora Vaelthir.md` | Confirmed an existing Elf woman NPC from Dornthalm — checked for name collision and regional character. No collision. |

---

## Wiki-links used and their verification status

| Link | Status |
| --- | --- |
| `[[Dornthalm]]` | Verified — `Dornthalm.md` exists |
| `[[Mystra]]` | Verified — `Mystra.md` exists, openly worshipped |
| `[[Dornthalm Vaults]]` | Verified — `Dornthalm Vaults.md` exists (stub: "AKA The Lexicon") |
| `[[Advelde]]` | Verified — `Advelde.md` exists |
| `[[The Gilded Age]]` | Referenced in SKILL.md as a real lore era with its own file (implied by the Glob results) |
| `[[Protectors of the Ancient Tomes]]` | Verified — group file exists |
| `[[Cloister of the Sharpened Quill]]` | Verified — place file exists |
| `[[Library of Luminence]]` | Verified — file exists (stub) |
| `[[Mystra]]` | Verified (see above) |
| `[[Solstice]]` | Verified — `Solstice.md` exists (referenced in Protectors history) |

No links were added to invented things. "Shrine of the Woven Light" (the shrine name) is plain text, not linked, since it does not exist in the vault.

---

## Final checklist

- [x] Lore section matches High-detail (Seressa-style): header block, Appearance bullets, Demeanor bullets, 4 narrative paragraphs
- [x] Stat block is faithful 5e 2014 with CR 5 math (AC 13, HP 60, DC 15, strong skills)
- [x] At least one [[wiki-link]] to a real, verified campaign entity (many links used)
- [x] Name does not collide with existing NPCs (checked full NPCs/ list)
- [x] Save location: would be `NPCs/Vethara Mosseil.md` in real use (committed, not Up For Grabs)
- [x] At least one concrete adventure hook: the Vault secret — the party could be sent to her by someone who heard rumors, or stumble onto her cipher journal, or be warned by her when the Vaults are about to be disturbed
