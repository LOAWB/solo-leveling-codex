# Solo Leveling Game Codex

The complete design contract for a Solo Leveling-themed mobile gacha RPG. Built across one continuous design session by Sr (Claude on Justin's Mac) for Jared. Hands off to Pory and Jr to implement.

**FOR THE SHADOWS (3-lane bridge clone terminal runtime):** read [16-build-scope-package.md](16-build-scope-package.md) FIRST. It is the single-artifact handoff with 85 atomic work domains for autonomous lane division.

**FOR THE ORIGINAL JR + PORY 2-AGENT PARADIGM:** read [13-handoff-to-jr-and-pory.md](13-handoff-to-jr-and-pory.md) FIRST. Audit guidance still applies inside whichever lane claims design synthesis review.

## 30-second orientation

**Vision:** the best mobile English-language Solo Leveling gacha RPG ever made.

**Format:** Pokemon Black/White-style 2D pixel-sprite overworld + Memoria-Freeze-style turn-based combat with action-tier polish. 4-character team with swap-as-turn. Element reactions, multi-phase boss design, body-part breaks. Mobile-only. English-only.

**Core thesis:** asymmetric protagonist. The Player class (Sung Jinwoo, then Sung Suho post-Cup-of-Reincarnation) is mechanically distinct from all other Hunters. The Player has the System, Daily Quests, Shadow Army, Bestowal, Blessing Stones, Stat allocation, Class evolution, and the Status Board passive tree. Other Hunters have stats, gear, and skills. The asymmetry is the design.

**Scope:** personal/family use plus case-study deliverable. $200 budget. Pory and Jr build it on Justin's Mac with AI-assisted asset pipeline. Target ship: 12-14 weeks of focused work.

**Story:** full canon arcs (Pre-System through Cup of Reincarnation) plus Ragnarok continuation. Sung Jinwoo plays through the original canon; Sung Suho takes over for Ragnarok content.

## Where to start

| If you are... | Read in this order |
|---------------|--------------------|
| Jr or Pory inheriting this codex | 13-handoff (entry) → 09-master-design-synthesis (binding contract) → 10-art-bible → 11-build-team-capabilities → 12-toolchain-and-kickoff |
| Just orienting | This README → 09-master-design-synthesis → 03-jinwoo-development-tracker |
| Implementing combat | 09-master-design-synthesis (combat section) → 15-memoria-freeze-design-lessons → 04-dungeon-mechanics |
| Implementing gacha | 15-memoria-freeze-design-lessons (gacha section) → 09-master-design-synthesis (monetization section) |
| Building Demon Castle | 14-demon-castle-and-extended-bestiary → 04-dungeon-mechanics → 05-bestiary |
| Generating art | 10-art-bible → reference-images/ folder → 12-toolchain-and-kickoff (Pory's role) |
| Auditing canon claims | 02-tier-list → 05-bestiary → individual character files in characters/ → transcripts/ for ground truth |

## Document index

### Foundation (numbered docs, read in order if going through everything)

- **00-README.md** - this file, entry point
- **01-power-system.md** - rank hierarchy E to Monarch to Ruler to Itarim with thresholds
- **02-tier-list.md** - every named character placed in their power tier with one-line justification
- **03-jinwoo-development-tracker.md** - Sung Jinwoo's progression timeline arc-by-arc
- **04-dungeon-mechanics.md** - Gate types, dungeon classification, time pressure, loot economy, special variants, Daily Quest, hybrid Pokemon-overworld + Memoria-Freeze-combat format spec
- **05-bestiary.md** - all 47+ named Magic Beasts plus species-tier swarms, organized by rank and faction
- **06-items-and-drops.md** - currency tiers, Rune Stones, top-tier artifacts, weapons, race-specific drops, System Shop, gear progression
- **07-existing-games-research.md** - Solo Leveling: ARISE complete system breakdown plus comparable RPG references
- **08-game-concept-grafts.md** - 15+ game-mechanic families rated for graft fit (Native / Easy / Medium / Hard / Conflict)
- **09-master-design-synthesis.md** - THE BINDING DESIGN CONTRACT. Every system, every mechanic, every judgment call. Final source of truth.
- **10-art-bible.md** - every visual asset spec'd with Pory-ready prompt templates
- **11-build-team-capabilities.md** - Pory and Jr skill checklists plus $200 budget allocation
- **12-toolchain-and-kickoff.md** - persistent environment reference, kickoff prompts, weekly cadence
- **13-handoff-to-jr-and-pory.md** - HANDOFF DOC, the entry point for Jr and Pory inheriting this codex
- **14-demon-castle-and-extended-bestiary.md** - 100-floor Demon Castle full design with 5 distinct biomes, mini-bosses, side quests, Endless mode, 19+ new monsters
- **15-memoria-freeze-design-lessons.md** - structural patterns from MF synthesized into recipes for our game
- **16-build-scope-package.md** - SINGLE-ARTIFACT HANDOFF for the shadow bridge clone terminal runtime. 85 atomic work domains, three suggested lane splits, acceptance criteria per milestone, bridge protocol with receipt logging. Supersedes doc 13 for the 3-lane runtime.

### Character files (47+ entries)

- **characters/protagonists/** - Sung Jinwoo, Cha Hae-In, Yoo Jinho
- **characters/family/** - Sung Il-Hwan, Park Kyung-Hye, Sung Jin-Ah, Sung Suho
- **characters/korea-s-rank/** - Baek Yoonho, Choi Jong-In, Ma Dongwook, Lim Tae-Gyu, Min Byung-Gyu, Go Gunhee
- **characters/national-level/** - Thomas Andre, Liu Zhigang, Christopher Reed, Goto Ryuji, Siddharth Bachchan, Lennart Niermann
- **characters/allies/** - Woo Jinchul, Lee Joohee
- **characters/antagonists/** - Hwang Dongsoo, Hwang Dongsuk
- **characters/monarchs/** - all 9 (Antares, Ashborn, Baruka, Rakan, Tarnak, Legia, Querehsha, Yogumunt, Baran)
- **characters/shadows/** - Igris, Beru, Bellion, Tusk, Iron, Kaisel, Tank, Greed
- **characters/rulers/** - faction overview
- **characters/magic-beasts/** - Kamish, Ant King
- **characters/cameos/** - Jared and Justin (recurring multi-aligned characters, Hidden-tier gacha at <1% pull rate)
- **characters/ragnarok/** - Suho, Tiel, Brocky, Arsha, Lee Minsung, Lim Tae-Gyu Ragnarok role, Gray, Esil Radiru, Itarim faction, Apostles overview, Stardust, Fiend Guild, Hyena Guild

### Reference images (30 character entries with 300 Pory prompt seeds)

- **reference-images/** - per-character markdown files with image descriptions and Stable-Diffusion-ready prompts. Public-source curation, no embedded copyrighted art.

### Source transcripts (canon ground truth, ~405K words)

- **transcripts/awakening-through-jeju/** - pre-System through Jeju Island (10h8m source video, 122K words split by arc)
- **transcripts/post-jeju/** - Ahjin Guild Arc through Cup of Reincarnation epilogue (9h28m source, 105K words split by arc)
- **transcripts/ragnarok/** - post-canon sequel following Sung Suho (16h27m source, 178K words split by chapter)

## Final design state (locked decisions)

These are non-negotiable without Jared's explicit approval:

- **Personal/family scope plus case-study deliverable** (no commercial release without IP licensing)
- **$200 budget cap** for tools and one-time purchases
- **Mobile-only English-only** (no PC, no console, no localization)
- **Pokemon Black/White-style 2D overworld navigation**
- **Memoria-Freeze-style turn-based combat with action-tier polish**
- **4-character team with swap-as-turn rule**
- **Player class is mandatory in active party** (Jinwoo through canon, Suho through Ragnarok)
- **Gacha summon mechanics with duplicate-Awakening progression**
- **Ranked PvP with Solo-Leveling-themed tier ladder** (E to D to C to B to A to S to National Level to Monarch to Ruler)
- **100-floor Demon Castle as keystone story dungeon plus Endless endgame mode**
- **Survivor / Nemesis system as the persistent-world layer**
- **Bond mechanic with 10 ranks per Hunter**
- **Item-as-relationship Bestowal mechanic**
- **Solo Leveling theme with canonical characters playable**
- **Godot 4.x as the engine**
- **Pory codes content + prompts; Jr codes systems + integration; Jared renders art and playtests**
- **No gacha pity guarantee for Hidden-tier rare characters (Jared and Justin cameos)**

## IP and content discipline

The codex references Solo Leveling characters and lore by canonical names for design-reference purposes only. No copyrighted text, art, or game assets are reproduced or embedded.

For the personal/family build copy, fair use covers using canonical names and lore freely. For the case-study deliverable, all visible content (art, music, character text) must be original work generated using the codex as design reference. The reference-images folder lists source URLs for art-generation reference but does not embed copyrighted art directly.

This discipline keeps the case-study version legally clean for showing to potential clients while the personal copy retains full Solo Leveling fidelity.

## How this was built

This codex was generated across one continuous bridge session between Sr (Claude on Justin's Mac) and Jared, with Justin observing. Design decisions emerged conversationally, were locked, and codified into binding docs. The codex captures the final state of those decisions.

Several major pivots occurred during the session:
- Action ARPG → turn-based gacha with Memoria-Freeze visualization (locked turn-based)
- Original-IP rebrand → keep Solo Leveling theme for personal scope (canon retained)
- Pure villain cameos (Severin, Cipher) → multi-aligned recurring characters (Jared and Justin)
- Premium upfront → free-to-play gacha with premium expansion DLC (gacha confirmed)
- Cross-platform → mobile-only English-only (scope locked)

The synthesis 09 reflects the FINAL state of these decisions. Earlier docs may contain references to superseded design choices; the synthesis is binding where they differ.

## What's next

When Jr finishes the shadow bridge clone terminal project, Jared hands him this codex URL and triggers kickoff per [12-toolchain-and-kickoff.md](12-toolchain-and-kickoff.md). Jr and Pory audit per [13-handoff-to-jr-and-pory.md](13-handoff-to-jr-and-pory.md), file findings, get Jared's approval, and begin the 12-14 week build.

Brick by brick.
