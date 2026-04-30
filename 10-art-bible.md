# Art Bible

Every visual asset the game needs, with size specs, style guidance, and Pory-ready prompt language. Written for the workflow where Jared renders the art and Pory describes what's needed.

This document treats Pokemon-DS / Pokemon-3DS as the visual baseline, with anime-style premium portraits for collection / cutscene moments. Solo Leveling theme. Solo Leveling: Ragnarok manhwa palette as primary reference (Redice Studio's color work).

---

## Overall art direction

**Visual cohesion summary:** "Pokemon Black/White DS sprite style for in-game, with anime cinema-grade portraits for collection and cutscenes. Solo Leveling color palette: deep purples and blacks for shadow effects, gold accents for System UI, warm reds for Demons, cold blues for Frost, neon greens for Insects."

**Reference points:**
- In-battle and overworld sprites: Pokemon Black/White (gen 5) animated sprites
- Character portraits: Solo Leveling manhwa anime art style (Redice Studio aesthetic)
- UI: System panel canon visual (purple-glow gold-text on black)
- Backgrounds: high-contrast anime-illustration backgrounds for cutscenes; pixel-art tilesets for in-game

**Color palette anchor:**
- Shadow Army: pure black with purple aura highlights, neon-eye accents
- Player System: gold typography on translucent black panels
- Magic Beasts: faction-coded (Demons red/orange, Beasts brown/tan, Insects neon green, Snow Folk pale blue, etc.)
- Hunter outfits: nation-coded (Korean S-rank dark navy with gold trim, American Goliath earthy tones, Japan blade-honor crimson, etc.)

---

## 1. Character portraits

### Specs
- Size: 1024x1024 (collection screen) and 512x512 (cutscene dialogue boxes)
- Format: PNG transparent background
- Style: Solo Leveling manhwa (Redice Studio style), anime-cinema grade
- Detail level: high. Faces have distinct expressions. Eyes are focal points (purple glow for Awakened states).

### Per character: 30 variants

For each playable character, you need 30 portraits across these categories:

**Base set (8 portraits):**
1. Default neutral expression, full body or 3/4 portrait
2. Smiling / friendly
3. Determined / serious combat face
4. Surprised / shocked
5. Pained / wounded
6. Smug / confident
7. Sad / contemplative
8. Sleeping / unconscious

**Combat states (6 portraits):**
9. Casting basic skill (mid-action mid-frame)
10. Casting major skill
11. Ultimate activation (full power, dramatic angle)
12. Critical hit windup
13. Defensive stance / blocking
14. Defeated / KO

**Outfits (4 portraits):**
15. Casual civilian outfit
16. Hunter battle gear (rank-appropriate)
17. Formal attire (cutscene wedding / association meeting / social event)
18. Alternate seasonal / event outfit

**Awakened / evolution forms (6 portraits):**
For Player and Shadow companions:
19. Pre-System / pre-awakening form
20. Standard awakened form
21. Post-class-change form
22. Final-arc form (Shadow Monarch / Knight Killer / etc.)
23. Power-aura overlay (for cutscene reveals)
24. Shadow form (for shadows: silhouette with purple glow accents)

For non-Player Hunters:
19. Day-clothes / off-duty
20. Mid-tier rank gear
21. Peak rank gear
22. Special quest cutscene outfit
23. Bond-rank-10 reward outfit
24. Dramatic moment portrait (for their personal arc climax)

**Special poses (6 portraits):**
25. Action pose 1 (with weapon raised)
26. Action pose 2 (mid-leap or mid-dodge)
27. Group photo pose (interacts with other character placement)
28. Profile silhouette (for menu icons)
29. Backshot (for cutscenes)
30. Awakening / level-up cinematic moment (the "the player has leveled" beat)

### Pory prompt template per portrait

```
Solo Leveling manhwa anime style portrait of [CHARACTER NAME], [DESCRIPTION], [POSE], [EXPRESSION], [CLOTHING], [BACKGROUND OR TRANSPARENT], [LIGHTING], cinematic detail, high contrast, sharp linework, Redice Studio aesthetic, [size in pixels]
```

**Examples filled in:**

```
Solo Leveling manhwa anime style portrait of Sung Jinwoo, Korean S-rank hunter, three-quarter angle facing left, determined combat expression with glowing purple eyes, black hooded coat over dark armor with gold accents, transparent background, dramatic side-lighting from upper-right, cinematic detail, high contrast, sharp linework, Redice Studio aesthetic, 1024x1024
```

```
Solo Leveling manhwa anime style portrait of Cha Hae-In, Korean S-rank sword hunter, three-quarter angle, smiling softly with eyes half-closed, white and silver swordsman outfit with golden belt, transparent background, soft warm lighting, romantic cutscene moment, cinematic detail, sharp linework, Redice Studio aesthetic, 512x512
```

```
Solo Leveling manhwa anime style portrait of Beru, hypersonic shadow ant general, full body action pose mid-leap, neon yellow eyes glowing, light purple shadow aura with smoky wings extended, sharp claws raised for execution strike, transparent background, low-angle dramatic perspective, electric purple lighting, cinematic detail, sharp linework, Redice Studio aesthetic, 1024x1024
```

### Character roster for portraits (priority order)

Tier 1 (must have, each gets 30 portraits):
- Sung Jinwoo (Player)
- Cha Hae-In
- Yoo Jinho
- Beru
- Igris
- Sung Jin-Ah
- Sung Il-Hwan

Tier 2 (each gets 15-20 portraits):
- Baek Yoonho
- Choi Jong-In
- Goto Ryuji
- Thomas Andre
- Hwang Dongsoo
- Tusk
- Iron
- Bellion
- Park Kyung-Hye

Tier 3 (each gets 6-10 portraits):
- Min Byung-Gyu
- Ma Dongwook
- Lim Tae-Gyu
- Liu Zhigang
- Christopher Reed
- Woo Jinchul
- Lee Joohee
- Hwang Dongsuk
- Kasaka, Cerberus, Vulcan (boss-tier portraits, fewer expressions)

Antagonists (each gets 8-12 portraits):
- Antares (multiple phase forms)
- Ashborn (Ruler form + Monarch form + dissolution form)
- Baruka, Rakan, Tarnak, Querehsha, Yogumunt, Legia, Baran (one Monarch portrait set each)

Ragnarok era (each gets 10-15 portraits):
- Sung Suho
- Tiel (Apostle form + Park Dojin disguise)
- Lee Minsung (human + corrupted form)
- Brocky (Rakan-loyal + brainwashed forms)
- Arsha (human + Queen Bee form)
- Gray
- Esil Radiru

Cameos (each gets 6-8 portraits):
- Jared (Bond Hunter)
- Justin (System Architect)
- Severin (Bond-Breaker)
- Cipher (Unbuilder)

Total portraits to create: ~600-800 across all characters at full scope. Lower the count per character if scope-cutting; the Tier 1 roster's 30 each is the minimum case-study floor.

---

## 2. Battle sprites (Pokemon Black/White animated style)

### Specs
- Size: 96x96 base sprite, 256x256 for detail boss sprites
- Format: PNG with transparent background, animated frames
- Style: Pokemon Black/White animated sprite. Smooth idle animation, frame-based attacks
- Animation frames: 4-8 per animation cycle

### Per character: 6 animation sets

**Idle (4-frame loop):** subtle breathing, weight shift, hair sway
**Walk forward (4-frame loop):** for moving on the battle screen
**Basic attack (5-7 frames):** windup, strike, recover
**Major skill (6-8 frames):** more dramatic, includes VFX prep
**Ultimate (8-12 frames):** full cinematic pose-and-strike sequence
**Hurt / faint (3-frame static + fall):** damage reaction + KO state

### Pory prompt template per battle sprite

```
Pokemon Black/White animated battle sprite of [CHARACTER], [POSE / ACTION], 96x96 pixels, 4-frame [ANIMATION TYPE] loop, transparent background, anime-faithful color palette, subtle outline, Solo Leveling manhwa-derived design, retro-pixel style with smooth pixel motion
```

**Examples:**

```
Pokemon Black/White animated battle sprite of Sung Jinwoo, casting Shadow Extraction skill, 96x96 pixels, 6-frame animation cycle showing dagger raised then pointed forward as purple shadow tendril emerges, transparent background, anime-faithful palette of black coat with gold accents and purple aura, subtle outline, Solo Leveling manhwa-derived design, retro-pixel style with smooth motion
```

```
Pokemon Black/White animated battle sprite of Beru, performing Execution Strike ultimate, 256x256 pixels (boss-tier sprite), 10-frame animation cycle, hypersonic dash forward then dismembering scissor-strike, transparent background, neon yellow eyes with light purple shadow aura, retro-pixel anime-faithful color palette, smooth motion frames
```

### Boss-tier battle sprites

For the major boss encounters, sprite size goes up to 256x256 with multi-phase variants:

- **Cerberus (Demon Castle 1F)**: three-headed dog, 4-frame idle + 6-frame fire-breath + 4-frame charge attack
- **Vulcan (Demon Castle 50F)**: avaricious demon S-rank, 5 animation sets including Rage transformation
- **Baran (Demon Castle 100F)**: Demon Monarch lightning kit, 6 animation sets
- **Ant King (Jeju)**: hypersonic boss, 5 animation sets, dual-phase (sword form + final form)
- **Antares (Final Battle)**: dragon emperor, 256x256 minimum, 8 animation sets across 4 phases (Ground / Sky / Berserk / True Form)
- Each Monarch boss: 5-6 animation sets

---

## 3. Overworld sprites

### Specs
- Size: 32x32 (Pokemon DS scale) or 48x48 (slightly larger for mid-detail)
- Format: PNG transparent, 4-direction walk cycles
- Style: Pokemon DS overworld sprite, anime-faithful palette

### Per character: 4-direction walk cycle

**Walk down (4-frame):** facing camera, walking toward player view
**Walk up (4-frame):** facing away
**Walk left (4-frame):** profile view
**Walk right (4-frame):** profile view

### Pory prompt template per overworld sprite

```
Pokemon DS overworld sprite of [CHARACTER], 32x32 pixels, [DIRECTION] walk cycle, 4-frame animation, transparent background, anime-faithful color palette, retro-pixel style, Solo Leveling outfit detail at small scale
```

### NPC overworld variants

In addition to playable characters, generate generic overworld NPCs:
- Hunter Association staff (Korean, Japanese, American variants)
- Civilians (Seoul streets, hospital, family home)
- Other guild members (White Tiger Guild, Hunters Guild, Goliath Guild, Fame Guild)
- Vendors and merchants
- Reporter / journalist character types

Roughly 30-50 unique NPC sprite sets needed for a full game. Reuse with palette swaps.

---

## 4. Tileset specs

### Per dungeon: full tileset

Each canon dungeon gets a tileset with:
- Floor tiles (3-5 variants per environment)
- Wall tiles (corner pieces, straight pieces, doorways)
- Object tiles (chests, decoration, hazards)
- Special tiles (spawn point, exit Gate, boss room marker)

### Tileset list (priority)

1. **Hapjeong Subway Station tileset**: dim subway tunnels, fluorescent flickering, Kasaka-color palette (dark green + concrete gray)
2. **Cartenon Temple tileset**: Greek/Egyptian temple aesthetic, sandstone tiles, golden columns, statue pieces, Kasaka boss room
3. **Demon Castle tileset**: gothic stone, red-fire torches, demon-rune carvings, multi-floor stairwell elements
4. **Red Gate tileset**: ice cavern, snow piles, frozen-bone decorations, ice elf throne pieces
5. **Hunters Guild Gate tileset**: orcish encampment, wooden palisades, totems
6. **Jeju Island tileset**: ant colony / Korean beach village, sand and shell flooring, ant-tunnel walls
7. **Tokyo S-rank Gate tileset**: post-apocalyptic Tokyo streets, broken neon signs, giant footprints
8. **Seoul streets tileset**: modern Korean urban, civilian buildings, hunter association signage
9. **Pyramid Field tileset (Ragnarok)**: Egyptian-themed, golden sand, mummy decorations
10. **Glacier Dungeon tileset (Ragnarok)**: deep ice cave, Sirka-themed
11. **Apostle Stronghold tileset (Ragnarok endgame)**: cosmic Itarim aesthetic, alien geometry, Stardust shards

### Pory prompt template per tileset

```
Pokemon DS-era tileset for [DUNGEON NAME], 32x32 tiles, [BIOME] aesthetic, [LIGHTING] palette, anime-faithful color palette, retro-pixel style, includes floor / wall / object / special tiles, top-down perspective, complete set for a dungeon level
```

**Example:**

```
Pokemon DS-era tileset for Demon Castle dungeon, 32x32 tiles, gothic-fortress aesthetic, dim red-and-orange torchlight palette, anime-faithful color palette, retro-pixel style, includes stone floor variants (smooth / cracked / blood-stained), gothic wall tiles (corners / straights / doorways with pointed arches), demon-rune decoration tiles, fire-torch hazard tiles, Demon Sovereign throne piece, complete set for a multi-floor dungeon level
```

---

## 5. UI element specs

### System panel UI (the canon Player System interface)

The System panel is the IP's most iconic visual. Get this right.

**Style:** translucent black background panels with gold typography, purple-glow accents, futuristic-cosmic aesthetic. Reference: every shot of Jinwoo's System panel in the manhwa and anime.

**Elements needed:**
- Quest panel (rectangular, gold-bordered, displays quest text and rewards)
- Stat allocation panel (six stat bars: STR, AGI, VIT, INT, PER, plus 'free points')
- Inventory panel (grid layout, ~6x6 slots, gold-bordered)
- Skill panel (skill icons + descriptions)
- Map panel (full Korea map with gates marked)
- Notification popup (level-up, item drop, quest complete) - golden flash animation
- Daily Quest panel (4-task list with checkboxes)
- Penalty Zone warning (red-glow override of normal panel)
- Shop panel (item list + prices)
- Status panel (Player rank, level, current HP/MP, active buffs)

### Battle UI

- HP bars (color-coded by character)
- MP bars
- Skill icons (4 active per character)
- Ultimate meter (fills with combat)
- Type effectiveness indicator (when picking targets)
- Break gauge
- Turn order indicator (top of screen)
- Element reaction popups

### Gacha summon UI

- Banner display (the rotating featured-character art)
- Summon button (with single / 10x options)
- Pity counter
- Pull animation framework (bright flash → silhouette → reveal)
- Result display (rarity stars + character art reveal)
- Currency display (Mana Stones, Powder of Inheritance, summon tickets)

### Pory prompt template per UI element

```
Solo Leveling System panel UI element, [ELEMENT NAME], translucent black background, gold typography, purple-glow accents, futuristic-cosmic aesthetic, [DIMENSIONS], anime-faithful color palette, sharp clean lines, Redice Studio cosmic-system style
```

---

## 6. VFX prompts

### Spell and skill VFX

Each skill needs a particle effect. For pixel-art style, this means a 64x64 to 128x128 particle sprite with 6-12 frames of animation.

**VFX list (priority):**
- **Arise extraction**: purple shadow tendril rising from defeated enemy, 12-frame animation
- **Element reactions**: 9 distinct element-collision animations (Fire+Ice = Melt explosion, etc.)
- **Critical hit**: gold burst with star sparks
- **Ultimate cinematic**: full-screen flash with character silhouette
- **Damage numbers**: floating gold damage numbers, larger for crits
- **Status effect icons**: poison, paralysis, sleep, freeze, burn, electrocute
- **Shadow Army summon**: dark portal opening with shadow soldiers emerging
- **Shadow Exchange teleport**: purple flash + shadow trail
- **Dragon's Fear (Kamish skill)**: massive aura wave radiating from caster
- **Demon King's Longsword Lightning**: chain-lightning storm AOE
- **Holy Water cure**: golden light dispelling negative effects
- **Stardust corruption (Ragnarok)**: purple-and-black creeping aura

### Pory prompt template per VFX

```
Pokemon Black/White-era VFX particle sprite for [SKILL NAME], 64x64 pixels, [FRAME COUNT]-frame animation cycle, transparent background, [COLOR PALETTE], anime-faithful retro-pixel style, dramatic burst effect, [ANIMATION DESCRIPTION]
```

---

## 7. Title screen, loading, special screens

### Title screen
- Background: dramatic Solo Leveling cinematic art (Sung Jinwoo standing with Beru beside him, cosmic background with Antares silhouette in distance)
- Logo: stylized Solo Leveling-themed game logo
- "Press Start" prompt with subtle pulse animation
- Background music: orchestral theme

### Loading screens
- 8-12 unique loading screen art pieces, each featuring a different character or scene
- Loading bar with System-panel-style typography
- Tip text rotating on screen

### Game over / Penalty Zone screen
- Red-glow override of System panel
- Penalty Zone warning text
- Countdown timer animation

### Achievement icons
- 50-100 achievement icons, 64x64 each
- Themed: defeating major bosses, recruiting all shadows, completing arcs, finding hidden items

### Pory prompt templates

```
Solo Leveling cinematic title screen art, full HD widescreen, Sung Jinwoo standing center holding twin daggers, Beru hypersonic shadow ant kneeling at his side, dramatic purple-and-gold cosmic sky with silhouette of Antares dragon emperor in distant clouds, Redice Studio anime art style, manhwa-faithful palette, ultra-cinematic dramatic lighting
```

```
Solo Leveling loading screen illustration, full HD widescreen, [SCENE DESCRIPTION], Redice Studio anime art style, manhwa-faithful palette
```

---

## Workflow recommendations

### Order of asset creation

1. **Week 1-2: Hero art**
   - 30 portraits for Sung Jinwoo (the hero card)
   - Title screen art
   - System panel UI mockup
   - One battle sprite set (Jinwoo)
   - One overworld sprite set (Jinwoo)

2. **Week 3-4: Vertical slice characters**
   - 20 portraits each: Cha Hae-In, Beru, Igris
   - Battle sprite sets for those 3 characters
   - Overworld sprite sets for those 3 characters
   - First tileset: Cartenon Temple

3. **Week 5-6: Demo loop content**
   - Cartenon Temple complete tileset
   - 1 boss battle sprite (Kasaka)
   - VFX particles for first 5 skills
   - All UI elements for the demo

4. **Week 7-8: Polish + secondary content**
   - 6 more characters (Tier 2 priority)
   - Demon Castle tileset
   - More VFX
   - Loading screens, achievement icons

### Tooling for Jared rendering

- **Aseprite ($20)**: best pixel art tool. Onion skinning for animation, palette management, exports cleanly
- **Krita (free)**: best for digital painting / portrait work. Lots of brushes
- **Stable Diffusion local + Anime LoRA**: for AI-base portrait generation that you then refine in Krita
- **Background removal**: rembg.cli (free)
- **Animation compiler**: Aseprite (built-in) or aseprite-export to GameMaker / Godot

### Pory's role
- Write detailed prompts for each asset
- Iterate on prompts when first attempts don't land
- Maintain a master asset list with completion status
- Suggest stylistic revisions when a piece doesn't match the bible

### Jared's role
- Render the art (Stable Diffusion + Krita refine, or Aseprite for pixel work)
- Curate / select among AI-generated variants
- Hand-touch faces, hands, and other detail areas where AI struggles
- Final cleanup pass

### Jr's role (Claude on Jared's Mac)
- Build the Godot project
- Write code for game systems (combat, gacha, UI, save/load)
- Implement assets as they arrive
- Game balancing and content tables

This division splits the work cleanly: art and direction with Jared+Pory, code and systems with Jr.

---

## Asset count summary

For a polished case-study demo with 6-8 playable characters and 1-2 boss encounters:

- Portraits: ~150-240 (6-8 chars x 20-30 each)
- Battle sprites: ~50-80 frames (6-8 chars x 6 animation sets)
- Overworld sprites: ~32-48 (6-8 chars x 4 directions)
- Tilesets: 1-2 complete dungeons
- UI: ~30-50 elements
- VFX: ~20-30 particle effects
- Title / loading / special screens: ~10-15 pieces

**Total assets: ~300-500 pieces.** Achievable in 6-12 weeks at a steady pace with Jared rendering and Pory prompting.

For a complete game (all canon arcs + Ragnarok):
- Portraits: ~600-800
- Battle sprites: ~200+
- Tilesets: 8-11 complete dungeons
- Total assets: ~1500-2500 pieces. Achievable in 6-12 months.

The case study slice ships first. The complete game expands from there.
