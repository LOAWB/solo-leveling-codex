# Solo Leveling Character Codex

Built for game-design reference. Source material: full anime story (Jeju Island onward) + manhwa canon + light novel where they diverge. All character entries link to the official Fandom wiki page for canonical portraits and full lore.

**Companion transcripts** (full universe split by arc, all source videos covered):

- `transcripts/awakening-through-jeju/` - pre-System through Jeju Island (10h8m source, 122K words).
- `transcripts/post-jeju/` - Ahjin Guild Arc through Cup of Reincarnation epilogue (9h28m source, 105K words).
- `transcripts/ragnarok/` - post-canon sequel following Sung Suho (16h27m source, 178K words).

Together they cover the entire Solo Leveling universe end-to-end including the Ragnarok continuation (~405K words clean text). The character codex was built primarily on the original canon; Ragnarok-era characters are not yet expanded but the transcript supports a future codex pass.

## How this is organized

- **01-power-system.md** - the rank hierarchy from E-Rank to Monarch to Ruler, with thresholds.
- **02-tier-list.md** - every named character placed in their power tier with one-line justification.
- **03-jinwoo-development-tracker.md** - Sung Jinwoo's progression timeline, level by level, with arc-by-arc strength jumps.
- **04-dungeon-mechanics.md** - Gate types, dungeon classification, time pressure, loot economy, special variants (Double / Red Gate / Field-Type / Instant / System), Daily Quest, item registry. Game-design portable.
- **05-bestiary.md** - all 47+ named Magic Beasts plus species-tier swarms, organized by rank and faction. Boss list, conversion paths (Arise mechanic), Monarch-army mapping, item drops.
- **06-items-and-drops.md** - every notable canonical item: currency tiers, Rune Stones, top-tier artifacts (Black Heart, Kamish's Wrath, Cup of Reincarnation), mid-tier weapons, race-specific drops, System Shop items, gear progression. Game-design item economy.
- **characters/** - individual files per character, grouped by role.

## Character categories

- **protagonists/** - Sung Jinwoo, Cha Hae-In, Yoo Jinho.
- **family/** - Sung Il-Hwan (father), Park Kyung-Hye (mother), Sung Jin-Ah (sister), Sung Suho (son with Hae-In).
- **korea-s-rank/** - Baek Yoonho, Choi Jong-In, Ma Dongwook, Lim Tae-Gyu, Min Byung-Gyu, Go Gunhee.
- **national-level/** - Thomas Andre (US), Liu Zhigang (China), Christopher Reed (US), Goto Ryuji (Japan), Siddharth Bachchan (India), Lennart Niermann (Germany).
- **allies/** - Woo Jinchul, Lee Joohee.
- **antagonists/** - Hwang Dongsoo, Hwang Dongsuk.
- **monarchs/** - all 9 (Antares, Ashborn, Baruka, Rakan, Tarnak, Legia, Querehsha, Yogumunt, Baran).
- **shadows/** - Jinwoo's army (Igris, Beru, Bellion, Tusk, Iron, Kaisel, Tank, Greed).
- **rulers/** - overview file (the Rulers operate as a faction).
- **magic-beasts/** - major non-Monarch threats (Kamish, Ant King).
- **cameos/** - original side characters (Jared, Justin), not Solo Leveling canon. Slotted into the universe with kits that reflect their real-world archetypes.
- **ragnarok/** - Ragnarok-era sequel characters (Suho, Tiel, Brocky, Arsha, the Itarim faction, Apostles, Stardust mechanics, Fiend / Hyena Guilds, Lee Minsung, Lim Tae-Gyu in his new role). Distinct from `family/sung-suho.md` which has the original-canon shorter entry.

## Per-character file structure

Each character file has:

```
# Name
**Wiki:** [link to Fandom page]
**Rank:** E / D / C / B / A / S / National / Monarch / Ruler
**Class:** Hunter type / Magic Beast / Shadow / etc.
**First appearance:** arc/chapter

## Bio
Compact backstory, 2-4 paragraphs.

## Abilities
Bullet list of named skills, passives, items. Power-relevant only.

## Strength notes
Who they beat, who beats them, where they sit in the ranking.

## Development arc
What changes from intro to current canon position.
```

## Game-design context

Notes embedded throughout flag mechanics that translate to game systems:
- **Class-uniqueness** moments (Jinwoo's Player class, Necromancer line)
- **Ability triggers** (Ruler's Authority, Dragon's Fear, Shadow Save)
- **Resurrection economy** (Arise mechanic, shadow extraction)
- **Stat caps and breakthroughs** (level cap removal, double awakening)
- **Faction relationships** (Monarchs vs Rulers vs Hunters, betrayal pivots)
