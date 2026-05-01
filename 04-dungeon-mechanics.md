# Dungeon Mechanics

Solo Leveling's dungeon system is one of its most game-design-portable elements. Built for game reference: every dungeon type, mechanic, and edge case with the rules that govern them.

## World navigation format

The game uses a hybrid format: Pokemon Black/White-style 2D tile-based overworld for navigation, plus Memoria-Freeze-style turn-based combat for engagements.

### Overworld
- 2D tile-based pixel-sprite world (Pokemon DS scale, 32x32 tiles)
- Top-down or near-top-down perspective
- Walking with directional input (4-direction movement)
- Towns connected by routes (Seoul, Busan, Jeju Island accessible via ferry, Tokyo via airport, NYC for international content)
- Building interiors as separate scenes (family apartment, hospital, Korean Hunter Association HQ, Ahjin Guild HQ, individual guild HQs, hospitals, gear shops)
- NPC characters walking around with overworld sprites
- Dialogue interactions trigger when player approaches and presses interact
- Random encounters in dungeon zones (similar to Pokemon's tall grass)
- Gates appear as visible portals on the overworld map; entering one transitions to dungeon scene

### Dungeon scenes
- Internal layouts use the same 2D tile-based engine but with dungeon tilesets per environment (Cartenon Temple, Demon Castle, Red Gate ice cavern, Jeju ant colony, Tokyo gate ruins, etc.)
- Boss rooms are larger discrete scenes
- Exit Gate visible after boss defeat

### Combat engagement
- Triggered by enemy contact in overworld zones, story scripted encounters, or boss room entry
- Camera zooms and Memoria-Freeze-style turn-based combat takes over
- Portrait + flash + damage numbers visualization
- After combat resolution, return to overworld

This hybrid format combines the BEST of two genres: Pokemon's exploration loop with Memoria Freeze's combat depth and visual polish. Asset-efficient (sprites + portraits scale separately) while feeling premium.

## The Gate

A Gate is a tear in reality that connects Earth to a dungeon dimension. Gates appear suddenly, anywhere on Earth, with mana radiation that the public can sense as low-grade unease. Civilians cannot enter Gates; only awakened humans (Hunters) and Magic Beasts can pass through.

Gates are graded E to S based on the mana output of the dungeon inside.

## Gate burst (the time pressure mechanic)

If a Gate is not cleared within a time window proportional to its rank, it bursts. A burst Gate releases its contents into the surrounding area. The Magic Beasts inside flood the world.

- E-rank Gate burst: small group of low-tier monsters in a city.
- S-rank Gate burst: extinction-level threat to the surrounding region.

This is the foundational pressure of the hunter economy. Hunters MUST raid Gates; if they don't, civilians die.

## The dungeon interior

Inside a Gate, the dungeon dimension follows different physics. Time may flow differently. Light sources are intrinsic. Mana density is far higher than Earth. Gravity, atmosphere, and other physical constants vary by dungeon.

Each dungeon has:
- **Spawn area** (entry point, near the Gate).
- **Monster zones** (graded internally, often increasing in difficulty toward the boss).
- **Boss room** (the final encounter).
- **Loot drops**: mana stones (currency), magic items (gear), essence stones (crafting materials).
- **Exit Gate** (return point; only opens after the boss is defeated, or via Hunter Association extraction in emergencies).

## Rank classification

Hunters are graded E to S based on awakening. Dungeons are also graded E to S based on the boss-tier inside.

| Dungeon Rank | Boss Tier | Recommended Hunter Rank | Civilian Threat if Burst |
|--------------|-----------|------------------------|--------------------------|
| E | Low Magic Beast | E or D | Few civilian deaths |
| D | Mid Magic Beast | D or C | District-level damage |
| C | Strong Magic Beast | C or B | City-block damage |
| B | Elite Magic Beast | B or A | Multi-block damage |
| A | High Elite Magic Beast | A or S | City-level damage |
| S | Apex Magic Beast | S+ | National-level threat |
| (Special) | Outside-grade | National Level only | Extinction-level |

## Special dungeon types

### Double Dungeon

A hidden A-rank dungeon disguised as a D-rank from the outside. Hunters enter expecting D-rank and find A-rank threats inside. This is how Sung Jinwoo died/awakened. Double Dungeons are extremely rare but signal-tier important.

### Red Gate

A dungeon where the Gate seals upon entry; hunters can't leave until the boss is defeated. Time pressure becomes survival pressure: starvation, mana exhaustion, and freezing become the actual threats alongside the monsters.

### Field-Type Dungeon

A dungeon that contains an entire open landscape (field, forest, mountain) rather than a confined space. Significantly larger than standard dungeons. Boss rooms are scattered as zones rather than single chambers. The Paju Dungeon (Ragnarok era) is a Field-Type.

### Instant Dungeon

Player-class only. Sung Jinwoo can summon dungeons via the System with custom rules. These are System-generated training environments that don't follow the normal dungeon physics. The Cartenon Temple is the most famous Instant Dungeon, generated as Jinwoo's job-change quest.

### System Dungeons (Cartenon-tier)

Variant of Instant Dungeons that contain NPC characters with their own narratives. Esil Radiru is an example: a healer NPC in the Cartenon Temple System Dungeon who later transitions to active world canon. These dungeons blur the line between simulated and real.

### Magic-Beast-origin Dungeons

Dungeons where a Monarch's authority leaks through. The Demonic Castle Dungeon was Baran's domain. The Jeju Island Gate effectively functioned as the Ant King's territory. These dungeons are Monarch-tier internally even when graded as A or S externally. Tier mismatch is a recurring danger.

## The Demon Castle (100-floor tower)

The Demon Castle is the most significant fixed dungeon in canon. It is Baran's (Demon Monarch's) domain accessible through a permanent S-rank gate. Sung Jinwoo clears all 100 floors over the course of multiple visits as part of his Job Change Quest line and to gather Holy Water of Life ingredients.

In the game, the Demon Castle is a 100-floor scaling dungeon with both story-progression and endgame-replay tracks.

### Floor structure

| Floor range | Content tier | Encounter type | Boss |
|-------------|--------------|----------------|------|
| Floor 1 | A-rank | Boss room | **Cerberus** (three-headed dog gatekeeper, drops basic Demon Castle items) |
| Floors 2-24 | Demon-tier mobs scaling D to A | Demon corridors and rooms | Mini-boss Demon Spawn at every 5th floor |
| Floor 25 | A+ rank | Boss room | **Mid-tier Demon boss** (tier-defining loot, unlocks fast-travel from this point) |
| Floors 26-49 | Demon-tier rising A to S | Larger demon halls with elite spawns | Mini-boss every 10 floors |
| Floor 50 | S-rank | Boss room | **Vulcan** (Avaricious Demon S-rank, drops Demon Sovereign's Earrings + Orb of Avarice + Fragment of the World Tree) |
| Floors 51-74 | S-rank elite | Vulcan's Guards (A-rank) as elites in demon zones | Repeating mini-bosses |
| Floor 75 | S-rank | Boss room | **Metus** (S-rank Demon mid-boss) |
| Floors 76-99 | S+ rank peak demon zones | Peak-difficulty demon zones with Demon Castle elites | Repeating mini-bosses |
| Floor 100 | S+ rank Monarch tier | Final boss room | **Baran** (Demon Monarch, drops Demon King's Longsword + Baran's Rune Stone with Shadow Exchange skill) |

### Story-progression unlock pacing

Players unlock Demon Castle floors in this order in the canon arc:
- **First visit (Job Change Quest mid-arc):** floors 1-50, ending at Vulcan defeat
- **Second visit (post-Reawakening):** floors 51-75, ending at Metus
- **Third visit (post-Red-Gate):** floors 76-100, ending at Baran and full clear
- **Each floor unlocks fast-travel within the castle once cleared**

### Holy Water of Life crafting (gating quest)

After clearing all 100 floors, the player can craft Holy Water of Life. Required ingredients are scattered across the 100 floors:
- Floors 1-25: low-tier ingredient (Demon Tear)
- Floors 26-50: mid-tier ingredient (Vulcan's Liver, Fragment of the World Tree)
- Floors 51-75: high-tier ingredient (Metus's Heart)
- Floors 76-100: rare ingredient (Demon Sovereign's Pure Mana)
- Final synthesis happens at the System Shop terminal with all four ingredients
- Holy Water cures Eternal Slumber (Park Kyung-Hye coma) and other dungeon-derived illnesses

This is a major story milestone, not an endgame grind. Jinwoo's family arc resolution depends on it.

### Endless Demon Castle (post-canon endgame)

After first full clear, the Endless Demon Castle mode unlocks. Floors 100+ scaling difficulty:
- Weekly reset of run progression
- Random affixes per floor (Frost Aura, Mana Drought, Berserker Boss, Sanguine, etc.)
- Boss variants at every 25 floors with new mechanics (Cerberus + Vulcan + Metus + Baran return as scaled mid-bosses)
- New floors 101+ feature Apostle-aligned demon variants in Ragnarok-era content
- Tier-defining loot at every 10-floor breakpoint
- Speed-clear leaderboards
- Co-op support: 4-player co-op for higher floors with shared loot drops

### Demon Castle game-design value

- Story-locked content for ~30-40 hours of play across Job Change → Reawakening → Red Gate arc cadence
- Endgame replay content for indefinite engagement
- Iconic recognition: Demon Castle is the most-recognized dungeon in canon, fans will expect to see it
- Multi-tier loot economy: each floor range supplies different gear-tier crafting materials
- Anti-power-creep: the staggered floor unlocks pace player progression with story arc beats


## The boss encounter

Every dungeon has a boss. Defeating the boss:
1. Stops the gate from bursting.
2. Causes the boss to drop a mana stone proportional to its tier.
3. Opens the exit Gate.
4. (Player-class only) Allows shadow extraction via Arise.

If the party fails the boss but escapes back to the entry Gate, the dungeon remains "active" and the Gate burst countdown continues. Hunter Associations dispatch reinforcements.

## Loot economy

- **Mana stones**: dungeon currency. Sized by tier. S-rank mana stones power industrial-grade applications.
- **Magic items**: equipment that scales with dungeon tier. Above-A-rank items are rare even from S-rank dungeons.
- **Essence stones**: crafting materials, distinct from mana stones. Used for guild crafting projects.
- **Gold Essence Stones**: highest-tier crafting material. Rare. Tiel paid Lee Minsung in these for Stardust services.

## Dungeon raiding party composition

A standard mid-tier raid party:
- **Tank** (defense / aggro pull, like Iron or Yoo Jinho)
- **Healer** (rare class, force-multiplier)
- **Striker(s)** (DPS, like Cha Hae-In or Goto Ryuji)
- **Mage / AOE** (crowd control, like Choi Jong-In or Tusk)
- **Scout** (mobility, like Kaisel for aerial)

S-rank raids may run with multiple S-rank hunters as the entire party because each hunter is itself a raid-tier asset.

## Daily Quest (Player-class only)

Sung Jinwoo's System gives him a daily quest: 100 push-ups, 100 sit-ups, 100 squats, 10km run. Failing to complete results in transport to a Penalty Zone (a survival arena with a single magic beast). The Penalty Zone forces engagement with combat as the cost of skipping the quest.

The Daily Quest mechanic is unique to the Player class. No other hunter has it.

## Special items / artifacts

- **Holy Water (Elixir of Life)**: System Shop endgame item. Cures Eternal Slumber and other dungeon-derived illnesses. Jinwoo cures his mother with it.
- **Demon King's Longsword / Ashborn's blade**: pre-existing legendary weapons inherited via Monarch lineage.
- **Stardust** (Ragnarok era): Apostle-tier brainwashing drug. See `characters/ragnarok/stardust-and-mist-burns.md`.
- **Horn / Kasaka**: Sung Suho's inheritance items in Ragnarok.

## The Dungeon-as-System mechanic (game-design takeaways)

1. **Time pressure is universal**: every Gate eventually bursts. No skipping forever. Forces engagement with the loop.
2. **Rank mismatch is a real threat**: Double Dungeons, Monarch-origin dungeons, hidden Magic-Beast-tier mean the rank label is necessary but insufficient. Players must read the dungeon, not just trust the metadata.
3. **Boss-room reward structure is asymmetric**: only the Player class extracts shadows. Other classes get standard loot. Asymmetric reward is a class-defining feature.
4. **Field-Type dungeons and Instant Dungeons expand the dungeon design space**: not all dungeons are corridor-and-room. Some are open-world. Some are System-simulated.
5. **NPC characters can become PC characters**: Esil Radiru proves the fourth wall is permeable. Game-design opportunity for "this NPC matters" reveal moments.
6. **Burst mechanics scale faction stakes**: a national-tier S-rank Gate ignored doesn't just hurt one hunter; it threatens millions of civilians. Failure cascades.
7. **Daily Quest as forced engagement loop**: fail-state isn't game-over; it's a punishment encounter. Skipping is its own threat tier.
