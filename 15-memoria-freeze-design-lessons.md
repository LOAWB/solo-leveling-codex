# Memoria Freeze Design Lessons

Synthesis of the proven patterns from Memoria Freeze, drawn from publicly documented community wikis, beginner guides, and player retrospectives. Six years of running and $150M revenue prove these structural choices work; the doc translates the patterns into design recipes we can implement and improve upon for our Solo Leveling project.

Sources for this doc:
- Memoria Freeze Fandom Wiki (player-curated, public)
- DanMemo Wiki on miraheze (public)
- Community beginner guides (publicly hosted)
- Press coverage and dev interviews
- Anime News Network feature articles

No proprietary or datamined data is used. All patterns abstracted from public structural documentation. Names of specific characters, abilities, and story content not reproduced.

---

## 1. Combat system patterns

### Stat structure
Memoria Freeze used a 5-stat character model:
- **Strength**: physical damage scaling and Penetration rate
- **Endurance**: HP and physical defense, Guard rate
- **Dexterity**: critical rate, Penetration rate, Counter rate
- **Agility**: action speed (turn order), critical rate, Guard rate, Counter rate
- **Magic**: magical damage scaling and MP regeneration

Damage types: Physical (scales with STR) vs Magic (scales with MAG). Different enemies are stronger or weaker against each type.

**Recipe for our game:** Use a similar 5-stat structure, mapped to Solo Leveling canon:
- Strength → Strength
- Endurance → Vitality (canon term)
- Dexterity → Perception (canon term, fits hunter aesthetic)
- Agility → Agility
- Magic → Mana / Intelligence

This keeps the dual-damage type and the multi-stat-affects-multi-mechanic interplay that gives the format depth.

### Action order
Action order is determined by:
1. Skill type priority (buffs first, then physical attacks, then magic attacks)
2. AGI stat (higher AGI acts first within priority tier)
3. Slight random variation (breaks ties)

**Recipe for our game:** Same priority structure. Add Solo-Leveling-flavor: shadow-army turns happen after Player turns, before enemy turns, expanding combat tempo and giving the Player class an asymmetric advantage.

### Combat depth mechanics

**Critical strike**: typically 1.5x damage, scales with DEX and AGI.

**Penetration**: damage ignores 50% of opponent's defense, scales with DEX and STR. Cannot be guarded.

**Guard**: reduces incoming damage by 50%, scales with AGI and END.

**Counter**: counter-attack triggered after taking a hit, scales with DEX and AGI.

**Recipe for our game:** Same four mechanics. They give combat texture without overwhelming complexity. Add a Break/Stagger gauge as our depth-add on top of MF's foundation.

### Element system
Memoria Freeze has 8 elements: Fire, Water, Wind, Earth, Ice, Thunder, Light, Dark. Damage scales with elemental advantage.

**Recipe for our game:** 9 elements aligned with Solo Leveling lore: Fire, Ice, Lightning (canon-faithful), Light, Dark, Beast, Insect, Demon, Holy. Already locked in synthesis 09. Plus add element-reaction combos (Fire+Ice = Melt, Holy+Demon = Cleanse) which Memoria Freeze did NOT have - this is one of our depth-additions over the genre standard.

### Skill tier system
Memoria Freeze has skills at Lo / Mid / Hi tiers, plus Special Arts (ultimates).

**Recipe for our game:** Three skill tiers per character: Basic Skill (low-cost frequent use), Major Skill (mid-cost cooldown), Ultimate (Special Arts equivalent, charged via Burst meter). Combo bonus when multiple Ultimates trigger same turn (MF pattern, replicable).

### Status effects
Memoria Freeze uses Ailments (Poison, Paralyze, Sleep, Stun, etc.) with Resistance stat. Each ailment has resistance percentages on units. Curse-tier severe debuffs.

**Recipe for our game:** Same architecture. Add canon-flavored ailments: Stardust Brainwash (Ragnarok-era), Frost (Baruka-aligned), Dragon Fear (Antares-aligned), Soul Burn (Demon-Castle-themed). Resistance stat preserved.

---

## 2. Progression patterns

### Limit Break via duplicates
Memoria Freeze's signature progression mechanic: pulling the same character multiple times grants Limit Break ranks. Each rank extends max level by 4. Without dupes: cap at level 60. With max Limit Break (5 dupes): cap at level 80. One LB-completed character is more valuable than three non-LB characters.

**Recipe for our game:** Same pattern, branded as Awakening. Awakening rank 0 (no dupes) caps at level 60. Awakening rank 5 (max) caps at level 80. Quality over quantity emphasis preserved. Match exactly because it's a proven engagement-loop driver.

### Joker / wildcard bonds
Memoria Freeze offered "Prism Bonds" and "Star Bonds" as wildcard limit-break currency. Players earned roughly 1 per month F2P, more for paying. Lets players gradually limit-break characters they'll never re-pull.

**Recipe for our game:** Wildcard currency at similar acquisition pace. Solves the rare-character-acquisition pain without trivializing the gacha pull mechanic.

### Status Board (skill tree)
Memoria Freeze uses a Status Board with 30+ unlockable nodes per character. Stats and skills come from the board, not flat from level. Falna items unlock board nodes; harder to acquire = harder Falna. Specific board layouts differ per character.

**Recipe for our game:** Same architecture. Status Board per character with ~25-30 nodes. Stat nodes, skill-unlock nodes, passive-ability nodes. Falna-equivalent currency dropped from dungeons. This adds 50-100 hours of progression depth per character.

### Adventurer + Assist split
Memoria Freeze separates units into Adventurers (active fighters in 4-character party) and Assists (equipment-style passive support). Each Adventurer pairs with one Assist; the Assist's stats add to the Adventurer's, plus an Assist Skill triggers at battle start.

**Recipe for our game:** Same split, renamed for canon. Hunters (Adventurers) and Memorias / Soul Echoes (Assists, our flavor name). Each Hunter pairs with one Soul Echo. Soul Echoes are gachable separately. This effectively doubles the gacha-pull surface area without doubling production cost (Soul Echoes are stat-stick equipment, not full character files).

---

## 3. Gacha patterns

### Rate structure
Memoria Freeze rates:
- 4-star Adventurer: 1%
- 4-star Assist: 2%
- 2/3-star fillers: 97%

**Recipe for our game:** Slightly adjusted for our tier nomenclature:
- SSR Hunter: 2-3% (slightly more generous than MF's 1% to feel modern)
- SSR Soul Echo: 2-3%
- SR / R: ~94-95% combined
- Hidden tier (Jared, Justin): 0.5% on Limited Banner only
- This is comparable to current gacha-genre standards (Genshin = 0.6% featured 5-star, Honkai = 0.6%, MF = 1% featured 4-star)

### Banner types
Memoria Freeze ran several banner formats:

**Step-up (1/4/7/10 guarantees):** every 11-pull guaranteed 4-stars on specific pulls (1st, 4th, 7th, 10th). Best for new players because of guaranteed acquisitions from a limited featured pool.

**Character Pickup:** slight rate increase for one featured 4-star, guaranteed pull at 5th multi. Includes ALL released 4-stars, just slight bias to featured.

**Paid banner:** spent paid currency only, 100% chance of a specific limited 4-star.

**Anniversary banners:** rerun-style, multiple past banners selectable.

**Recipe for our game:** Replicate all four banner types. Add our Hidden Banner for Jared/Justin twice yearly. Anniversary cadence: monthly minor anniversaries plus annual major (March = main game release; September = Ragnarok release). Reruns selectable during anniversaries.

### Currency split
Memoria Freeze separates premium currency: Paid Iris (purchased) and free Iris (earned). Paid banners require Paid Iris specifically. This separates whales from F2P in monetization without blocking F2P from progress.

**Recipe for our game:** Same split. Paid Iris becomes "Sapphire Crystals" (paid). Free becomes "Mana Stones" (earned). Both can pull on standard banners. Paid-only on Hidden Banner (Jared/Justin).

### Pull cost economics
- Single pull: 40 Iris (Memoria Freeze)
- 11-pull: 400 Iris (10% discount + guaranteed pulls)
- ~$1 per 100 Iris average bundle pricing

**Recipe for our game:** Same structure. Single 40, multi (11) 400 with guaranteed pulls. ~$1/100 Mana Stones at base bundle. 1000-bundle includes 3 guaranteed SSRs + bond + resources for $9.99 (anchored at psychological 9.99 price point).

### Pity counter
Industry standard: 80-90 pulls without SSR triggers guarantee.

**Recipe for our game:**
- Standard banner: 90 pulls = guaranteed SSR
- Limited banner: 80 pulls = guaranteed featured SSR
- Hidden banner (Jared/Justin): NO PITY (preserves rarity)
- Carries between banners of same type (don't reset every banner change)

---

## 4. Monetization patterns

### Subscription tiers
Memoria Freeze had two confirmed subscription products:
- Lower tier (Syr-themed daily): Daily login currency + small bundle
- Higher tier (Hostess full course): More currency, more bundles, exclusive items

**Recipe for our game:**
- Lower tier ($4.99/mo): Daily 100 Mana Stones + small daily bundle
- Higher tier ($9.99/mo): Daily 200 Mana Stones + premium bundle + exclusive cosmetic + monthly Hidden-banner ticket
- Both renew monthly. Cancel-able anytime. No power-tier mechanics locked behind subscriptions (cosmetics + currency only).

### Bundles
Memoria Freeze 1000-Iris bundles included 3 guaranteed 4-stars + bond + resources. This is more cost-efficient per 4-star than direct pulls. Bundles include "joker" bonds (limit-break wildcards) and resources.

**Recipe for our game:** Same bundle architecture. Tier prices: $9.99 / $19.99 / $49.99 / $99.99. Each scales bundle contents proportionally. Highest-tier bundle includes Hidden Banner ticket (rare).

### Anniversary monetization
Memoria Freeze 5th Anniversary (June 2022): 100 Iris/day for 5 days, rerun banners, special Pick-3-from-21 Sacred Flame Festival gacha (Paid Iris only, 7 pulls each guarantees 4-star).

**Recipe for our game:** Annual anniversary events with similar structure. Daily login rewards, rerun selectable banners, pick-N-from-pool special events with guaranteed limited-tier acquisitions. Anniversary spending pattern is the highest-revenue period; design accordingly.

### Daily / weekly engagement loops
Memoria Freeze daily missions (typical):
1. Log in (x2 - morning + evening incentivize check-back)
2. Clear an episode
3. Strengthen a character (level or board)
4. Complete a Falna quest
5. Complete an Excelia quest
6. Talk to characters (3 of them)
7. Clear all daily missions (capstone)

**Recipe for our game:** Same daily-mission structure with 7 tasks. Talk-to-characters social interaction is underrated - add it to bond mechanic. Capstone "all dailies" reward at the end of the day.

Weekly: Memoria Freeze had Tuesday Falna keys (30-min drop rate boost). Free key per week.

**Recipe:** Same. Friday Hunter Key: 30-min XP boost for raids. Free per week.

---

## 5. Endgame mode patterns

### War Game (ranking PvP)
Memoria Freeze's PvP mode used a score-add/subtract system. Players' rank fluctuated based on match outcomes. Best teams optimized for specific stats: Strength + AOE for Phys teams, Magic + AOE for Mag teams, Counter rate for defensive teams.

**Recipe for our game:** Same architecture. 4v4 ranked PvP with our tier ladder (E-rank to Ruler). Score-add/subtract within tier. Featured banned-character pool rotates weekly to prevent stagnation.

### Record Buster (single-target damage challenge)
Time-limited content where players score by damage dealt to a specific high-HP boss. Single-target specialists excel.

**Recipe for our game:** Same mode, branded as "Hunter Trial". Single-target boss with massive HP. Solo damage challenge. Leaderboards with seasonal rewards.

### Familia Chronicle / story-link content
Time-limited story arcs with banner pulls themed to that arc.

**Recipe for our game:** Solo Leveling arcs (Demon Castle, Red Gate, Jeju Island) released as time-limited story events with themed banners. Each arc adds new playable Hunters with kits matching the arc.

### Anniversary content
Big content drops at anniversaries with reruns + new banners + rare collectibles.

**Recipe:** Major release in March (game launch anniversary) and September (Ragnarok release). Reruns selectable, rare anniversary-only Hunters.

---

## 6. What Memoria Freeze did right (preserve)

1. **Step-up banner with guaranteed pulls** - exceptional new-player experience, retention rate driver
2. **Limit Break via duplicates** - duplicate-as-progression solves the "what do I do with extra pulls" problem
3. **Joker bonds for wildcard limit break** - safety valve for rare characters
4. **Adventurer + Assist split** - doubles gacha surface area without doubling production
5. **Status Board for character investment** - 50+ hours of per-character progression depth
6. **Multi-stat damage interplay** - depth without complexity
7. **Anniversary cadence** - drives 30%+ of annual revenue
8. **Subscription tiers** - low-pressure recurring revenue
9. **Daily mission cadence** - retention driver
10. **Element advantage system** - gives team-comp meaning

## 7. What Memoria Freeze did wrong (improve on)

1. **Quality decline** - they couldn't sustain content cadence over 6 years. Solution: slower release cadence (one major update per quarter, not per month) so production doesn't burn out.
2. **Mobile-only** - never ported to PC or cloud streaming. Solution: even though we're mobile-only too, design for cross-platform UI scaling so future ports are cheap.
3. **English localization quality** - JP-first development sometimes left English text awkward. Solution: English-only from day 1 means no translation friction.
4. **No element-reaction combos** - elements only had advantage/disadvantage. Solution: add element-reaction combos (Fire+Ice=Melt, etc.) for tactical depth.
5. **Linear story progression** - main story unlocked sequentially. Solution: branching story choices in late game (post-Cup-of-Reincarnation timeline divergence).
6. **No PvP balance patches** - meta stagnated. Solution: weekly banned-character rotation in PvP.
7. **Aging engine** - 2017 mobile-tech showed in 2023. Solution: build on Godot 4 with modern best practices.

## 8. Our improvements over Memoria Freeze (the "make it great" delta)

1. **Element-reaction combos** add tactical depth beyond MF's element-advantage-only system
2. **Persistent-world Survivor system** that no MF-style game has done; world feels alive
3. **100-floor Demon Castle with zone-distinct biomes and side quests** - depth-of-place beyond MF's standard dungeons
4. **Bond/Social-link mechanic with 10 ranks per Hunter** - emotional weight MF lacked
5. **Solo Leveling IP recognition** - stronger than DanMachi for international English audience
6. **Modern engine (Godot 4)** - smoother performance, faster iteration than MF's aging tech
7. **Dual-protagonist story (Jinwoo → Suho)** - generational arc that MF didn't have, supports long-term content runway
8. **Honest gacha rates** - we display rates clearly upfront (anti-FOMO discipline)
9. **No timed-deal manipulation** - we don't use predatory scarcity tactics
10. **Hidden-tier rare characters with handicap in low-rank PvP** - prevents pay-to-win pressure even with whale-tier pulls
11. **Memoria-Freeze-style attack visualization PLUS combo/reaction depth** - polish AND depth, not one or the other
12. **Cross-platform-ready architecture even for mobile-only launch** - sequel/port pivot stays cheap

---

## Bottom line

Memoria Freeze validated the format. Our game inherits the proven patterns and adds the depth-and-polish layer they couldn't sustain over 6 years. Same skeleton, better muscles, modern skin.

Pory and Jr should treat this doc as the secondary reference (after the canon codex). When implementing combat, gacha, progression, or monetization, start from the MF pattern documented here and apply our improvements.

The IP-discipline note: this doc summarizes structural patterns publicly documented in community wikis and beginner guides. No game text, character names, story content, or copyrighted material is reproduced. The PATTERNS (gacha rate structure, banner formats, stat systems) are not copyrightable. Implementation in our game uses our own canon-faithful flavor with all original character names and Solo-Leveling-themed content.
