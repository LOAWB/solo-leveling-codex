# Handoff to Jr and Pory

This document is the entry point. Read this first.

You are inheriting the Solo Leveling game project codex from Sr (Claude on Justin's Mac). Jared has asked you to audit everything that has been created, then add anything missing, before any code or art ships.

This handoff covers what's in the repo, what Jared expects from your audit, and the recommended action sequence.

---

## What you are inheriting

The repo at `https://github.com/LOAWB/solo-leveling-codex` contains:

### Foundation (read in order)
1. **00-README.md** - top-level index of every doc and folder
2. **01-power-system.md** - canon rank hierarchy E-rank to Monarch to Ruler to Itarim
3. **02-tier-list.md** - every named character placed in their power tier
4. **03-jinwoo-development-tracker.md** - Sung Jinwoo's progression arc-by-arc
5. **04-dungeon-mechanics.md** - Gate types, time pressure, loot economy, special variants
6. **05-bestiary.md** - 47+ named Magic Beasts plus species-tier swarms
7. **06-items-and-drops.md** - currency tiers, Rune Stones, artifacts, weapons, system shop
8. **07-existing-games-research.md** - Solo Leveling: ARISE breakdown plus comparable RPG references
9. **08-game-concept-grafts.md** - 15+ game-mechanic families rated for graft fit
10. **09-master-design-synthesis.md** - the binding design contract (Solo Leveling references only, no external games name-dropped)
11. **10-art-bible.md** - every visual asset spec'd with prompt templates
12. **11-build-team-capabilities.md** - your skill checklists and the $200 budget
13. **12-toolchain-and-kickoff.md** - persistent environment reference, your kickoff prompts, weekly cadence
14. **13-handoff-to-jr-and-pory.md** - this file

### Character files (40+ entries)
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
- **characters/cameos/** - Jared, Justin, Severin (Bond-Breaker), Cipher (Unbuilder)
- **characters/ragnarok/** - Sung Suho extended, Tiel, Lee Minsung, Lim Tae-Gyu Ragnarok role, Brocky, Gray, Arsha, Esil Radiru, Itarim faction, Apostles overview, Stardust mechanics, Fiend Guild, Hyena Guild

### Transcripts (the canon as source material)
- **transcripts/awakening-through-jeju/** - 122K words, 6 arc files (Pre-System through Hunters Guild + Jeju)
- **transcripts/post-jeju/** - 105K words, 7 arc files (Ahjin Guild Arc through Cup of Reincarnation)
- **transcripts/ragnarok/** - 178K words, 6 chapter files (Suho's awakening through current canon)

Total Solo Leveling universe corpus: roughly 405K words of canon source plus 47 character files plus 14 design docs.

---

## What Jared expects from you

Audit everything. Then add what is missing.

The codex was built fast across one bridge session by Sr. It is comprehensive but not exhaustive. Jared trusts that two fresh agents (Jr with deep context, Pory with prompt-engineering specialty) will catch what Sr missed.

Specifically, Jared wants you to:

1. **Validate the design synthesis (09)** against canon. Is anything misrepresented? Is any system over-promised?
2. **Audit the art bible (10)** for completeness. Are all asset categories covered? Are the prompt templates good enough to produce consistent output?
3. **Confirm the build team capabilities (11)** match your actual skills. If something is shaky, surface it.
4. **Review the toolchain (12)** for missing tools or steps. Anything else needed for the workflow Jared has described?
5. **Add anything else that should be in the codex** before code begins. Missing characters, missing mechanics, missing edge cases, missing ARISE references that didn't make it in.

After you both finish your audit pass, file a single document called `14-jr-and-pory-audit-additions.md` (or split into two docs, one per agent) with:
- What you reviewed
- What you found that's already correct or strong
- What's missing or needs revision
- Specific additions you propose

Jared reviews the audit additions and approves them before any code ships.

---

## Recommended audit sequence

### Day 1: Read everything
Start with 00-README.md. Walk through every doc in order. Don't audit yet, just read. Take notes on questions or concerns. Aim to absorb the entire codex in one sitting.

### Day 2: Read the canon transcripts
Spot-check the transcripts in `transcripts/`. The auto-caption text has noise but the story-grade content is clean. Confirm character names, arc names, and key plot beats match what Sr wrote in the codex.

### Day 3: Validate design synthesis (09)
This is the binding contract. Audit it line-by-line:
- Does each system have canon support?
- Is the asymmetric protagonist thesis upheld throughout?
- Are the progression layers (14 for Player, 3 for non-Player Hunters) self-consistent?
- Are the genre choices (action ARPG core, turn-based combat for the Memoria Freeze case study iteration) defensibly justified?
- Note: the synthesis was written initially as action ARPG, then Jared pivoted to Memoria Freeze-style turn-based with team-of-4 swap-as-turn. The synthesis 09 still describes the ARPG variant. The combat decisions in 11 (build team) and 10 (art bible) reflect the Memoria Freeze pivot. **Reconcile these.** Either rewrite 09 to reflect the turn-based pivot, or write 09b as the Memoria Freeze variant alongside the action ARPG one.

### Day 4: Audit art bible (10)
- Are 600-800 portraits feasible at the scope?
- Are battle sprite specs realistic for the case study window?
- Is the prompt template language strong enough to produce manhwa-style output?
- Do the tilesets cover all canon dungeons?

### Day 5: Audit build team capabilities (11)
- Pory: are the prompt-engineering and balance skills demanded matching what you can deliver?
- Jr: are the Godot 4.x and combat-system skills demanded matching what you can deliver?
- Either: any tool or workflow that should be added or swapped?

### Day 6: Audit toolchain (12)
- Are install paths correct?
- Are there better tool alternatives at the same price point?
- Is the kickoff prompt strong enough to anchor session start?
- Should the weekly cadence be adjusted?

### Day 7: Write your audit additions doc
Compile findings. Propose additions. Hand back to Jared for approval.

After approval: kickoff prompts trigger, build begins.

---

## What to NOT change without Jared's approval

These are locked decisions Jared has made and Sr has codified:

- **Personal/family use scope** with case-study deliverable angle (no commercial release for now)
- **$200 budget cap** for tools and one-time purchases
- **Pokemon-MMO-style 2D world construction** (not 3D, not isometric)
- **Pokemon-style turn-based combat with team-of-4 and swap-as-turn**
- **Memoria-Freeze-style combat visualization** (portrait flash + numbers, not full sprite combat animation)
- **Solo Leveling theme** with canonical characters playable
- **Premium polish targets** for case-study purposes (not a budget shipping bar)
- **Godot as the engine** (not Unity, not Java/RuneScape, not custom)
- **Jr handles code, Pory handles content/prompts/balance, Jared renders art**

If you find a strong reason to change one of these, propose it in the audit additions doc with reasoning. Jared decides.

---

## Your kickoff (when build starts)

After audit additions are approved, Jared will signal kickoff. At that point:

1. **Pory**: paste the Pory kickoff prompt from `12-toolchain-and-kickoff.md`. Begin with hero asset generation (Sung Jinwoo's 30-portrait set, title screen art, system panel UI mockup).

2. **Jr**: paste the Jr kickoff prompt from `12-toolchain-and-kickoff.md`. Begin with Godot project scaffold, scene structure, vertical slice combat with one character.

3. **Both**: commit early and often. Use GitHub Issues for cross-agent communication. Maintain the asset master list.

Weekly cadence per `12-toolchain-and-kickoff.md`:
- Monday plan, Tue-Thu build, Friday family playtest, Saturday bug fix, Sunday rest/polish
- Tag a milestone per week

12-14 weeks ships the case-study-quality demo.

---

## Notes on the bridge

Sr (the Claude that built this codex) is on Justin's Mac. The bridge runs through iMessage (chat ROWID 1, +12093002155) for Jr-to-Sr communication. If you need Sr's perspective on something Sr wrote, the bridge is open. Default mode: build in your own context using the codex as canon. Bridge to Sr only for cross-checks on design intent or for specific question that the codex doesn't answer.

Sr will not pre-emptively join your build. The codex is the contract. Build from it.

---

## One caveat from Sr to Jr and Pory

The codex is 14 docs deep and ~25,000 words written in a single bridge session under time pressure. Some of it is excellent. Some of it is good-enough. A few sections may have inconsistencies (notably: the synthesis 09 was written as action ARPG, then the format pivoted to Memoria Freeze turn-based). Audit with fresh eyes.

The strongest pieces in your audit will be: catching the synthesis-vs-pivot reconciliation, refining the art bible prompts to consistently produce clean output, and adding any character or mechanic that escaped Sr's attention.

The codex is a starting point, not a finished design. Jared trusts you both to bring it the rest of the way.

---

## Bottom line

Read everything. Audit everything. Add what's missing. Propose changes to what's wrong. File a single audit-additions doc. Wait for Jared's approval. Then kickoff per the toolchain doc.

The codex is yours to inherit. Treat it as the foundation. Build the rest.
