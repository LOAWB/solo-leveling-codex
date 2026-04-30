# Master Design Synthesis

The unified design contract for the game. Every system from canon, every mechanic worth grafting from other RPGs, every judgment call made. Not code. Not a plan. The design.

This document supersedes individual recommendation files. Where they differ, this document is final.

---

## Vision (one paragraph)

You are not the strongest Hunter. You are the only Hunter who can become anything. The world has Gates, ranks, raids, and a strict hierarchy that says your power is fixed at awakening. The System on your screen is the System everyone whispers about, the one that broke Sung Jinwoo. It is broken for you too. The game is the loop of becoming: each Gate cleared rewrites your potential, each Magic Beast defeated joins your shadow army, each bonded ally rewrites the math of every fight. You start as the world's weakest. You end as the universe's apex. The space between is the game.

---

## The single thesis: asymmetric protagonist

Every other RPG promises that you are the chosen one. This game tells you you are the chosen one and proves it by making you mechanically distinct from every other character. You are the only one with the System. You are the only one who levels. You are the only one whose rank changes. You are the only one with Daily Quests, Penalty Zones, Inventory, Stat Allocation, Bestowal, Arise, Shadow Army, Blessing Stones, and the Shop. Every other Hunter has a fixed ceiling. They are NPCs and party members; you are the protagonist class.

This is the design fork in the road. Most RPGs treat protagonist and party as different stat sheets of the same template. Solo Leveling treats them as fundamentally different beings. **Lean into this hard.** Every system in this design is built around the asymmetry.

---

## Core gameplay loop (moment-to-moment)

You are at a Gate. You enter. Inside is a dungeon: monster zones, environmental puzzle, a boss room. You bring your party (3 Hunters + your shadow army). You fight with stamina-based combat (Souls feel: dodge, parry, strike with weight). You break boss body parts (Monster Hunter), trigger phase shifts, manage party tags (HoYoverse swap-action). You kill the boss. You Arise (extract its shadow). You get loot tiered E to Cosmic. You exit. You are slightly stronger. You go to the next Gate. The loop is hour-zero satisfying because the combat itself is good. The loop scales because every kill compounds (shadows + stats + items + bonds + Nemesis state of survivors + Daily Quest completion + System Shop currency).

The genre stack: action ARPG core (Souls feel + Monster Hunter hunt structure + Diablo itemization), with gacha-adjacent depth layers (artifacts + runes + blessing stones), with single-player Persona-tier social-bond layer, with Shadow-of-Mordor Nemesis endgame. You are not building a Genshin clone or an ARISE clone. You are building the game Solo Leveling fans always thought ARISE would be.

---

## Combat system

### Stance and rhythm
Souls-tier stamina-based combat. Light attack, heavy attack, dodge, parry, block. Stamina regenerates between strikes. Out-of-stamina = vulnerable. No infinite combos. Movement matters.

### Action commands per Hunter
Each Hunter has 4 active skills (basic, two skills, ultimate) plus a passive. Solo Leveling: ARISE has this shape; we keep it.

### Tags / character swap
You bring 3 Hunters + Jinwoo on most missions. You play one at a time. Tag-swap is fluid (HoYoverse tagging). On swap, the swapping-out character can leave a residual buff on the field (similar to Honkai Star Rail's tag system).

### Element reactions
Solo Leveling's elements are: Fire, Ice, Lightning, Light, Dark, Beast, Insect, Demon, Holy. Reactions when combining:
- Fire + Ice = Melt (massive single-target)
- Lightning + Water/Ice = Electrocute (status DoT)
- Dark + Light = Annihilation (raw damage)
- Holy + Demon = Cleanse (purifies brainwash, removes Stardust)
- Beast + Insect = Ravage (party damage to single)
- Light + Beast = Hunt (mobility burst)

### Shadow Army deployment
Jinwoo has a separate input for shadow command. Shadows are summoned/dismissed via System UI. They fight autonomously with command directives (assault, hold, defend, withdraw). Up to 20 shadows on the field at once depending on Player level. Shadows scale with Jinwoo's level and can level independently via combat.

### Body-part breaks (Monster Hunter graft)
Magic Beasts have 3-6 breakable parts. Breaking parts triggers phase shifts, drops body-part-specific materials, and disables specific boss mechanics (break Antares' wings = no Dive Phase).

### Boss fight structure
Multi-phase, with phase shifts triggered by HP thresholds, body part breaks, or environmental conditions. Each phase introduces new mechanics. WoW-tier raid encounter design (8-25 hunters for S-rank raids; 4 for standard raids; solo for Daily Quest content).

### Stagger / Break system (Lost Ark + ARISE graft)
Every enemy has a Break gauge. Filling it triggers a Stagger window where the enemy is vulnerable to amplified damage and execution finishers (the one-shot the Ant King kind of moment). Specific weapons have Break-affinity. Specific party comps optimize for Break.

---

## Progression layers (the asymmetric protagonist's eight onions)

Jinwoo (Player class) has these layers stacked. Other Hunters have only the first three.

1. **Character level** (1-100, like ARISE)
2. **Stat allocation** (5 free points per level, Player-only)
3. **Equipment** (weapons, 8 artifact slots, jewelry)
4. **Skill system** (4 active + passive per character)
5. **Tripod skill enhancement** (Lost Ark graft: each skill has 3 selectable enhancement nodes, choose 2)
6. **Rune Stones** (skill modifications dropped from Magic Beasts)
7. **Blessing Stones** (Player-only, 4 slots, fusion-based, Jinwoo-exclusive)
8. **Passive tree** (Player-only, ~200 nodes, branching paths around Stealth / Combat / Necromancy / Authority)
9. **Bond ranks with each ally** (10 ranks per Hunter, Persona 5 graft)
10. **Shadow army roster** (catch-evolve, party-management layer)
11. **Faction reputation** (Hunter Association, individual guilds, Rulers)
12. **System Shop access tier** (unlocks expand as Jinwoo levels)
13. **Daily Quest streak** (consecutive completion grants compounding bonuses)
14. **Class evolution** (Necromancer → Shadow Sovereign → Shadow Monarch, gated by story)

That's 14 progression layers for the Player. Other Hunters have layers 1-4 only. The asymmetry is the design.

---

## Itemization

### Currency tiers
- **Mana Stones** (E to S): primary loot drops, function as POE-style currency. E reroll single sub-stat; D reroll all subs; C upgrade rarity; B add affix; A lock affix; S mirror.
- **Essence Stones**: crafting input from named Magic Beasts.
- **Gold Essence Stones**: top-tier crafting from cosmic encounters.
- **Powder of Inheritance**: Blessing Stone fusion currency.
- **Apostle Shards**: Ragnarok-era endgame currency.

### Loot tiers (Diablo color hierarchy)
- E: White (Common)
- D: Blue (Uncommon)
- C: Yellow (Rare)
- B: Orange (Heroic)
- A: Purple (Epic)
- S: Red (Legendary)
- Cosmic / one-of-a-kind: Gold (Mythic / Story-locked)

### Weapons
- Player weapons (Jinwoo only): 80+ entries, organized by tier, each tied to a canonical source. Daggers (his primary), longswords, scythes, grimoires, fans, quarterstaves. Each weapon has a passive effect that scales with stats.
- Hunter signature weapons: each playable Hunter has one SSR signature weapon designed for their kit.
- Common Hunter weapons: shared pool of mid-tier weapons.

### Artifacts (8 slots)
4 Armor slots (Helmet, Armor, Gloves, Boots) + 4 Jewelry slots (Necklace, Bracelet, Ring, Earrings). Set bonuses at 2/4/8 pieces (combination sets exist that span armor and jewelry). Rolled main + sub stats. Enhancement system with success-rate-based upgrades and fail-bonus accumulation.

### Set bonuses (proposed core list)
- **Demon Castle Set** (2-piece +Fire damage / 4-piece +Demon-class damage / 8-piece unlock Demon Sovereign mode)
- **Frost Folk Set** (Cold-element scaling)
- **Ant Colony Set** (multi-summon damage scaling)
- **Beast King Set** (physical damage scaling)
- **Insect Queen Set** (DoT scaling)
- **Shadow Marshal Set** (Player-only, shadow army efficiency)
- **Bond Forge Set** (stats scale with bonded crew presence)
- **Counter-Architect Set** (Cipher cameo, infrastructure damage)
- **Heir of Destruction Set** (Antares-fragment scaling, Suho/Ragnarok unlock)
- **Stardust Resistance Set** (anti-brainwash, Ragnarok-era)
- **Ruler's Vessel Set** (National Level cosmic-tier)

### Rune Stones
Skill modification stones dropped from Magic Beasts. Each named Magic Beast has a unique Rune Stone with its signature ability. Common variants drop from species-tier creatures. Each skill can equip up to 3 Runes simultaneously.

### Blessing Stones (Player only)
33+ stones across Empowerment and Survival categories. Three rarities. Fusion-based acquisition. 4 equip slots. Passive effects that stack.

### Story-locked drops (canon-faithful)
- **Black Heart** (one-time, Shadow Monarch succession)
- **Cup of Reincarnation** (one-time, Rulers' faction artifact)
- **Holy Water of Life** (full Demon Castle clear required)
- **Kamish's Wrath** (post-Kamish-Raid quest unlock)
- **Antares Fragment** (Suho-arc unlock, post-game)

### Bestowal mechanic (canon)
Jinwoo can permanently transfer items to companions. Once bestowed, the item is locked to that companion and gets a personal scaling bonus on top of base stats. Examples: Demon King's Longsword to Igris (becomes Knight Killer-class scaling), Orb of Avarice to Tusk (becomes dragon-staff scaling), Kamish's Wrath kept by Jinwoo (becomes paired-dagger scaling).

---

## Dungeon system

### Gate types
- **Standard Gates** (E-S): conventional dungeon corridors and rooms, scaled by tier.
- **Field-Type Gates** (mid-late game): open-world dungeons where the entire interior is a region (forest, mountain, desert, glacier). Multiple objectives, environmental puzzles, mid-bosses.
- **Red Gates** (rare, dangerous): seal upon entry. No exit until boss is defeated. Survival mechanics (hunger, mana exhaustion, hostile environment).
- **Double Dungeons** (very rare): masquerade as a lower rank from outside, are actually higher rank inside. Set-piece narrative encounters.
- **Instant Dungeons** (Player only): System-generated dungeons unique to Jinwoo. Job change quests, Cartenon-style System Dungeons. Contains NPC characters with unique storylines.
- **System Dungeons** (Cartenon-tier): NPCs inside have agency. Some can transition to active-world allies (Esil Radiru pattern).

### Dungeon mechanics
- **Time pressure / Burst**: every Gate has a burst countdown. Failing to clear in time releases monsters into the world. Player faction reputation suffers; some quests fail.
- **Loot drops**: per-monster + boss-specific + environmental chests.
- **Environmental hazards** (Souls graft): traps, pitfalls, ambient damage zones. Item descriptions and lore notes scattered through the dungeon.
- **Bonfire / Gate-checkpoint**: rest restores HP/Stamina, respawns monsters (except bosses). Save point.
- **Elite spawns**: rare named-Magic-Beast variants that drop boss-tier loot.

### Endless Tower (Demon Castle replay)
After clearing the canon Demon Castle, an endless variant unlocks. Floors 100+, scaling difficulty, weekly reset. Each floor has random affixes (Mythic+ graft from WoW). Loot scales with floor depth.

### Greater Rifts (Diablo graft)
Generic procedurally-generated Gates. Scaling difficulty. Speed-clear leaderboards. Cosmetic and mid-tier loot. Endgame replay loop.

---

## Catch / Evolution / Shadow Army (the Pokemon spine)

Every Magic Beast is a potential shadow. The Arise mechanic is the catch.

### Catch mechanic
After defeating a Magic Beast, Jinwoo can attempt Arise. Success rate based on:
- Damage Jinwoo personally dealt (more = higher rate)
- Magic Beast tier vs Player level
- Story conditions (some bosses can only be Arisen at specific story beats)
- Class affinity (Necromancer / Shadow Sovereign tier)

### Shadow tiers
- **Soldier** (basic infantry, hundreds available, swarm tactics)
- **Knight** (elite line, ~50 max in roster)
- **General** (named units like Igris, Beru, Tusk, Iron, Bellion - up to 8 active)
- **Marshal** (Bellion, Beru post-evolution, Igris post-evolution - up to 2 active)
- **Beast / Special** (mounts, scouts, unique-role units like Tank, Kaisel - flexible)

### Evolution
Shadow evolution is event-driven, not level-driven. Igris evolves to Knight Killer after the Red Gate Arc. Beru evolves through Jeju Island → Ahjin Guild Arc training. Each evolution requires a specific quest or condition. Evolutions are dramatic stat increases plus new abilities.

### Roster management
You have an active roster (deployed in fights) and a reserve roster (stored). Active roster size scales with Player level (max ~20 deployed shadows + 8 named generals + 2 marshals + Marshall ).

### Shadow loyalty / synergy
Shadows have loyalty stats that increase with deployment. High-loyalty shadows perform better, take initiative, and can level up beyond their base cap. Bestowing items further increases loyalty.

### Shadow type chart
Type effectiveness like Pokemon. Shadow type counters Magic Beast type. Holy beats Demon. Light beats Dark. Beast beats Insect. Insect beats Demon. Demon beats Light. Building a balanced army of types is the meta-game.

---

## Nemesis system (Shadow of Mordor graft, the secret weapon)

This is the system that makes the game distinctive. Solo Leveling: ARISE doesn't have it. Canon supports it perfectly.

### Nemesis state
Every Magic Beast you don't capture or kill cleanly becomes a Nemesis. They escape, go into hiding, level up, recruit subordinates, take territory in unclaimed Gates. They remember the player.

### Nemesis behaviors
- **Level up over time**: a Nemesis you let escape grows stronger.
- **Recruit subordinates**: lower-tier Magic Beasts join their faction.
- **Take territory**: claim Gates as their domain. Future raids in those Gates feature them.
- **Form alliances**: faction politics emerge between Nemeses (Beast vs Demon, etc.).
- **Develop traits**: random scarring (e.g., "afraid of Fire" if you killed them with Fire previously, or "Berserker on low HP" if you let them escape after near-death).
- **Hunt the player back**: high-level Nemeses can ambush you during normal Gate raids.

### Itarim corruption (Ragnarok-era)
Apostles can brainwash Nemeses. A Nemesis who allies with the Itarim becomes a far more dangerous variant with new abilities (Brocky pattern). Cleansing brainwash with Holy element opens dialogue: convert to ally or kill cleanly.

### Cipher and Severin (cameos)
The cameo antagonists ARE Nemesis-class characters. They remember player interactions, level over time, plan against the protagonist. Their arcs are Nemesis arcs that span multiple game cycles.

### Why this matters
The Nemesis system creates the persistent-world feel that no Solo Leveling game has captured. It makes the world feel alive. It makes individual escaped Magic Beasts memorable. It justifies the canonical "surviving Monarch servants in hiding" plot point as gameplay.

---

## Bond system (Persona 5 graft)

### Social Links per Hunter
Each playable Hunter has 10 ranks of bond. Each rank up grants a passive ability:
- Rank 1-3: stat boosts (Attack, Defense, HP, Crit Rate)
- Rank 4-6: skill modifications (cooldown reduction, damage amplification)
- Rank 7-9: unique synergy abilities (combo finishers, paired ultimates)
- Rank 10: bond ultimate ability + cosmetic + storyline conclusion

### How bonds rank up
- **Mission completion together** (primary): bringing the Hunter on raids gradually fills bond meter.
- **Dialogue choices** (secondary): conversations between missions offer choices that fill bond meter faster when aligned with Hunter's personality.
- **Gift-giving** (tertiary): bestow items that match Hunter's preferences. Diminishing returns after first.
- **Shared activities** (life-sim layer): training together, eating, social events.

### Bond Forge mechanic (canon Jared cameo)
Bonded Hunters confer stat multipliers when deployed together. Two bonded Hunters in party: +5% damage. Three: +10%. Four (Jinwoo + 3 max-bond Hunters): +20% damage + special team passive. Models the Bond Forge Set as a baseline system, not just an artifact bonus.

### Severin counter (cameo antagonist)
Severin's Wedge mechanic interferes with Bond ranks during specific encounters. The fight is to identify what he's done before he severs the bond entirely. Bond resilience can be trained.

---

## Faction structure

### Three-tier hierarchy (canon)
- **Hunters** (humans, Player + Hunter classes)
- **Magic Beasts / Monarchs** (faction tier, Antares-led)
- **Rulers** (cosmic faction, vessel-bound to humans)

### Fourth-tier reveal (Ragnarok)
- **Itarim / Apostles**: cosmic invader faction above all the above

### Faction reputation (player-facing)
- **Korean Hunter Association**: standard guild
- **International Hunter Associations**: separate reputation per nation
- **Individual Guilds**: White Tiger, Hunters Guild, Goliath, Draw Sword, Fame, Ahjin (your guild)
- **The Rulers**: faction reputation, unlocks vessel-tier passives at high rep
- **The Itarim**: hostile by default, no positive reputation possible. But individual Apostles may be temporarily appeased.

### Faction-locked content
- High Korean rep: access to S-rank Korean raids
- High Goliath rep: alliance with Thomas Andre (post-defeat reconciliation arc)
- High Ruler rep: National Level Hunter quest unlocks (vessel-tier abilities)
- Negative Itarim rep: more frequent Apostle ambushes

---

## Ahjin Guild (your guild HQ)

### Guild as customizable hub
After founding Ahjin Guild with Yoo Jinho (canon), you have a HQ that:
- Stores shadow army not currently active
- Houses Hunter recruits (each playable Hunter you've bonded with has a room)
- Has a strategy room (raid planning interface)
- Has a forge (crafting station)
- Has a System Shop terminal (Player class only)
- Has training arenas (combat skill drills)

### Recruitment loop
Yoo Jinho manages public-facing operations. Hunters can be recruited via:
- Story progression (canon Hunters)
- Bonus quests (rare Hunters)
- Reputation milestones (faction-locked Hunters)
- Specific dungeon clears (Esil Radiru pattern: NPCs become PCs)

### Guild rank
Ahjin Guild itself has a faction rank. As you complete major quests and raids, the Guild ascends in Korean and global rankings. High Guild rank unlocks elite raids and political influence.

---

## Daily Quest System (canon + Hades graft)

### Daily Quest panel
Player-class only. Each day, the System assigns a 4-task quest:
- 100 push-ups (light combat training in-game)
- 100 sit-ups (parry drill)
- 100 squats (dodge drill)
- 10km run (movement / exploration)

### Completion rewards
- Mana Stones (scaling with consecutive completion streak)
- Stat points
- Random System Shop unlock
- Daily Quest streak bonus (compounds: 7-day streak = +1 stat point per level retroactive)

### Penalty Zone
Skip a Daily Quest = transport to Penalty Zone. Survival arena with a single magic beast scaled to your level. Defeating it grants partial Daily Quest credit. Failure = wake up in your home with a Health/Stamina debuff for 24 hours.

### Roguelike layer
Penalty Zone runs are roguelike-shaped. Random affixes on the boss. Random environmental modifiers. Random Magic Beast type. Beat it: meta-progression rewards. Lose: Health debuff but no permanent loss.

### Daily Quest as design lever
This is the engagement-loop driver. Players who complete dailies steadily compound stats. Players who skip get harder content via Penalty Zone. Either path is rewarded; skipping isn't punished, just channeled differently.

---

## Story progression (canon arcs as game arcs)

The canon arcs map directly to game chapters. Each arc has a unique mechanic introduction.

| Arc | Intro mechanic | Boss |
|-----|---------------|------|
| Pre-System | Tutorial: weak hunter combat | None |
| Double Dungeon | System awakening, Daily Quest unlocks | Statue of God |
| Reawakening | S-rank reassessment, Player-class confirmed | None |
| Job Change Quest (Cartenon) | Class evolution, Arise unlocks, Igris recruited | Kasaka, Statue of God |
| Demonic Castle | Item-as-lore descriptions, Souls-feel combat | Cerberus, Vulcan, Metus, Baran |
| Red Gate | Survival mechanic, sealed dungeon, Igris evolution | Ice Elves, Baruka |
| Hunters Guild Gate | Coalition raid mechanic, multi-S-rank coordination | Kargalgan |
| Ahjin Guild formation | Guild-management, recruitment, Yoo Jinho bond | None (faction rep arc) |
| Jeju Island | Massive coalition raid, Goto Ryuji death, Beru recruit | Ant King |
| Post-Jeju (recruit Cha Hae-In) | Bond Forge mechanic introduction | Various |
| Double Dungeon Arc (post-anime) | Nemesis system intro (Hwang Dongsoo) | Hwang Dongsoo |
| Japan Crisis | Mass shadow deployment | Various Tokyo Giants |
| International Guild Conference | Faction reputation diversification, Thomas Andre fight | Thomas Andre |
| Monarchs War | Final-act mechanic: cosmic reveal, vessel power | Multiple Monarchs |
| Final Battle | Antares boss, multi-phase, full kit unlocked | Antares |
| Epilogue | Cup of Reincarnation cinematic, time-rewind narrative beat | None |
| Ragnarok | Suho protagonist switch, Apostle introduction, new generation | Brocky, Tiel, Arsha |

### Arc-as-pacing
Each arc takes 8-15 hours of play. Total main story: 100-150 hours. Side content + endgame: 200+ hours additional.

### Suho post-game
After completing the main story, the Ragnarok arc unlocks Suho as a playable Player-class character. He starts at high level but has a different progression path (Heir of Destruction vs Shadow Sovereign). Effectively new-game-plus with a different protagonist.

---

## Endgame loops

### Greater Rifts / Procedural Gates
Diablo-style. Scaling difficulty. Cosmetic and crafting rewards. Speed-clear leaderboards.

### Endless Tower (Demon Castle replay)
Lost Ark Cube + canon Demon Castle. 100+ floors. Weekly reset. Random affixes. Tier-defining loot at floor breakpoints (every 10 floors).

### Nemesis Hunting
Track down escaped Nemeses. Each has procedural traits and rewards. Killing or capturing them affects the world state.

### Apostle Waves (Ragnarok-era seasons)
Seasonal content: a new Apostle invades. Their territory expands across the map weekly. Players cooperate (async) to push them back. Seasonal artifacts and weapons drop.

### Bond Stories
Each Hunter has a 10-rank bond storyline that pays off in late game with personalized side-quests, unique cutscenes, and a final ability that can only be earned by maxing the bond.

### Suho campaign (post-game)
Full second protagonist with Apostle-faction antagonists.

### Mythic difficulty
Story raids re-runnable on Mythic difficulty with new mechanics, cosmic affixes, and improved drops.

---

## Multiplayer / async social (light touch)

### Co-op raids (optional)
Some S-rank Gates support 4-player co-op. Each player brings their own Hunter team. Loot is per-player.

### Async Resonance markers (Death Stranding lite)
Players can leave markers in dungeons (notes, warnings, hints) visible to other players. Limited capacity per player.

### Nemesis sharing
A particularly powerful Nemesis from your world can be shared as a "rival contract" with other players. They face it in their world. Bounty rewards on completion.

### Guild halls (cosmetic)
Friends can visit your Ahjin Guild HQ to see your shadow army roster, your trophies, your Hunter relationships.

### What we explicitly skip
- PvP arenas (off-tone)
- Open-world server (single-player core; async only)
- Trading / auction houses (would create gacha-tier monetization pressure)

---

## Monetization (premium model recommendation)

### Core game: premium ($60-70 standard)
Full main story, all canon Hunters, all crafting, all systems. No paywall in the gameplay loop.

### Optional cosmetics
Outfits, weapon skins, shadow army color palettes, Ahjin Guild decoration. Pure cosmetic, no power impact.

### Expansion model
Major content (Ragnarok, post-canon Suho campaign) shipped as expansions ($30 each). Players who buy stay engaged for years.

### What we explicitly skip
- Gacha pulls (ARISE pattern, off-vibe)
- Pay-to-win artifact rolls
- Loot boxes
- Energy systems (no daily-cap on play)
- Battle passes (no manufactured FOMO)

### Why
The Solo Leveling story is a power fantasy about earning your strength. Selling shortcuts undercuts the thesis.

---

## Visual / audio direction

### Art style
3D action-RPG. Stylized but not cartoony. Reference: Lost Ark's art direction with Solo Leveling's manhwa-derived character designs. Magic Beasts faithful to canon visuals. Shadow soldiers visually distinct (purple aura, ethereal edges).

### Camera
Third-person, over-shoulder. Combat zoom-out for situational awareness. Cinematic camera for boss intro / phase shifts.

### Performance / scope
Target current-gen consoles + PC. Mobile not core (avoid ARISE comparison). Optional cloud-streaming for mobile flex.

### Music
Solo Leveling anime OST as inspiration. Hideyuki Fukasawa-style orchestration. Korean instrumentation as flavor (gayageum on bond moments, taepyeongso on Korean raids). Heavy electronic undercurrent on Apostle/Itarim content (cosmic-tier feels alien).

### Voice acting
Korean voice cast as primary (matches anime), English dub localization. Each canonical character voiced by anime voice actors when possible.

---

## What this game is NOT

- Not a gacha. No pulls, no banners, no FOMO.
- Not an MMO. Single-player core with optional async multiplayer.
- Not Genshin in costume. ARISE already did that. We are doing the next thing.
- Not turn-based. Action-tier combat is non-negotiable for this IP.
- Not pay-to-win. Premium upfront cost, optional cosmetics. Earned power, not bought power.
- Not generic. Every system is asymmetric protagonist + canon-faithful.
- Not derivative. Borrows mechanics, but the COMBINATION is original. No game has stacked Pokemon + Monster Hunter + Souls + Persona + Shadow of Mordor + Diablo + Lost Ark on one IP and done it well.

---

## What this game IS

- Solo Leveling's lore translated into the game it always implied.
- Asymmetric protagonist as the foundational design choice.
- Action ARPG core with Souls combat feel + Monster Hunter hunt structure.
- Pokemon-style catch + party + evolution layered on canon Arise.
- Diablo-tier itemization with POE-tier currency-as-crafting.
- Persona 5 social bond depth + canon Bond Forge system.
- Shadow of Mordor Nemesis system as the secret weapon for persistent-world feel.
- ARISE's progression layer architecture (artifacts + runes + blessing stones), refined.
- Lost Ark's combat mod depth (tripod) + Korean MMO tonal alignment.
- Story-faithful to canon's emotional weight (item-as-relationship, story-locked drops, generational succession).
- Single-player core with async social texture.
- Premium monetization with cosmetic expansion model.

---

## Bottom line

Most game concepts graft cleanly because Solo Leveling's lore was structured around RPG concepts from the start. The work is not invention; it is selection and alignment. This document selects the highest-impact, lore-faithful grafts and aligns them around the singular thesis: asymmetric protagonist. Every system reinforces that thesis. Every mechanic is justified by canon hooks. Nothing is included because it's trendy; nothing is excluded because it's hard.

The game that ships from this design contract is the one Solo Leveling fans always wanted. ARISE is the gacha version. This is the actual game. Build it once, build it right, ship it premium. Earn the universe.

The marginal cost of completeness is near zero with AI-assisted development. Boil the ocean. Ship the whole thing.

This is the design. Build when you're ready.
