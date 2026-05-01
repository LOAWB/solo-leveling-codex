# Build Team Capabilities

What Pory (GPT-5.5 Max via codex CLI) and Jr (Claude Opus 4.7 1M context) need to be capable of, and how the $200 budget gets spent.

This document is the capability checklist. Treat it as the qualification bar before kickoff. If a skill below is shaky, surface it early so the team can compensate.

---

## Pory's role and required capabilities

Pory is the prompt-engineer, content writer, design balance partner, and code-review second pair of eyes.

### Art and prompt engineering
- Stable Diffusion prompt engineering for anime portrait generation
- Manhwa art style replication via prompt structure (Redice Studio aesthetic, Solo Leveling color palette)
- Pokemon Black/White animated sprite prompt engineering (pixel art, transparent background, frame-by-frame animation)
- Pokemon DS overworld sprite specs (32x32 four-direction walk cycles)
- Tileset specification language (32x32 grid tiles, dungeon-themed coherent palettes)
- UI element prompts (System panel aesthetic, gold-on-black, purple-glow accents)
- VFX particle prompts (Pokemon-Black-White-era, frame-by-frame)
- Title screen, loading screen, achievement icon prompt language
- Iteration: when Jared renders a result that doesn't match the bible, Pory revises the prompt

### Content writing
- Quest dialogue (in-character voices for Jinwoo, Cha Hae-In, Yoo Jinho, Beru, Igris, Sung Il-Hwan, Park Kyung-Hye, Sung Jin-Ah, etc.)
- Item descriptions (souls-style lore-dense descriptions for every artifact, weapon, drop)
- Magic Beast bestiary entries (in-game)
- Cutscene scripting
- Tutorial text for game systems
- Achievement / quest titles and descriptions
- Bond rank conversation trees per Hunter

### Game design and balance
- Turn-based combat damage formula design (Pokemon-style: stats + level + type matchup + crit + STAB)
- Gacha rate balancing (per-rarity pull rates, pity system thresholds, banner-specific featured rate-ups)
- Player progression curve (XP-to-level table, stat-points-per-level, gear-tier progression timing)
- Magic Beast stat tables (HP, ATK, DEF, SPD, type, abilities, drops)
- Skill balance (cooldown, damage, MP cost, status effect rates)
- Quest reward balancing
- Daily Quest reward scaling for streaks
- Penalty Zone scaling (stays threatening but not unfair)

### Design documents
- Asset master list (which assets exist, which don't, completion status)
- Content tables in markdown / CSV / JSON for handoff to Jr
- Build phase plans
- Test plans for each major feature
- Bug tracker entries

### Code review (secondary)
- GDScript review (catch logic errors, performance issues)
- C# review if Unity option chosen
- General software architecture critique
- API design review

---

## Jr's role and required capabilities

Jr is the engineer building the actual game. Jr's deep context (1M tokens) holds the entire codebase plus the codex, which means cross-system reasoning is reliable.

### Engine and language
- Godot 4.x (current stable: 4.3+)
- GDScript (Godot's primary language) - syntax, idioms, performance patterns
- Optional: C# in Godot if Pory and Jared prefer for any reason
- Godot scene structure and node hierarchy
- Godot signals (event-driven communication)
- Godot resources (custom data files for content tables)
- Godot exports (variables editable in editor)
- Godot autoloads (singleton management)

### 2D RPG-specific
- TileMap node setup with collision layers
- 2D tile-based pathfinding (built-in Godot AStar2D)
- AnimatedSprite2D and AnimationPlayer for character sprites
- 2D camera management (Camera2D with smoothing, screen shake)
- Parallax backgrounds for depth
- Dialogue UI implementation
- Inventory UI implementation
- Menu system (main menu, pause menu, settings)

### Combat system architecture
- Turn-based combat state machine
- Action queue and priority resolution
- Type-effectiveness chart implementation
- Damage formula implementation
- Status effect system (poison, paralysis, sleep, freeze, burn, electrocute, brainwashed)
- Ultimate meter management
- Animation timing and sync with UI (damage numbers floating up at right time)
- Memoria-Freeze-style combat visualization (camera zoom on attacker, portrait flash, slash overlay, damage numbers)

### Gacha system
- Weighted RNG implementation with proper seeding
- Pity counter implementation
- Banner system (multiple concurrent banners, rotating featured characters)
- Summon animation framework
- Currency management (Mana Stones, Powder of Inheritance, summon tickets)
- Duplicate detection and Awakening rank progression

### Save/load
- Godot resource serialization
- JSON save format with versioning
- Save slot management
- Cloud save (optional, via Steam Cloud integration if shipped commercially; skip for personal-use)
- Auto-save vs manual save handling

### UI
- Godot Control node tree
- Theme system for consistent styling
- Responsive layouts (different screen sizes / aspect ratios)
- Animated UI transitions
- System panel UI faithful to canon (gold-on-black, purple-glow)
- Custom shader for the System panel translucent effect

### Audio
- AudioStreamPlayer for SFX
- AudioStreamPlayer2D for positional audio
- Music looping and adaptive music layering
- Audio compression and asset management

### VFX
- Godot particle systems (CPUParticles2D, GPUParticles2D)
- Shaders for special effects (Shadow Army purple aura, element reactions, ultimate cinematic flashes)
- Sprite batching for many simultaneous particles
- Screen-space effects (screen shake, full-screen flashes for ultimates)

### Game systems
- Quest system with state tracking
- Dialogue tree system with branching
- Achievement system
- Daily Quest scheduling (real-time clock or in-game time)
- Penalty Zone trigger and execution
- Survivor / Nemesis system (procedural rivals with persistent state)
- Bond rank tracking
- Faction reputation tracking
- Shadow army roster management
- Bestowal system (item-to-companion permanent transfer)

### Performance and optimization
- Sprite batching
- Scene pooling for repeated content
- Memory management (Godot's automatic refcount, but careful with circular references)
- Profiling via Godot built-in profiler
- Frame rate targeting (60fps minimum on Mac/PC)

### Cross-platform
- Mac native build (.app)
- Windows build (.exe)
- Linux build
- Browser export via HTML5 (for easy family sharing)
- Per-platform asset optimization

### Git workflow
- Atomic commits
- Branch management for parallel feature work
- Conflict resolution
- Tag-based release management
- README and CONTRIBUTING docs

### Testing
- Manual playtest scripting
- Automated test suite for critical systems (combat math, gacha math, save/load roundtrip)
- Bug reproduction documentation
- Regression test harness

---

## Skills both need

### Solo Leveling lore
The codex (this repo) is the canonical reference. Both agents should consume:
- All character files in `characters/`
- Power system in `01-power-system.md`
- Bestiary in `05-bestiary.md`
- Items registry in `06-items-and-drops.md`
- Master design synthesis in `09-master-design-synthesis.md`
- Art bible in `10-art-bible.md`

### Memoria Freeze combat visualization
- Portrait + flash + damage numbers pattern
- Card-flip ultimate animations
- Element-color-coded backgrounds during attacks
- Camera-zoom on attacker, no full sprite combat animation needed

### Pokemon-DS / Pokemon-MMO world structure
- Tile-based 2D overworld
- Towns connected by routes
- Random encounters in dungeon zones
- Building interiors as separate scenes
- NPC dialogue interactions
- Persistent home base (Sung family apartment + Ahjin Guild HQ)

### Pokemon-style turn-based combat
- 4-character active party with bench
- Swap-as-turn mechanic
- Type effectiveness chart
- Status effects
- Critical hits, Break gauge, Ultimate meter
- Item usage in combat

---

## $200 budget allocation

Existing subscriptions (NOT from this $200):
- Claude Max plan: ~$200/month (already paying)
- GPT-5.5 Max plan: ~$200/month (already paying)

The $200 buys tools and one-time assets:

### Must-have tools

| Item | Cost | Why |
|------|------|-----|
| Aseprite (pixel art editor) | $20 (one-time) | Best-in-class for pixel art. Onion skin, palette mgmt, animation export. |
| Steam Direct fee | $0 (skip) | Personal use only. No commercial release needed. |
| Godot engine | $0 | Free, open source. |
| Stable Diffusion (local) | $0 | Free, runs on Mac. |
| GitHub (private repo) | $0 | Free unlimited private repos. |
| Audacity (audio editor) | $0 | Free. |
| LMMS or Bosca Ceoil (music DAW) | $0 | Free. |
| freesound.org SFX library | $0 | Free under CC license. |
| **Subtotal** | **$20** | Foundation tooling. |

### Quality-of-life upgrades (recommended)

| Item | Cost | Why |
|------|------|-----|
| Midjourney 1 month | $30 | Higher-quality AI portrait base art than local SD. Cancel after one month of bulk generation. |
| Suno AI Pro 1 month | $10 | Higher-quality AI music for ~12 game tracks. |
| ElevenLabs Starter 1 month | $5 | Optional voice acting for key cutscene lines. |
| Anime LoRA model packs | $0 | Free download from Civitai for local SD. |
| **Subtotal** | **$45** | Premium polish layer. |

### Asset commissions (optional)

| Item | Cost | Why |
|------|------|-----|
| Indie commission for 5 hero portraits | $50-100 | If you want one truly polished artist-touched piece for marketing screenshots. |
| Royalty-free music tracks | $0-30 | If Suno output isn't enough. |
| **Subtotal** | **$50-130** | Use only if AI art alone doesn't carry the vision. |

### Buffer / contingency

| Item | Cost | Why |
|------|------|-----|
| Storage upgrade for assets | $0-20 | If your Mac runs low on space. |
| Steam Direct fee (if commercial pivot) | $100 | Refundable after $1K sales. |
| Misc | $0-20 | Unexpected. |

### Recommended $200 allocation

- Aseprite: $20
- Midjourney 1 month for bulk portrait gen: $30
- Suno AI Pro 1 month: $10
- ElevenLabs Starter 1 month: $5
- Anime LoRA + Stable Diffusion local setup: $0
- Buffer for indie commission of 1-2 hero portraits: $50-100
- Reserve: $35-85

Total spent: $115-165, leaving $35-85 reserve for contingencies. Well within budget.

---

## Skills checklist (qualification bar)

Print this checklist. Walk through it with Pory and Jr at kickoff. If anything is shaky, address it before code starts.

### Pory checklist

- [ ] Can write 100+ Stable Diffusion prompts in the manhwa-anime style consistently
- [ ] Can iterate on a prompt when Jared rejects the rendered result
- [ ] Can write in-character dialogue for major canon characters (Jinwoo, Cha Hae-In, Beru, etc.)
- [ ] Can write souls-style item descriptions (lore-dense, world-building)
- [ ] Can balance turn-based combat math (hit a target Time-To-Kill on fights)
- [ ] Can balance gacha rates with pity systems
- [ ] Can read GDScript and catch logic errors
- [ ] Can manage an asset spreadsheet
- [ ] Can stay disciplined to the codex's canon constraints

### Jr checklist

- [ ] Has working knowledge of Godot 4.x and GDScript idioms
- [ ] Can structure a multi-scene Godot project cleanly
- [ ] Can implement a turn-based combat state machine
- [ ] Can implement a Pokemon-style team-of-4 with swap-as-turn
- [ ] Can implement a weighted-RNG gacha system with pity counter
- [ ] Can implement Memoria-Freeze-style combat visualization (portrait + flash + numbers)
- [ ] Can write a JSON-based save/load system with versioning
- [ ] Can implement a quest system with state tracking
- [ ] Can implement a dialogue tree system
- [ ] Can implement procedural Survivor / Nemesis state
- [ ] Can implement Daily Quest scheduling
- [ ] Can ship a Mac native build and a browser HTML5 build
- [ ] Can manage Git atomically
- [ ] Can profile and optimize when frame drops happen
- [ ] Can stay disciplined to the codex and synthesis docs

### Both

- [ ] Have read the entire codex (this repo) at kickoff
- [ ] Agree on the design synthesis as the binding contract
- [ ] Agree on the art bible as the visual contract
- [ ] Agree on a weekly checkpoint cadence
- [ ] Have a clear escalation path if blocked

---

## Workflow recommendations

### Project structure (Godot)
```
solo-leveling-game/
├── project.godot
├── scenes/
│   ├── main.tscn
│   ├── battle/
│   ├── overworld/
│   ├── ui/
│   └── cutscenes/
├── scripts/
│   ├── combat/
│   ├── gacha/
│   ├── save/
│   ├── nemesis/
│   └── characters/
├── assets/
│   ├── portraits/
│   ├── sprites/
│   ├── tilesets/
│   ├── ui/
│   ├── vfx/
│   ├── audio/
│   └── music/
├── data/
│   ├── characters.json
│   ├── magic_beasts.json
│   ├── items.json
│   ├── skills.json
│   ├── quests.json
│   └── dialogue.json
└── docs/
    └── (link to codex repo)
```

### Daily workflow (when actively building)
1. Jared: review yesterday's commits and assets, set today's priority
2. Pory: write art prompts and content for today's priority
3. Jared: render art with Pory's prompts, hand-touch as needed
4. Jr: implement code for today's priority while assets render
5. Jr: integrate new assets at end of day
6. Jared: playtest and report bugs
7. Pory + Jr: fix bugs, prep tomorrow

### Weekly checkpoint
- Demo current build to family
- Identify what worked and what didn't
- Adjust scope if needed
- Pory updates the asset master list and design balance
- Jr updates the codebase architecture doc
- Commit and tag the week's milestone

### Phase ordering (recommended)
1. **Week 1-2**: Vertical slice (one character, one battle, one summon, one tile dungeon)
2. **Week 3-4**: Three more characters playable, first full mission
3. **Week 5-6**: Combat polish + UI complete + gacha animations
4. **Week 7-8**: Story missions through Cartenon Temple Arc complete
5. **Week 9-10**: Demon Castle Arc + Red Gate Arc
6. **Week 11-12**: Hunters Guild + Jeju Island Arc
7. **Week 13-14**: Polish, balance, family playtest, ship

12-14 weeks (3-3.5 months) for case-study-quality demo with full canon arc coverage.

If you go family-fun-game-quality (more content depth), add 2-3 months for Ragnarok arc + endgame + Survivor system polish.

---

## Risk register

| Risk | Mitigation |
|------|-----------|
| Pory and Jr disagreeing on architecture | Codex synthesis doc is binding; resolve via re-read |
| AI art not landing the manhwa style | Use manhwa LoRA + reference panels for prompts; commission one indie artist for 1-2 hero pieces if needed |
| Combat math feels off in playtest | Pory rebalances, Jr re-implements; iterate weekly |
| Family playtesters don't enjoy it | Pivot scope: cut content, focus on what works |
| Solo Leveling-IP-curiosity getting public | Personal use only; never share build URL publicly |
| Pory or Jr context window filling up | Jr's 1M context handles entire codebase; Pory may need codebase summaries refreshed mid-session |
| Missing critical canon detail | Codex is the source of truth; if missing, add to codex first |

---

## Bottom line

Pory and Jr have all the skills needed for this scope if they have read the codex. The $200 budget is enough because:
- Engine and most tooling are free
- AI art generation (local SD or Midjourney short-term) handles 90% of the visual work
- Aseprite at $20 covers the pixel-art polish layer
- Music and SFX have free or ultra-cheap options
- Personal-use scope eliminates Steam fees, marketing budget, IP licensing concerns

Spend wisely: $20 Aseprite + $30 Midjourney + $10 Suno + $5 ElevenLabs + $50-100 reserve for one human-artist commission if needed = $115-165, well under $200.

12-14 weeks of consistent build cadence ships a case-study-quality Solo Leveling Memoria-Freeze-style RPG with team-based combat, gacha summons, premium portraits, full canon arc coverage, and family-playable depth.

Brick by brick. The bricks are scoped. The team is qualified. The budget holds. Ship it.
