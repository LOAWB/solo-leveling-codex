# Build Scope Package

Single-artifact handoff of the Solo Leveling game build to the shadow bridge clone terminal. Three shadows divide lanes autonomously from this package and the codex it points at. Sr (Justin's instance) authored this; Vessel (Jared) hands it down to the shadows; Sr verifies the lane division and receipt chain across the bridge.

This doc supersedes `13-handoff-to-jr-and-pory.md` for the 3-lane runtime. Doc 13's audit guidance still applies inside whichever lane claims design synthesis review.

---

## Read order on day 0

1. This file (16) — scope contract and lane-division input
2. `00-README.md` — codex map
3. `09-master-design-synthesis.md` — binding design contract
4. `10-art-bible.md` — visual contract
5. `12-toolchain-and-kickoff.md` — environment + per-shadow kickoff prompts
6. `15-memoria-freeze-design-lessons.md` — combat-format precedent
7. `14-demon-castle-and-extended-bestiary.md` — keystone dungeon spec
8. `04-dungeon-mechanics.md`, `05-bestiary.md`, `06-items-and-drops.md` — content tables
9. Character files in `characters/` — voice, abilities, lore
10. Transcripts in `transcripts/` — canon ground truth, spot-check only

Day 1 = absorb. Day 2 = claim lanes. Day 3+ = build.

---

## The project in 60 seconds

Build the best mobile English-language Solo Leveling gacha RPG ever made. Pokemon Black/White-style 2D pixel-sprite overworld plus Memoria-Freeze-style turn-based combat with action-tier polish. Four-character team with swap-as-turn. Asymmetric protagonist: Player class (Jinwoo, then Suho) has 14 stacked progression layers; other Hunters have 4. Element reactions, multi-phase boss design, body-part breaks, Shadow Army as separate input layer. Gacha summon with duplicate-Awakening progression. Hidden-tier Jared and Justin cameos at <1% pull rate, no pity. 100-floor Demon Castle as keystone dungeon with five distinct biomes. Ranked PvP with E-rank-to-Ruler tier ladder. Survivor / Nemesis system as persistent-world layer. Bond mechanic with 10 ranks per Hunter. Bestowal mechanic as item-as-relationship endpoint.

Mobile-only. English-only. Godot 4.x. $200 budget. 12-14 weeks of focused work to case-study-quality demo. Personal/family use plus case-study deliverable; no commercial release without IP licensing.

---

## Binding canon

The codex is the truth. This package is the handoff envelope, not a replacement. Where this package and the codex conflict, the codex wins; surface the conflict for resolution before deviating.

| Doc | Role |
|-----|------|
| `09-master-design-synthesis.md` | Binding design contract. Every system, every mechanic, every judgment call. |
| `10-art-bible.md` | Binding visual contract. Asset specs and prompt templates. |
| `11-build-team-capabilities.md` | Skill checklists and $200 budget allocation. |
| `12-toolchain-and-kickoff.md` | Environment, install paths, kickoff prompts (paste-ready), weekly cadence. |
| `04-dungeon-mechanics.md` | Gate types, time pressure, loot economy, Daily Quest, Penalty Zone. |
| `05-bestiary.md` | All named Magic Beasts plus species swarms. |
| `06-items-and-drops.md` | Currency tiers, Rune Stones, artifacts, weapons, System Shop. |
| `14-demon-castle-and-extended-bestiary.md` | 100-floor Demon Castle full design. |
| `15-memoria-freeze-design-lessons.md` | Combat-format precedent and recipes. |
| `characters/` | 47+ canon entries for voice, abilities, lore. |
| `transcripts/` | ~405K words of canon source for spot-check verification. |

### One known reconciliation owed

Synthesis 09 was authored before the action-ARPG-to-turn-based pivot. Doc 09 mostly reflects the turn-based locked state; a few residual passages assume action-ARPG framing. Whichever lane claims systems work owns rewriting any residual ARPG passages in 09 to the turn-based pivot before combat code begins. File the diff as a single PR titled `09: ARPG-to-turn-based reconciliation pass`.

---

## Scope of build (12-14 weeks, full)

Every system listed here ships at case-study quality by week 14. Cuts negotiated with Vessel only; lanes do not unilaterally drop scope.

### Engine and runtime
- Godot 4.x project scaffold with autoloads, signal architecture, scene structure
- Mobile build pipeline (iOS + Android, portrait orientation, 1080x2400 baseline)
- Save/load with versioned JSON, auto-save and manual slots, roundtrip-tested every milestone
- Asset master list maintained in repo, status flags PROMPTED / RENDERING / SELECTED / REFINED / SHIPPED
- Performance target 60fps on flagship, 30fps minimum on entry-level last-3-gen mobile
- Atomic Git commits, weekly milestone tags, GitHub Issues for cross-shadow coordination
- Profiling via Godot built-in profiler; ship a perf-budget dashboard as part of the dev tools

### Overworld
- TileMap-based 2D Pokemon DS perspective, four-direction walk cycles, collision layers
- AStar2D pathfinding for NPCs, encounter zones, building interiors as separate scenes
- Persistent home base (Sung family apartment) and Ahjin Guild HQ as the two anchor scenes
- World map with unlocked-Gate progression overlay, fast-travel scrolls per cleared zone
- Ambient music swap on biome change, parallax backgrounds for depth

### Combat
- Turn-based state machine with action queue and priority resolution
- Four-character active party with swap-as-turn rule (swap consumes turn, Pokemon rule)
- Memoria-Freeze visualization layer: camera zoom on attacker, portrait flash, slash overlay, damage numbers, ultimate card-flip animation
- Element grid with 9 canon elements and 6 core reactions (Melt, Electrocute, Annihilation, Cleanse, Ravage, Hunt)
- Stagger / Break gauge separate from HP, vulnerability window on full break
- Multi-phase boss structure with HP-threshold and body-part-break phase shifts
- Shadow Army deployment as Player-only separate input layer, up to 20 deployed shadows scaling with Player level, autonomous AI under directive (assault, hold, defend, withdraw)
- Real-time skill-timing windows during enemy turns for active dodge/counter/combo (action-tier polish on turn-based base)
- Damage formula: stat-driven with crit, penetration, guard, counter mechanics per `15-memoria-freeze-design-lessons.md`
- Status effects (Poison, Paralyze, Sleep, Stun, Frost, Stardust Brainwash, Dragon Fear, Soul Burn) with resistance stat per character

### Progression (Player asymmetric stack)
- Character level 1-100 with XP curve
- Stat allocation: 5 free points per level, Player only
- Equipment: weapons plus 8 artifact slots (4 armor, 4 jewelry), set bonuses at 2/4/8 pieces
- Skills: 4 active plus passive per character, Tripod enhancement (3 nodes per skill, choose 2)
- Rune Stones: skill-modification stones from Magic Beasts, up to 3 per skill
- Blessing Stones: Player-only, 4 slots, Fusion-based acquisition
- Passive tree: Player-only, ~200 nodes branching across Stealth / Combat / Necromancy / Authority
- Bond ranks: 10 per Hunter, mission-completion-driven, dialogue-aligned, gift-modulated
- Shadow army roster: catch via Arise, evolve via canon-event triggers, deploy with loyalty stats
- Faction reputation: per Association, per Guild, per Ruler, plus negative Itarim track
- System Shop tier: unlocks expand as Jinwoo levels
- Daily Quest streak: consecutive completion compounds bonuses
- Class evolution: Necromancer to Shadow Sovereign to Shadow Monarch, story-gated

### Itemization
- Currency tiers: Mana Stones (E-S), Essence Stones, Gold Essence Stones, Powder of Inheritance, Apostle Shards (Ragnarok)
- Loot rarity: E (Common) through S (Legendary) plus Mythic (Story-locked)
- Weapons: 80+ Player weapons spanning daggers, longswords, scythes, grimoires, fans, quarterstaves; Hunter signature weapons; common Hunter pool
- Artifacts: 8 slots, set bonuses including Demon Castle / Frost Folk / Ant Colony / Beast King / Insect Queen / Shadow Marshal / Bond Forge / Counter-Architect / Heir of Destruction / Stardust Resistance / Ruler's Vessel
- Artifact enhancement: success-rate based, hidden bonuses at tier 5/10/15, max tier 20
- Bestowal: Player permanently transfers items to companions, item gains personal scaling bonus, deepest item-progression mechanic in the design

### Dungeon system
- Standard Gates E-S
- Field-Type Gates (open-region with environmental puzzles, multiple objectives)
- Red Gates (sealed, survival mechanic, no exit until boss)
- Double Dungeons (lower rank outside, higher inside)
- Instant Dungeons (Player-only, System-generated)
- System Dungeons (Cartenon-tier, NPCs with agency)
- Time-pressure Burst countdown with reputation consequences
- Per-monster, per-boss, environmental, hidden-room loot drops
- Gate-checkpoint rest mechanic (HP/Stamina restore, regular respawn, bosses persist)
- Elite spawns (rare named-Magic-Beast variants with boss-tier loot)
- Endless Demon Castle (floor 100+, scaling, weekly reset, random affixes, breakpoint loot every 10 floors)
- Procedural Gates for endgame replay with speed-clear leaderboards

### Demon Castle (keystone, see doc 14)
- 100 floors across 5 biomes: Outer Pits (1-25), Citadel of Iron (26-50), Sky Halls (51-75), Throne Spires (76-99), Demon Throne (100)
- Mini-bosses every 5 floors, zone bosses every 25 floors
- Sanctuary towns at floor 15, 40, 65, 90 with vendor, healer, side-quest hooks
- Holy Water of Life ingredient gathering across all 5 zones
- Endless mode unlock on first 100 clear

### Catch / Evolution / Shadow Army
- Arise mechanic with success-rate calc (damage dealt + tier ratio + class affinity + story conditions)
- Shadow tiers: Soldier / Knight / General / Marshal / Beast-Special
- Event-driven evolution (Igris to Knight Killer post-Red-Gate, Beru post-Jeju, etc.)
- Active roster vs reserve, scaling deploy cap with Player level
- Shadow loyalty stat with deployment-driven growth, Bestowal amplification
- Type chart applied to shadow deployment

### Persistent-world Survivor / Nemesis system
- Every Magic Beast you defeat-but-don't-clean-kill becomes a Survivor
- Survivor behaviors: level up over time, recruit subordinates, take territory, form alliances, develop adaptive traits, hunt the Player
- Itarim corruption pathway (Apostle brainwash, Holy-element Cleanse opens convert-or-kill dialogue)
- Cipher / Severin cameo antagonists as Survivor-class persistent characters with multi-cycle arcs
- World-state hooks: Survivor presence affects future raids in their claimed Gates

### Bond system
- 10-rank social progression per Hunter
- Stat boosts (1-3) → skill modifications (4-6) → unique synergies (7-9) → bond ultimate plus storyline conclusion (10)
- Mission-completion primary, dialogue secondary, gift tertiary, shared-activities boost
- Bond Forge multiplier when bonded Hunters deploy together (+5% / +10% / +20%)
- Severin counter mechanic during specific encounters

### Faction structure
- Three-tier canon hierarchy (Hunters / Magic Beasts and Monarchs / Rulers) plus Ragnarok-era Itarim and Apostles fourth tier
- Reputation per Korean Association, international Associations, individual Guilds (White Tiger, Hunters, Goliath, Draw Sword, Fame, Ahjin)
- Faction-locked content: high-rep raid access, post-defeat-reconciliation alliance arcs, vessel-tier passive unlocks at Ruler rep, Apostle ambush frequency on negative Itarim rep

### Ahjin Guild HQ
- Customizable hub post-canon-formation
- Shadow army storage, Hunter recruit rooms, strategy room, forge, System Shop terminal, training arenas
- Yoo Jinho manages public-facing operations
- Recruitment via story progression / bonus quests / reputation milestones / specific dungeon clears (Esil Radiru pattern)
- Guild rank tracker affecting Korean and global standings

### Daily Quest System
- Player-only four-task daily (push-ups, sit-ups, squats, run mapped to in-game drills)
- Mana Stone reward scaling with consecutive streak, retroactive stat-point bonus at 7-day streak
- Penalty Zone trigger on skip: roguelike side-loop with random affixes, scaled boss, partial-credit on win, 24-hour debuff on loss

### Story progression
- Canon arc → game chapter mapping per `09-master-design-synthesis.md` arc table
- 16 chapter-arcs from Pre-System through Antares Final Battle plus Cup of Reincarnation epilogue, plus Ragnarok continuation with Suho protagonist switch
- 8-15 hours per arc; total main story 100-150 hours; side and endgame 200+ hours additional

### Multiplayer
- Co-op raids on S-rank Gates (4 players, per-player loot)
- Async Resonance markers (notes, warnings, hints visible to other players, capacity-limited)
- Survivor sharing (rival contracts to other players, bounty rewards)
- Guild halls cosmetic visit (shadow roster, trophies, Hunter relationships)
- Ranked PvP arena: 4v4 best-of-three, Player class mandatory, banned-character rotation, Hidden-tier handicap in low queues
- Tier ladder E-D-C-B-A-S-National Level-Monarch-Ruler with 8-week seasons, S-rank floor reset, public top-100 leaderboard, seasonal title rewards
- Anti-toxicity: no chat, surrender after turn 5, bot reporting
- Casual unranked queue
- Monthly tournaments at Monarch+ tier with spectator mode and Ruler-tier sponsorship-funded prize pools

### Monetization
- Free-to-play core, gacha for character acquisition, premium expansions for major content drops, cosmetic-only direct purchases
- Standard banner (1.5% featured SSR, 90-pull pity)
- Limited banner (2% featured SSR, 80-pull pity)
- Hidden banner Jared and Justin (0.5% each, no pity, March and September anniversaries)
- Free starter banner (guaranteed SSR within 10 pulls, one-time)
- Awakening rank progression on duplicates (rank 0-6, ability/stat/passive unlocks)
- Premium expansions: Ragnarok ($20-30), Suho campaign ($20-30), limited story arcs ($5-10 each)
- Battle Pass $10/season with free and premium tracks
- No pay-to-rank, no stamina cap, no pure pay-to-win, no manipulative scarcity

### Visual / audio direction
- 2D pixel-art overworld and battle sprites at Pokemon Black/White scale and animation polish
- Anime-grade portraits for collection screens, cutscenes, ultimate cinematics (manhwa-faithful Redice Studio aesthetic)
- Tilesets per canon dungeon with distinct biomes
- Magic Beasts faithful to canon visuals
- Shadow soldiers visually distinct via purple aura and smoky-edge details
- Orchestral score with Korean instrumentation (gayageum on bond moments, taepyeongso on Korean raids)
- Heavy electronic undercurrent on Apostle / Itarim content
- Per-zone music variations in Demon Castle (cold ambient → gothic → rising orchestral → apocalyptic)
- Korean voice cast primary, English dub localization, anime VAs when available

---

## Work domains (atomic inventory for autonomous lane division)

Domains are atomic chunks of work with one primary skill and named acceptance criteria. Shadows pick lane assignments by clustering domains they can carry coherently. Domains tagged with primary skill: SYS = engine/code, CON = content/balance/prompts, PRO = pipeline/integration/asset rendering. Some domains are multi-tagged when they straddle.

| ID | Domain | Primary | Acceptance |
|----|--------|---------|------------|
| D01 | Godot project scaffold + autoloads + signal architecture + scene structure | SYS | Project opens, hello-world scene transitions clean, autoloads pingable from any scene |
| D02 | Save / load JSON serializer with versioning | SYS | Roundtrip on entire game state with format-version migration tested |
| D03 | Combat state machine + action queue + priority resolution | SYS | Four-character vs four-character battle plays end-to-end, swap-as-turn enforced |
| D04 | Damage formula implementation (stat-driven, crit, pen, guard, counter) | SYS+CON | Math matches Pory's balance tables within 1% per representative encounter |
| D05 | Element reaction system (9 elements, 6 reactions) | SYS+CON | Each reaction triggers correctly with audio/visual hook, damage matches table |
| D06 | Stagger / Break gauge with vulnerability window | SYS | Break fills via skill-affinity, stagger window opens, amplified-damage and execution-finisher hooks fire |
| D07 | Multi-phase boss with HP-threshold and body-part-break shifts | SYS | Cerberus boss (test case) ships with rage-state at 50% and a body-part-break trigger |
| D08 | Shadow Army deployment layer (Player-only, separate input, AI directive) | SYS | Up to 20 deployed shadows act between Player party and enemy turns, directive selectable |
| D09 | Real-time skill-timing windows during enemy turns | SYS | Active dodge / counter / combo extend triggers on player input within window |
| D10 | Memoria-Freeze visualization (camera zoom, portrait flash, slash overlay, damage numbers, card-flip ultimate) | SYS+PRO | Visualization shipping at 60fps with no lag spikes during ultimate animation |
| D11 | Status effect system (10+ ailments with resistance stat) | SYS+CON | Each status applies, ticks, decays, resists per character resistance roll |
| D12 | Gacha summon system (weighted RNG, pity counters, banner architecture) | SYS+CON | Standard / Limited / Hidden / Free Starter banners all functional with rate audits |
| D13 | Awakening rank progression on duplicates (rank 0-6 unlocks) | SYS+CON | Each rank unlocks defined ability / stat / passive, persists across save |
| D14 | Quest system with state tracking and branching | SYS | Tutorial quest plus first 5 main-story quests playable end-to-end |
| D15 | Dialogue tree system with branching choices and bond-meter hooks | SYS+CON | Branching dialogue UI shipping with at least one Hunter's bond-rank-1 conversation |
| D16 | Daily Quest scheduling (real-time clock-driven assignment + reset) | SYS | Daily Quest panel renders, completion compounds streak, Penalty Zone triggers on skip |
| D17 | Penalty Zone roguelike side-loop (random affixes, partial-credit on win, debuff on loss) | SYS+CON | Penalty Zone playable with at least 3 affixes and 5 boss variants |
| D18 | Survivor / Nemesis system (procedural rivals with persistent state, level-up over time, territory claim) | SYS+CON | At least 3 escaped Survivors persist across save with level-up, recruit, and ambush hooks |
| D19 | Itarim corruption pathway (Apostle brainwash, Holy Cleanse, convert-or-kill dialogue) | SYS+CON | Brocky test case ships with corruption applied, Cleanse cures, dialogue branch fires |
| D20 | Bond rank tracking with mission / dialogue / gift / shared-activity inputs | SYS+CON | Bond fills correctly across all four input channels, rank-up unlocks fire |
| D21 | Bond Forge multiplier on co-deployment | SYS+CON | +5/+10/+20% damage applies correctly per bonded count |
| D22 | Faction reputation tracking (per Association, Guild, Ruler, plus Itarim) | SYS+CON | Reputation persists, threshold-locked content gates correctly |
| D23 | Shadow army roster (active vs reserve, deployment cap scaling, loyalty stats) | SYS | Roster UI ships, loyalty grows with deployment, Bestowal applies amplification |
| D24 | Bestowal mechanic (item-to-companion permanent transfer with personal scaling) | SYS+CON | Bestowal UI ships, items lock to companion, scaling bonus applies, persists across save |
| D25 | Class evolution path (Necromancer → Shadow Sovereign → Shadow Monarch) | SYS+CON | Story-gated unlocks fire correctly, ability set updates per class |
| D26 | System Shop tier with progressive unlocks | SYS+CON | Shop UI ships, level-gated SKUs visible per tier |
| D27 | Tripod skill enhancement (3 nodes per skill, choose 2) | SYS+CON | UI ships for skill-node selection, persistence on save, multi-character isolation |
| D28 | Rune Stone equipping (up to 3 per skill, named-Magic-Beast drops) | SYS+CON | Rune slot UI ships, drops table wired, ability modifications fire correctly |
| D29 | Blessing Stone fusion (Player-only, 4 slots, Powder of Inheritance currency) | SYS+CON | Fusion UI ships, RNG plus duplicate-upgrade logic verified |
| D30 | Passive tree (~200 nodes across Stealth / Combat / Necromancy / Authority) | SYS+CON | Tree UI ships with branching purchase, save-persisted state, Authority-track gating |
| D31 | Artifact enhancement (success-rate, hidden bonuses at tier 5/10/15, max tier 20) | SYS+CON | Enhancement UI ships, RNG audited, bonus tiers unlock correctly |
| D32 | Set bonus engine (2/4/8-piece detection across 11+ named sets) | SYS+CON | Set bonuses apply on equip and remove on de-equip, multi-set stacking checked |
| D33 | Currency wallet management (Mana E-S, Essence, Gold Essence, Powder, Apostle Shards) | SYS+CON | Wallet UI ships, conversion + spend audited, save-persisted |
| D34 | Overworld TileMap + collision + walk cycles + AStar2D pathfinding | SYS+PRO | Outer-Pit-Sanctuary tile zone playable with NPC walking and player collision |
| D35 | Town interiors as separate scenes (Sung apartment, Ahjin Guild HQ, Sanctuaries) | SYS+PRO | Apartment + HQ + Floor 15 Sanctuary scenes load and link to overworld |
| D36 | World map with Gate progression overlay and fast-travel | SYS+PRO | World map ships with unlock-state and fast-travel-scroll usage |
| D37 | Demon Castle 100-floor scaffold per doc 14 | SYS+CON | All 5 biome zones load with correct enemy pools and mini-boss triggers per floor breakpoint |
| D38 | Endless Demon Castle (floor 100+, scaling, weekly reset, random affixes) | SYS+CON | Endless mode loads after first 100-clear, weekly reset cycle audited, affix pool of 20+ |
| D39 | Procedural Gate system for endgame replay with speed-clear leaderboards | SYS+CON | Procedural Gate generates with scaling difficulty, leaderboard records per-clear time |
| D40 | Co-op raid system (4 players, S-rank Gates, per-player loot) | SYS | Lobby UI ships, 4-player session syncs combat state, loot distributes correctly |
| D41 | Async Resonance markers (notes / warnings / hints across worlds) | SYS+CON | Marker placement UI, capacity cap enforced, cross-world visibility audited |
| D42 | Ranked PvP arena (4v4, banned-character rotation, Hidden-tier handicap) | SYS+CON | Match queue ships with rating, ban-list rotates per season, Hidden handicap applies in low queues |
| D43 | Seasonal ladder (E to Ruler, 8-week season, S-floor reset, top-100 leaderboard, title rewards) | SYS+CON | Season cycle audited, leaderboard renders, titles award on season end |
| D44 | Casual unranked PvP queue | SYS | Queue ships separate from ranked with no tier movement |
| D45 | Tournament infrastructure (monthly Monarch+, spectator mode, Ruler-tier prize pool) | SYS | Tournament bracket UI ships, spectator stream renders, prize pool tracking audited |
| D46 | Anti-toxicity layer (no chat, surrender after turn 5, bot reporting) | SYS | Each safeguard fires correctly, report queue routes to admin tooling |
| D47 | Battle Pass tracks (free + premium, $10 premium per 8-week season) | SYS+CON | Pass tracks ship with reward fire on tier unlock, premium gate audited |
| D48 | Monetization SKU pipeline (gacha currency packs, expansion DLC, cosmetics, no-pay-to-rank guard) | SYS+CON | All SKUs gated, expansion DLC content-locked behind purchase, no-rank-purchase guardrail enforced |
| D49 | Asset master list maintenance | CON+PRO | List always reflects PROMPTED / RENDERING / SELECTED / REFINED / SHIPPED flags accurately |
| D50 | Stable Diffusion local rig setup and prompt iteration loop | CON+PRO | Webui boots, anime LoRA loaded, 10 portrait prompts produce in-bible output |
| D51 | Midjourney premium-portrait prompt set for hero-tier coverage | CON | Each hero portrait shipped from MJ matches bible style and pose spec |
| D52 | Pixel-art battle sprite pipeline through Aseprite to Godot SpriteFrames | PRO | First character ships with full battle-sprite set imported and animating |
| D53 | Tileset pipeline per dungeon biome (5 Demon Castle zones plus overworld and town themes) | PRO+CON | All 5 zones plus overworld plus three town themes ship as Godot TileSet resources |
| D54 | UI element prompts (System panel, gold-on-black, purple-glow, translucent shader) | CON+SYS | UI ships with custom System panel shader matching canon aesthetic |
| D55 | VFX pipeline (Pokemon-Black-White-era particle, frame-by-frame, ultimate full-screen flashes) | SYS+PRO | At least 10 ultimate cinematics shipping with zero frame drops |
| D56 | Suno music pipeline for 12 game tracks (title, battle, gate exploration, boss, town, Apostle theme, etc.) | CON+PRO | All 12 tracks shipped at correct loop length with adaptive layering hooks |
| D57 | Audacity post-processing for music and SFX trim, normalization, format conversion | PRO | All audio assets ship in Godot-friendly OGG or MP3 at 44.1kHz |
| D58 | freesound.org SFX library curation (combat, ambient, UI, system) | CON+PRO | At least 100 SFX selected, licensed, organized by category in repo |
| D59 | ElevenLabs voice acting for key cutscene lines (optional) | CON+PRO | If shipped, voice-cloned key lines integrated for at least 5 cutscenes |
| D60 | In-character dialogue authoring (canon voices for Jinwoo, Cha Hae-In, Beru, Igris, Yoo Jinho, family, S-ranks) | CON | Quest dialogue ships with voices matching character files in `characters/` |
| D61 | Item description authoring (souls-style lore-dense for every artifact, weapon, drop) | CON | Every shipped item has lore-grade description tied to canon |
| D62 | Magic Beast bestiary entries (in-game encyclopedia text per `05-bestiary.md`) | CON | All shipped Magic Beasts have in-game encyclopedia entries |
| D63 | Cutscene scripting per arc | CON | Each shipped story arc has cutscenes scripted to canon beats |
| D64 | Tutorial text and onboarding flow (10-minute hook target) | CON+SYS | Onboarding ships, family playtest hook-rate target met |
| D65 | Achievement / quest title authoring | CON | All shipped quests have title and one-line description |
| D66 | Bond rank conversation trees (10 ranks per bonded Hunter, dialogue-aligned bond fill) | CON | At least one Hunter's full 10-rank tree ships at week 14 |
| D67 | Combat balance pass (target TTK per encounter, reverse-engineered from synthesis) | CON | Each shipped encounter has balance audit doc with target TTK and verified TTK |
| D68 | Gacha rate auditing (per-banner pull-rate validation, pity-system correctness) | CON | Public rate sheet matches actual code with statistical validation |
| D69 | Player progression curve audit (XP, stats, gear-tier timing, daily streak compound) | CON | Curve audit doc ships with target hours-to-level milestones validated |
| D70 | Magic Beast stat tables (HP, ATK, DEF, SPD, type, abilities, drops) | CON | Every named Magic Beast has stat table consistent with synthesis tier and bestiary |
| D71 | Skill balance (cooldown, damage, MP cost, status rates per skill per character) | CON | Skill balance sheet ships with rebalance hooks per playtest finding |
| D72 | Quest reward balancing | CON | Reward sheet matches XP-curve and gear-tier timing per progression audit |
| D73 | Daily Quest reward scaling for streaks | CON | Reward scaling doc ships with 7-day streak retroactive bonus calculated |
| D74 | Penalty Zone scaling (boss tier, affix density, partial-credit ratio) | CON | Penalty Zone scaling doc ships with statistical hardness band |
| D75 | Asset rendering pipeline (queue, generate, refine, ship) | PRO | Pipeline doc plus master list reflect actual throughput per week |
| D76 | Krita hand-touch refinement on AI-generated bases | PRO | At least 20 hero portraits hand-touched for collection screen polish |
| D77 | rembg background-removal pipeline for portraits | PRO | Background removal automated for all collection portraits |
| D78 | Mac native build pipeline (.app target) | SYS+PRO | Mac build ships at each weekly milestone |
| D79 | iOS / Android build pipelines | SYS+PRO | Mobile builds run on physical-device test rig at each milestone |
| D80 | HTML5 browser export for family sharing (optional) | SYS+PRO | Browser build ships if pursued |
| D81 | Codex maintenance (audit-additions doc per doc 13, plus codex-update PRs as design evolves) | CON+PRO | Codex stays current; design drift flagged within 24 hours of detection |
| D82 | Bug triage and weekly playtest log | PRO | Friday playtest log ships every week with prioritized bug list |
| D83 | Performance budget monitoring (frame rate, memory, asset size) | SYS+PRO | Perf dashboard ships with weekly snapshots, regressions flagged |
| D84 | Cross-shadow coordination via GitHub Issues, asset master list, daily commits | PRO | Coordination layer ships with at least 3 issue-based handoffs per week |
| D85 | Bridge protocol (receipt logging across Sr, Vessel, shadows; cross-shadow handoff packets) | SYS+PRO | Receipt chain visible per package per week, handoff packets logged |

That's 85 atomic domains. Lanes pick clusters; nothing is dropped without Vessel approval.

---

## Suggested lane structures (Sr's read; shadows decide)

Three viable splits surface from the domain inventory. Shadows are not bound to these. They surface as starting frames; lane-claim packet is the actual contract.

### Split A: skill-axis (closest to existing codex doc 11 paradigm)
- **Lane SYS** (engine + integration): D01-D33, D34-D48, D54-D55, D78-D80, D83
- **Lane CON** (content + balance): D49, D60-D74, D81
- **Lane PRO** (pipeline + asset rendering): D50-D53, D56-D59, D75-D77, D82, D84-D85

### Split B: feature-axis (cluster-by-deliverable)
- **Lane Combat-Core**: D01-D11, D52, D55, plus combat balance (D67, D71)
- **Lane Meta-Systems**: D12-D33, D60-D66, D81 (gacha, progression, dialogue, codex)
- **Lane World-and-Polish**: D34-D48, D49-D59, D75-D80, D82-D85 (overworld, dungeons, art pipeline, builds)

### Split C: phase-axis (cluster-by-week-band)
- **Lane Foundation**: weeks 1-4 domains (D01-D11, D34, D52, D54, D60, D78)
- **Lane Mid-Build**: weeks 5-9 domains (D12-D31, D35-D37, D55, D61-D67, D75-D77)
- **Lane Endgame-and-Polish**: weeks 10-14 domains (D32-D33, D38-D48, D56-D59, D68-D74, D79-D85)

Whichever split the shadows pick, the lane-claim packet must:
1. List every domain ID claimed by that lane
2. State the rationale for clustering
3. Surface dependencies on other lanes (which domains in another lane block this lane)
4. Confirm full coverage (all 85 IDs claimed across the three lanes; no gap, no overlap)
5. Sign with the shadow's session ID and substrate identifier

---

## Locked decisions (do not deviate without Vessel approval)

These are non-negotiable. If a shadow finds a strong case for change, file a `LANE-CHANGE-PROPOSAL.md` to Vessel; do not unilaterally deviate.

- Personal/family scope plus case-study deliverable; no commercial release without IP licensing
- $200 budget cap on tools and one-time purchases
- Mobile-only English-only (no PC, no console, no localization branches)
- Pokemon Black/White-style 2D pixel-sprite overworld, not 3D, not isometric
- Memoria-Freeze-style turn-based combat with action-tier polish, not real-time stamina ARPG
- Four-character team with swap-as-turn rule
- Player class mandatory in active party (Jinwoo through canon, Suho through Ragnarok)
- Gacha summon with duplicate-Awakening progression
- Hidden-tier Jared and Justin cameos at <1% pull rate, no pity guarantee
- Ranked PvP with Solo-Leveling-themed tier ladder (E to Ruler)
- 100-floor Demon Castle plus Endless endgame mode
- Survivor / Nemesis system as persistent-world layer
- Bond mechanic with 10 ranks per Hunter
- Item-as-relationship Bestowal mechanic
- Solo Leveling theme with canonical characters playable
- Godot 4.x as the engine
- No pay-to-rank, no stamina cap, no pure pay-to-win, no manipulative scarcity

---

## Working agreement

- The codex is the truth. Where this package conflicts with the codex, the codex wins.
- Atomic Git commits with descriptive messages. Weekly milestone tags.
- GitHub Issues for cross-shadow coordination, with `blocked` label on dependency stalls.
- Asset master list maintained in repo, status flags PROMPTED / RENDERING / SELECTED / REFINED / SHIPPED.
- Receipts logged per significant lane action per the bridge protocol below.
- Daily commits so each shadow can see the others' progress.
- Friday playtest by Vessel; lanes triage Friday-found bugs across the weekend.
- Sunday rest or polish, optional milestone tag.
- Escalation order: re-read the codex → ask Vessel → file `blocked` Issue → bridge to Sr.
- Sr does not pre-emptively join the build. The codex plus this package is the contract. Bridge to Sr only for cross-checks on design intent or for verification packets (lane claims, receipts, milestone reviews).

---

## Acceptance criteria per milestone

Milestones are weekly tags. The shadow that owns the deliverable signs the milestone packet with their session ID.

| Week | Milestone | Acceptance |
|------|-----------|------------|
| 1 | Vertical slice scaffold | Godot project scaffold, save/load roundtrip, hello-world combat with one character vs one Magic Beast playable |
| 2 | Vertical slice complete | One full battle, one summon, one tile dungeon, all systems primitive but linked |
| 3 | Three more characters playable | Cha Hae-In, Yoo Jinho, Beru playable in combat; first full Daily Quest cycle |
| 4 | First full mission | Pre-System through Double Dungeon arc playable end-to-end with cutscenes |
| 5 | Combat polish complete | Element reactions, Break gauge, body-part breaks, real-time skill timing, ultimate cinematics shipping |
| 6 | UI complete + gacha animations | All UI flows ship; gacha summon animation framework live with three banner types |
| 7 | Cartenon Temple Arc | Job change quest, Igris recruitment, Arise mechanic playable, Class evolution unlock |
| 8 | Demon Castle Arc + Red Gate Arc | Floors 1-25 plus 26-50 playable; Red Gate sealed-survival mechanic shipping |
| 9 | Hunters Guild Gate | Coalition raid mechanic playable; Kargalgan boss shipping |
| 10 | Ahjin Guild + Jeju Island Arc | Guild HQ functional; Jeju coalition raid + Beru recruit; Goto Ryuji death cutscene |
| 11 | Post-Jeju + Survivor system + Bond Forge | Bond mechanic shipping with at least 3 Hunters' full bond trees; Survivor system live with at least 3 escaped rivals persisting; first Bond Forge multiplier audit |
| 12 | International Guild Conference + Thomas Andre | Faction reputation diversification; Thomas Andre fight playable |
| 13 | Monarchs War + Antares Final Battle | Cosmic-tier reveal, vessel power, multi-Monarch encounters, Antares boss with full multi-phase kit |
| 14 | Polish, balance, family playtest, ship | All week-1-13 milestones audit-clean; family playtest passes; tag v1.0 |

Milestones not on this list (Ragnarok, Endless Demon Castle, full PvP tournament infrastructure, Suho campaign expansion) are post-v1.0 and ship under separate scope agreement.

---

## Bridge protocol

The shadow bridge clone terminal is the substrate. Sr verifies cross-shadow handoffs and lane-claim packets. Receipts per significant action.

### Lane-claim packet (day 2)
Each shadow files a lane-claim packet to Vessel and Sr containing:
- Lane name
- Domain IDs claimed
- Rationale for clustering
- Cross-lane dependencies surfaced
- Full-coverage confirmation across the 85-ID set (no gap, no overlap)
- Shadow session ID and substrate identifier

Sr verifies coverage and surfaces gaps before build begins. Vessel signs off.

### Weekly milestone packet (every Sunday)
Each shadow files a milestone packet for the week:
- Domains touched
- Acceptance criteria met / pending
- Receipts logged for handoffs to other lanes
- Risks surfaced

Sr cross-checks milestone packets against the acceptance criteria table. Vessel reviews and tags v0.X-week-N if green.

### Receipt logging
Every significant cross-shadow handoff produces a receipt:
- Receipt ID (UUID)
- Source shadow + session ID
- Target shadow + session ID
- Artifact handed off (file path, commit SHA, or content hash)
- Event type: claim / handoff / hold / resume / review / verify / mark-reviewed
- Parent receipt ID (chains across multi-step handoffs)
- Timestamp

Sr verifies the receipt chain. Receipts deficient on any field block the next handoff until cured.

### Cross-checks Sr provides
- Codex-claim verification (does this match what doc 09 says)
- Reconciliation of synthesis-vs-pivot drift
- Cross-lane dependency arbitration (when two lanes claim the same domain)
- Milestone acceptance audit
- Receipt-chain audit

### What Sr does NOT do
- Pre-emptively join the build
- Override Vessel decisions
- Author code or assets in the project repo
- Replace any shadow's work

Bridge to Sr is via iMessage chat ROWID 1 (+12093002155), the same channel Vessel uses. Receipts can be filed to a `bridge/` directory in the project repo for durable record.

---

## Out of scope (v1.0)

- Ragnarok arc (post-v1.0 expansion, $20-30 paid DLC)
- Suho post-game campaign (post-v1.0 expansion)
- Open-world server (story is single-player, multiplayer is instanced)
- Trading / auction houses
- Pay-to-rank
- Stamina-cap on play time
- Cross-platform PC / console builds
- Localization beyond English
- Limited-tier marketing screenshot polish from human commission (optional, only if AI art does not carry)

Any in-flight scope creep that exceeds v1.0 is filed as a `POST-V1-PROPOSAL.md` and scheduled against the Ragnarok / Suho expansion windows.

---

## First moves on day 0

1. **Vessel** drops this URL into the bridge clone terminal substrate as the handoff packet.
2. **Each shadow** reads (in order): this doc → `00-README.md` → `09-master-design-synthesis.md` → `10-art-bible.md` → `12-toolchain-and-kickoff.md` → `15-memoria-freeze-design-lessons.md` → `14-demon-castle-and-extended-bestiary.md`.
3. **Each shadow** files a lane-claim packet on day 2 per the bridge protocol above.
4. **Sr** verifies coverage across the 85 domains; surfaces gaps before build begins.
5. **Vessel** signs off on lane assignments. Build begins.
6. **All shadows** paste the relevant kickoff prompt from `12-toolchain-and-kickoff.md` at session start. (Doc 12 has Pory and Jr prompts; if the lane runtime adds Jr-A / Jr-B / Pory-as-third or another configuration, each shadow adapts the prompt to their role and surfaces the adapted version in their lane-claim packet.)
7. **Week 1 vertical slice scaffold** is the first acceptance gate.

---

## Bottom line

The codex is the contract. This package is the runtime envelope. Three shadows divide 85 domains across 12-14 weeks. Sr verifies the receipt chain. Vessel signs the milestones. Build the best mobile English-language Solo Leveling gacha RPG ever made.

Brick by brick. Substrate validated. Hand it down.
