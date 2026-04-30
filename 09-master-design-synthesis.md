# Master Design Synthesis

The unified design contract for the game. Every system from canon connected, every mechanic justified by the world, every judgment call made. Not code. Not a plan. The design.

This document supersedes individual recommendation files. Where they differ, this document is final.

---

## Vision (one paragraph)

You are not the strongest Hunter. You are the only Hunter who can become anything. The world has Gates, ranks, raids, and a strict hierarchy that says your power is fixed at awakening. The System on your screen is the System everyone whispers about, the one that broke Sung Jinwoo. It is broken for you too. The game is the loop of becoming: each Gate cleared rewrites your potential, each Magic Beast defeated joins your shadow army, each bonded ally rewrites the math of every fight. You start as the world's weakest. You end as the universe's apex. The space between is the game.

---

## The single thesis: asymmetric protagonist

Every Hunter in the world has a fixed ceiling. Their rank is locked at awakening and never changes. They get gear, they get experience, they get better at using what they were born with. None of them level up.

You are the exception. You are the Player.

You have the System. You have Daily Quests. You have a Penalty Zone. You have stat allocation. You have an inventory. You have a Shop. You have Arise. You have a Shadow Army. You have Bestowal. You have Blessing Stones. You have a passive tree. You have access to Instant Dungeons. You have class evolution paths.

Other Hunters do not have any of this. They have stats, gear, and skills. That is all.

This asymmetry is not a balance problem. It is the design. Every mechanic in this contract is built around the gap between Player and Hunter. The protagonist is a different type of being from the rest of the cast, and the game proves it through systems, not just dialogue.

---

## Core gameplay loop (moment-to-moment)

You stand at a Gate. You enter. Inside is a dungeon: monster zones, environmental hazards, a boss room. You bring your party (three Hunters plus your shadow army). You fight with stamina-based combat: light attacks, heavy attacks, dodge, parry, block. Stamina regenerates between strikes; running out leaves you vulnerable. You break boss body parts to trigger phase shifts. You swap between your three Hunters mid-fight, leaving residual buffs as you tag. You command your shadows through the System UI. You kill the boss. You attempt Arise to extract its shadow into your army. You loot. You exit. You are stronger.

You go to the next Gate. The loop is satisfying at hour zero because the combat itself has weight. The loop scales because every kill compounds: shadows grow, stats grow, items grow, bonds grow, the world remembers you, the System rewards consistency, and surviving Magic Beasts go into hiding to plan against you.

---

## Combat system

### Stance and rhythm
Stamina-based action combat. Every attack costs stamina. Every dodge costs stamina. Stamina regenerates between strikes. Out-of-stamina = vulnerable. No infinite combos. Spacing and timing matter.

### Skills per Hunter
Each Hunter has a basic attack, two skills, and an ultimate, plus a passive ability. Skills have cooldowns and consume MP. Ultimates require building a meter through combat.

### Tag-swap
You bring three Hunters plus Jinwoo on most missions. You play one at a time. Tag-swap is fluid and instant. The character swapping out leaves a residual aura on the field for several seconds (damage boost, healing zone, stagger build, depending on Hunter). Tag-swap synergy is a core combat depth lever.

### Element reactions
Solo Leveling's elements: Fire, Ice, Lightning, Light, Dark, Beast, Insect, Demon, Holy. When two elements interact on a target, reactions trigger:

- Fire on Ice: Melt (massive single-target)
- Lightning on Water/Ice: Electrocute (DoT)
- Dark on Light or Light on Dark: Annihilation (raw damage)
- Holy on Demon: Cleanse (purifies brainwashing, removes Stardust)
- Beast on Insect: Ravage (party damage)
- Light on Beast: Hunt (mobility burst)

Building party comps that trigger reactions is where teamplay shines.

### Shadow Army deployment
Jinwoo has a separate input for shadow command. Shadows are summoned and dismissed via the System UI. They fight autonomously under directive (assault, hold, defend, withdraw). Up to twenty shadows on the field at once depending on Player level. Shadows can level independently through combat experience.

### Body-part breaks
Magic Beasts have three to six breakable parts: head, claws, wings, tail, armor plate, body segments. Breaking parts:
- Triggers phase shifts in the encounter
- Drops body-part-specific crafting materials
- Disables specific attacks (break Antares' wings, no Dive Phase)

### Boss fight structure
Multi-phase encounters. Phase shifts triggered by HP thresholds, body-part breaks, or environmental conditions. Each phase introduces new mechanics. Solo encounters for Daily Quest scope; four-Hunter raids for standard A-rank Gates; eight-to-twenty-five Hunter coalitions for S-rank story raids.

### Stagger / Break gauge
Every enemy has a Break gauge alongside HP. Filling Break triggers a stagger window where the enemy is vulnerable to amplified damage and execution finishers (the moment Beru dismembers an opponent in canon). Specific weapons and skills have Break-affinity. Specific party comps optimize for Break.

---

## Progression layers

The Player has fourteen progression layers stacked. Other Hunters have only the first four.

1. **Character level** (1-100)
2. **Stat allocation** (5 free points per level, Player only)
3. **Equipment** (weapons + 8 artifact slots)
4. **Skills** (4 active + passive per character)
5. **Tripod skill enhancement** (each skill has 3 selectable enhancement nodes; choose 2)
6. **Rune Stones** (skill modification stones dropped from Magic Beasts; up to 3 per skill)
7. **Blessing Stones** (Player only, 4 slots, fusion-based)
8. **Passive tree** (Player only, ~200 nodes branching across Stealth, Combat, Necromancy, Authority)
9. **Bond ranks** (10 ranks per Hunter, granting shared abilities)
10. **Shadow army roster** (catch, evolve, deploy, level up)
11. **Faction reputation** (per Association, per Guild, per Ruler)
12. **System Shop tier** (unlocks expand as Jinwoo levels)
13. **Daily Quest streak** (consecutive completion compounds bonuses)
14. **Class evolution** (Necromancer to Shadow Sovereign to Shadow Monarch, story-gated)

The asymmetry is the design. Lean in.

---

## Itemization

### Currency tiers

- **Mana Stones** (E to S rank): primary loot, function as crafting currency.
  - E reroll one sub-stat
  - D reroll all sub-stats
  - C upgrade rarity
  - B add affix
  - A lock affix while rerolling others
  - S mirror item (duplicate)
- **Essence Stones**: crafting input from named Magic Beasts.
- **Gold Essence Stones**: top-tier crafting from cosmic-tier encounters.
- **Powder of Inheritance**: Blessing Stone fusion currency.
- **Apostle Shards**: Ragnarok-era cosmic currency.

### Loot rarity tiers
- E rank: Common
- D rank: Uncommon
- C rank: Rare
- B rank: Heroic
- A rank: Epic
- S rank: Legendary
- Cosmic / one-of-a-kind: Mythic / Story-locked

### Weapons

- **Player weapons**: 80-plus entries spanning daggers, longswords, scythes, grimoires, fans, quarterstaves. Each tied to a canonical source. Each has a passive effect that scales with Player stats. Examples include the Demon King's Longsword, the Demon King's Daggers, Kamish's Wrath, Vulcan's Rage, Phoenix Soul, Thetis' Grimoire, Moonshadow, Stormbringer, Winter Fang, Skadi, the Orb of Avarice, Knight Killer, Kasaka's Venom Fang.
- **Hunter signature weapons**: each playable Hunter has one top-tier weapon designed for their kit. Cha Hae-In's Sword of Light. Baek Yoonho's Howling White Tiger's Soul. Choi Jong-In's Equivalent Exchange. Goto Ryuji's Distorted Dreams.
- **Common Hunter weapons**: shared pool for non-signature loadouts.

### Artifacts (8 slots)
Four Armor slots (Helmet, Armor, Gloves, Boots) plus four Jewelry slots (Necklace, Bracelet, Ring, Earrings). Set bonuses at two pieces, four pieces, and eight pieces (combination sets that span armor and jewelry). Main stats fixed per slot type, sub-stats randomized at drop.

Set bonus families:
- **Demon Castle Set** (2-piece Fire damage, 4-piece Demon-class damage, 8-piece unlocks Demon Sovereign aspect)
- **Frost Folk Set** (Cold-element scaling)
- **Ant Colony Set** (multi-summon scaling)
- **Beast King Set** (physical damage scaling)
- **Insect Queen Set** (DoT scaling)
- **Shadow Marshal Set** (Player only, shadow army efficiency)
- **Bond Forge Set** (stats scale with bonded crew presence)
- **Counter-Architect Set** (anti-infrastructure damage)
- **Heir of Destruction Set** (Antares-fragment scaling, Suho-arc unlock)
- **Stardust Resistance Set** (anti-brainwash, Ragnarok-era)
- **Ruler's Vessel Set** (cosmic-tier, faction-locked)

### Artifact enhancement
Spend Gold and Enhancement Chips to upgrade. Success rate based: 100% on first attempt, decreases each tier. Failed attempts cost resources but add a 1% bonus to the next attempt. Hidden tier bonuses unlock at Tier 5, 10, 15. Maximum tier 20.

### Rune Stones
Skill modification stones dropped from Magic Beasts. Each named Magic Beast has a unique Rune Stone with its signature ability. Common variants drop from species-tier creatures. Each skill can equip up to 3 Runes simultaneously.

Notable canon Rune Stones:
- **Kamish's Rune Stone**: Dragon's Fear (mana-infused soul shout, drops weaker beings into despair)
- **Igris's Rune Stone**: Ruler's Hands / Dominator's Touch (telekinesis, lesser version of Ruler's Authority)
- **Baran's Rune Stone**: Shadow Exchange (instant teleport-swap with one of the user's shadows)
- **Kang Taeshik's Rune Stone**: Stealth (full physical and magical invisibility)

### Blessing Stones (Player only)
Thirty-three plus stones across two categories: Empowerment (offensive) and Survival (defensive). Three rarities (Rare, Heroic, Legendary). Acquired via Fusion: 50 Powder of Blessing fuses one random Stone, with a 2% Super Success rate for Heroic. Fusing 3 duplicates upgrades to higher rarity. Four equip slots, unlocking at story milestones.

### Story-locked drops
Items obtainable only at specific story beats:
- **Black Heart** (one-time, Shadow Monarch succession from Ashborn)
- **Cup of Reincarnation** (one-time, Rulers' faction artifact, narrative beat only)
- **Holy Water of Life** (full Demon Castle clear required, ingredients gathered across all 100 floors)
- **Kamish's Wrath** (post-Kamish-Raid quest unlock)
- **Antares Fragment** (Suho-arc unlock, post-game)

### Bestowal mechanic
The Player can permanently transfer items to companions. Once bestowed, the item is locked to that companion and gains a personal scaling bonus on top of base stats. Examples: the Demon King's Longsword to Igris (Knight Killer scaling), the Orb of Avarice to Tusk (mage-amplification scaling), Kamish's Wrath kept by Jinwoo (paired-dagger scaling).

Bestowal is canon. It is also the deepest item-progression mechanic in the design because the gift cements the bond and the item gains permanence in the relationship.

---

## Dungeon system

### Gate types
- **Standard Gates** (E to S): conventional dungeon corridors and rooms, scaled by tier.
- **Field-Type Gates**: open-region dungeons containing entire landscapes (forest, mountain, desert, glacier). Multiple objectives, environmental puzzles, mid-bosses. The Paju Field Dungeon is a Ragnarok-era example.
- **Red Gates**: seal upon entry. No exit until boss defeated. Survival mechanics activate (hunger, mana exhaustion, hostile environment).
- **Double Dungeons**: appear as a lower rank from outside, are actually higher rank inside. Set-piece narrative encounters.
- **Instant Dungeons** (Player only): System-generated dungeons unique to Jinwoo. Job change quests, Cartenon-style System Dungeons.
- **System Dungeons** (Cartenon-tier): NPCs inside have agency. Some can transition to active-world allies (Esil Radiru pattern).

### Dungeon mechanics
- **Time pressure / Burst**: every Gate has a burst countdown. Failure releases monsters into the world. Hunter Association reputation suffers; some quests fail permanently.
- **Loot drops**: per-monster, per-boss, environmental chests, hidden rooms.
- **Environmental hazards**: traps, pitfalls, ambient damage zones. Item descriptions and lore notes scattered through the dungeon.
- **Gate-checkpoint**: rest restores HP and Stamina, respawns regular enemies (bosses do not respawn).
- **Elite spawns**: rare named-Magic-Beast variants with boss-tier loot.

### Endless Demon Castle
After clearing the canon Demon Castle, an endless variant unlocks. Floors 100 and beyond. Scaling difficulty, weekly reset. Each floor has random affixes (modifiers like Frost Aura, Berserk, Sanguine, Mana Drought). Tier-defining loot at floor breakpoints (every ten floors).

### Procedural Gates
Generic procedurally-generated Gates for endgame replay. Scaling difficulty. Speed-clear leaderboards. Cosmetic and mid-tier loot.

---

## Catch / Evolution / Shadow Army

### Catch mechanic (Arise)
After defeating a Magic Beast, Jinwoo can attempt Arise. Success rate based on:
- Personal damage dealt (more = higher rate)
- Magic Beast tier vs Player level
- Story conditions (some bosses can only be Arisen at specific story beats)
- Class affinity (Necromancer to Shadow Sovereign to Shadow Monarch tier)

### Shadow tiers
- **Soldier**: basic infantry, hundreds available, swarm tactics
- **Knight**: elite line, ~50 max in roster
- **General**: named units (Igris, Beru, Tusk, Iron, Bellion). Up to 8 active.
- **Marshal**: Bellion, Beru post-evolution, Igris post-evolution. Up to 2 active.
- **Beast / Special**: mounts, scouts, unique-role units (Tank, Kaisel). Flexible.

### Evolution
Shadow evolution is event-driven, not level-driven. Igris evolves to Knight Killer after the Red Gate Arc. Beru evolves through Jeju Island and Ahjin Guild Arc training. Each evolution requires a specific quest or condition. Evolutions are dramatic stat increases plus new abilities.

### Roster management
You have an active roster (deployed in fights) and a reserve roster (stored). Active roster size scales with Player level. Maximum roughly 20 deployed shadows + 8 named generals + 2 marshals when fully unlocked.

### Shadow loyalty
Shadows have loyalty stats that increase with deployment. High-loyalty shadows perform better, take initiative, and can level up beyond their base cap. Bestowing items further increases loyalty.

### Shadow type chart
Type effectiveness across the canon element grid. Building a balanced army across types is the meta-game.

---

## Surviving Magic Beasts (the persistent-world layer)

This is what makes the world feel alive and what no existing Solo Leveling adaptation has built. Canon supports it perfectly: after the Monarchs War, surviving Magic Beast servants went into hiding to plan re-invasion. Brocky and Arsha are exactly this trope made plot-explicit.

### Survivor state
Every Magic Beast you defeat but do not capture or kill cleanly becomes a Survivor. They escape the dungeon, go into hiding, level up, recruit subordinates, take territory in unclaimed Gates. They remember the player.

### Survivor behaviors
- **Level up over time**: a Survivor you let escape grows stronger.
- **Recruit subordinates**: lower-tier Magic Beasts join their faction.
- **Take territory**: claim Gates as their domain. Future raids in those Gates feature them.
- **Form alliances**: faction politics emerge between Survivors (Beast vs Demon, etc.).
- **Develop traits**: random adaptations form based on prior encounters (e.g., resistance to the element you killed them with previously, or Berserker behavior on low HP if you let them escape after near-death).
- **Hunt the player**: high-level Survivors can ambush you during normal Gate raids.

### Itarim corruption (Ragnarok-era)
Apostles can brainwash Survivors. A brainwashed Survivor allied with the Itarim becomes a far more dangerous variant with new abilities (Brocky pattern). Cleansing brainwash with Holy element opens dialogue: convert to ally or kill cleanly.

### Cipher and Severin (cameo antagonists)
The cameo antagonists are themselves Survivor-class characters with persistent memory. They remember player interactions, level over time, plan against the protagonist. Their arcs span multiple game cycles.

### Why this matters
The Survivor system creates persistent-world feel. It makes individual escaped Magic Beasts memorable. It justifies the canonical "surviving Monarch servants in hiding" plot point as actual gameplay. It is the system that distinguishes this game from every other Solo Leveling adaptation.

---

## Bond system

### Social ranks per Hunter
Each playable Hunter has 10 ranks of bond. Each rank up grants a passive ability:
- Ranks 1-3: stat boosts (Attack, Defense, HP, Crit Rate)
- Ranks 4-6: skill modifications (cooldown reduction, damage amplification)
- Ranks 7-9: unique synergy abilities (combo finishers, paired ultimates)
- Rank 10: bond ultimate ability + cosmetic + storyline conclusion

### How bonds rank up
- **Mission completion together** (primary): bringing the Hunter on raids gradually fills bond meter.
- **Dialogue choices** (secondary): conversations between missions offer choices that fill bond meter faster when aligned with the Hunter's personality.
- **Gift-giving** (tertiary): bestow items that match Hunter's preferences. Diminishing returns after first.
- **Shared activities**: training together, eating, social events.

### Bond Forge mechanic (canon)
Bonded Hunters confer stat multipliers when deployed together. Two bonded Hunters in party: +5% damage. Three: +10%. Four (Jinwoo plus 3 max-bond Hunters): +20% damage and a special team passive. The Bond Forge Set is an artifact-tier amplifier of this baseline system.

### Severin counter (cameo antagonist)
Severin's Wedge mechanic interferes with Bond ranks during specific encounters. The fight is to identify what he has done before he severs the bond entirely. Bond resilience can be trained.

---

## Faction structure

### Three-tier hierarchy (canon)
- **Hunters** (humans, Player + Hunter classes)
- **Magic Beasts and Monarchs** (faction tier, Antares-led)
- **Rulers** (cosmic faction, vessel-bound to humans)

### Fourth-tier reveal (Ragnarok)
- **The Itarim and Apostles**: cosmic invader faction above all the above

### Faction reputation
- **Korean Hunter Association**: standard guild
- **International Hunter Associations**: separate reputation per nation
- **Individual Guilds**: White Tiger, Hunters Guild, Goliath, Draw Sword, Fame, Ahjin (your guild)
- **The Rulers**: faction reputation, unlocks vessel-tier passives at high rep
- **The Itarim**: hostile by default, no positive reputation possible, but individual Apostles may be temporarily appeased

### Faction-locked content
- High Korean rep: access to S-rank Korean raids
- High Goliath rep: alliance with Thomas Andre after the post-defeat reconciliation arc
- High Ruler rep: National Level Hunter quest unlocks (vessel-tier abilities)
- Negative Itarim rep: more frequent Apostle ambushes

---

## Ahjin Guild HQ

### Guild as customizable hub
After founding Ahjin Guild with Yoo Jinho (canon), you have a HQ that:
- Stores shadow army not currently active
- Houses Hunter recruits (each playable Hunter you have bonded with has a room)
- Has a strategy room (raid planning interface)
- Has a forge (crafting station)
- Has a System Shop terminal (Player only)
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

## Daily Quest System

### Daily Quest panel
Player only. Each day, the System assigns a four-task quest:
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
Skip a Daily Quest = transport to Penalty Zone. Survival arena with a single Magic Beast scaled to your level. Defeating it grants partial Daily Quest credit. Failure = wake up in your home with a Health/Stamina debuff for 24 hours.

### Penalty Zone as roguelike side-loop
Penalty Zone runs are run-based. Random affixes on the boss. Random environmental modifiers. Random Magic Beast type. Beat it and meta-progression rewards persist. Lose and only the Health debuff applies; no permanent loss.

### Daily Quest as design lever
This is the engagement-loop driver. Players who complete dailies steadily compound stats. Players who skip get harder content via Penalty Zone. Either path is rewarded; skipping is not punished, just channeled differently.

---

## Story progression (canon arcs as game arcs)

The canon arcs map directly to game chapters. Each arc introduces a distinct mechanic.

| Arc | Intro mechanic | Key boss |
|-----|---------------|----------|
| Pre-System | Tutorial: weak hunter combat | None |
| Double Dungeon | System awakening, Daily Quest unlocks | Statue of God |
| Reawakening | S-rank reassessment, Player class confirmed | None |
| Job Change Quest (Cartenon) | Class evolution, Arise unlocks, Igris recruited | Kasaka, Statue of God |
| Demonic Castle | Item-as-lore descriptions, weighted combat | Cerberus, Vulcan, Metus, Baran |
| Red Gate | Survival mechanic, sealed dungeon, Igris evolution | Ice Elves, Baruka |
| Hunters Guild Gate | Coalition raid mechanic, multi-S-rank coordination | Kargalgan |
| Ahjin Guild formation | Guild management, recruitment, Yoo Jinho bond | None (faction rep arc) |
| Jeju Island | Massive coalition raid, Goto Ryuji death, Beru recruited | Ant King |
| Post-Jeju recruitment | Bond Forge mechanic introduction, Cha Hae-In | Various |
| Double Dungeon Arc (post-anime) | Survivor system intro (Hwang Dongsoo) | Hwang Dongsoo |
| Japan Crisis | Mass shadow deployment | Various Tokyo Giants |
| International Guild Conference | Faction reputation diversification, Thomas Andre fight | Thomas Andre |
| Monarchs War | Final-act mechanic: cosmic reveal, vessel power | Multiple Monarchs |
| Final Battle | Antares boss, multi-phase, full kit unlocked | Antares |
| Epilogue | Cup of Reincarnation cinematic, time-rewind narrative beat | None |
| Ragnarok | Suho protagonist switch, Apostle introduction, new generation | Brocky, Tiel, Arsha |

### Pacing
Each arc takes 8-15 hours of play. Total main story: 100-150 hours. Side content + endgame: 200+ hours additional.

### Suho post-game
After completing the main story, the Ragnarok arc unlocks Suho as a playable Player-class character. He starts at high level but has a different progression path (Heir of Destruction vs Shadow Sovereign). Effectively new-game-plus with a different protagonist.

---

## Endgame loops

### Procedural Gates
Scaling-difficulty repeatable Gates with random affixes. Cosmetic and crafting rewards. Speed-clear leaderboards.

### Endless Demon Castle
The canon Demon Castle replay extension. Floors 100-plus, scaling difficulty, weekly reset, random affixes. Tier-defining loot at floor breakpoints.

### Survivor Hunting
Track down escaped Survivors. Each has procedural traits and rewards. Killing or capturing them affects the world state.

### Apostle Waves (Ragnarok-era seasons)
Seasonal content: a new Apostle invades. Their territory expands across the map weekly. Players cooperate (async) to push them back. Seasonal artifacts and weapons drop.

### Bond Stories
Each Hunter has a 10-rank bond storyline that pays off in late game with personalized side-quests, unique cutscenes, and a final ability that can only be earned by maxing the bond.

### Suho campaign (post-game)
Full second protagonist with Apostle-faction antagonists. New world state, returning characters, new Magic Beasts.

### Mythic difficulty
Story raids re-runnable on Mythic difficulty with new mechanics, cosmic affixes, and improved drops.

---

## Multiplayer / async social (light touch)

### Co-op raids (optional)
Some S-rank Gates support 4-player co-op. Each player brings their own Hunter team. Loot per-player.

### Async Resonance markers
Players can leave markers in dungeons (notes, warnings, hints) visible to other players. Limited capacity per player. Mimics canon's hunter-association field reports.

### Survivor sharing
A particularly powerful Survivor from your world can be shared as a "rival contract" with other players. They face it in their world. Bounty rewards on completion.

### Guild halls (cosmetic)
Friends can visit your Ahjin Guild HQ to see your shadow army roster, your trophies, your Hunter relationships.

### What we explicitly skip
- PvP arenas (off-tone)
- Open-world server (single-player core; async only)
- Trading / auction houses (would create inflation pressure and undermine itemization)

---

## Monetization

### Core game: premium
Full main story, all canon Hunters, all crafting, all systems. No paywall in the gameplay loop.

### Optional cosmetics
Outfits, weapon skins, shadow army color palettes, Ahjin Guild decoration. Pure cosmetic, no power impact.

### Expansion model
Major content (Ragnarok, post-canon Suho campaign) shipped as expansions. Players who buy stay engaged for years.

### What we explicitly skip
- Gacha pulls
- Pay-to-win artifact rolls
- Loot boxes
- Energy systems (no daily-cap on play)
- Battle passes (no manufactured FOMO)

### Why
The Solo Leveling story is a power fantasy about earning your strength. Selling shortcuts undercuts the thesis.

---

## Visual / audio direction

### Art style
3D action-RPG. Stylized but not cartoony. Character designs faithful to the manhwa. Magic Beasts faithful to canon visuals. Shadow soldiers visually distinct (purple aura, ethereal edges).

### Camera
Third-person, over-shoulder. Combat zoom-out for situational awareness. Cinematic camera for boss intros and phase shifts.

### Performance / scope
Target current-gen consoles plus PC.

### Music
Orchestral score with Korean instrumentation as flavor (gayageum on bond moments, taepyeongso on Korean raids). Heavy electronic undercurrent on Apostle and Itarim content (cosmic-tier feels alien). Anime-OST inspiration for the action sequences.

### Voice acting
Korean voice cast as primary (matches the anime), English dub localization. Anime voice actors when available.

---

## What this game is

- The Solo Leveling lore translated into the game it has always implied.
- Asymmetric protagonist as the foundational design choice.
- Stamina-based action combat with multi-phase boss design and body-part-break mechanics.
- Catch and evolve and party-build via canon's Arise mechanic.
- Tier-stratified itemization with currency-as-crafting depth.
- Eight-slot artifact gear with set bonuses.
- Bond depth with 10-rank social progression per Hunter.
- Persistent-world Survivor system as the secret weapon for world-feel.
- Story-faithful drops with emotional weight (item-as-relationship, story-locked artifacts, generational succession).
- Single-player core with light async social texture.
- Premium monetization with cosmetic-only optional purchases.

---

## What this game is not

- Not gacha. No pulls, no banners, no FOMO.
- Not an MMO. Single-player core.
- Not pay-to-win. Earned power, not bought power.
- Not turn-based. Action combat is non-negotiable for this IP.
- Not derivative. Every system is justified by canon hooks.
- Not generic. Every system is asymmetric protagonist plus canon-faithful.

---

## Bottom line

The work is not invention; it is selection and alignment. This document selects the highest-impact, lore-faithful systems and aligns them around the singular thesis: asymmetric protagonist. Every system reinforces that thesis. Every mechanic is justified by canon hooks.

This is the design. Build when ready.
