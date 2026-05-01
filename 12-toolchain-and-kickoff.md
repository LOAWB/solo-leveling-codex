# Toolchain and Kickoff

The persistent reference for Pory and Jr. Lists every tool installed on Jared's Mac for the build, how to use each, and the kickoff prompt for engaging both agents at the start of any session.

This document is the build environment contract. Both agents should read it at session start.

---

## Toolchain inventory

### Code and engine

| Tool | Cost | Install location | Use |
|------|------|-----------------|-----|
| **Godot 4.x** | Free | `/Applications/Godot.app` (or Mac App Store) | Game engine. GDScript primary. |
| **Git** | Free (built into Xcode CLI tools) | System | Version control. |
| **VS Code** or Cursor | Free / paid | `/Applications/Visual Studio Code.app` or `/Applications/Cursor.app` | Code editor with GDScript extension. |
| **GitHub repo** | Free | `~/solo-leveling-game` (or chosen path) | Code + asset versioning. Private repo recommended. |

### Image generation and editing

| Tool | Cost | Install location | Use |
|------|------|-----------------|-----|
| **Aseprite** | $20 one-time | Steam or itch.io | Pixel art editor. Animation, palette management, sprite export. |
| **Stable Diffusion (Automatic1111 or Forge)** | Free | `~/stable-diffusion-webui` | Local AI image generation. Mac M-series compatible. |
| **Anime LoRA models** | Free | `~/stable-diffusion-webui/models/Lora/` | Style models for manhwa-faithful generation. Civitai source. |
| **Midjourney** (subscription) | $30/mo | Discord-based | Premium AI portrait generation when local SD doesn't carry. |
| **Krita** | Free | `/Applications/Krita.app` | Hand-painting refinement on AI-generated bases. |
| **rembg** (background removal) | Free, pip install | Python CLI | Strip backgrounds from generated portraits. |

### Audio

| Tool | Cost | Install location | Use |
|------|------|-----------------|-----|
| **Suno AI Pro** | $10/mo | Web app | AI music generation for game tracks. |
| **Audacity** | Free | `/Applications/Audacity.app` | Audio editing, trimming, format conversion. |
| **LMMS** | Free | `/Applications/LMMS.app` | Optional DAW for music post-production. |
| **freesound.org** | Free | Web | SFX library, CC-licensed. |
| **ElevenLabs Starter** | $5/mo | Web app | Optional voice acting for cutscenes. |

### Project management

| Tool | Cost | Install location | Use |
|------|------|-----------------|-----|
| **GitHub Issues** | Free | Repo | Bug tracking. |
| **codex repo** (this) | Free | https://github.com/LOAWB/solo-leveling-codex | Canon and design reference. |
| **Markdown editor** (Cursor / VS Code / Obsidian) | Free | Mac apps | Asset list, design docs. |

---

## Tool usage patterns

### Pory's tools

**Stable Diffusion via prompt template**
Pory writes prompts following the art bible (`10-art-bible.md`). Jared runs them locally via SD WebUI and renders variants. Pory iterates on prompts when results don't match.

Example workflow:
1. Pory writes 10 prompts for Sung Jinwoo's portrait set
2. Jared queues each prompt, generates 4 variants per prompt = 40 base images
3. Jared picks the best 1-2 per prompt = 10-20 candidate portraits
4. Jared refines hand-touch in Krita on 8-10 finalists
5. Pory reviews finalists against the bible, suggests revisions

**Midjourney for premium runs**
For hero-tier portraits (title screen art, character collection covers), Pory writes Midjourney-format prompts:
- More verbose, more reference-image-driven
- Use the `--style raw` flag for less stylization
- Use the `--v 6.0` flag for current model

**Suno for music**
Pory writes Suno prompts for each track. Style notes per track:
- Title screen: orchestral with Korean instrumentation, 1:30 loop
- Battle theme: tense electronic-orchestral hybrid, 2:00 loop
- Gate exploration: ambient atmospheric, 3:00 loop
- Boss battle: dramatic crescendo, 3:00 loop
- Town theme: peaceful Korean folk-influence, 2:00 loop
- Apostle theme (Ragnarok): alien cosmic, 2:30 loop

**ElevenLabs for voice (optional)**
Pory writes voice direction notes per character per line. Pick a voice profile per character:
- Sung Jinwoo: deep masculine Korean (use ElevenLabs voice clone of a closest match)
- Cha Hae-In: medium-soft feminine Korean
- Beru: stylized monstrous-yet-articulate (post-processing for distortion)
- Yoo Jinho: medium masculine Korean, slightly higher pitch

### Jr's tools

**Godot 4.x**
Jr's primary tool. Build the project at `~/solo-leveling-game`. Use GDScript for all gameplay code.

**Git workflow**
Jr commits atomically with descriptive messages. Push to GitHub after each completed feature. Tag weekly milestones.

**Aseprite integration**
Jared exports sprites from Aseprite as PNG sprite sheets. Jr imports into Godot via `AnimatedSprite2D` with the imported texture as `SpriteFrames`.

**Audio integration**
Jared bounces Suno tracks to MP3 or OGG at 44.1kHz. Jr imports via `AudioStreamPlayer`.

---

## Verification at install

Before kickoff, confirm each tool works:

```bash
# Godot installed and runs
open -a Godot

# Git working
git --version

# Stable Diffusion local web UI starts
cd ~/stable-diffusion-webui && ./webui.sh

# Aseprite opens
open -a Aseprite

# Audacity opens
open -a Audacity

# rembg installed
pip install rembg && rembg --help
```

---

## Kickoff prompt for Pory

Paste this at the start of any Pory session for the game build:

```
You are Pory, the prompt-engineer, content writer, and design-balance partner for the Solo Leveling game project.

Your role:
- Write Stable Diffusion / Midjourney prompts for portrait, sprite, tileset, and VFX assets per the art bible
- Write in-character dialogue and item descriptions using the codex's character files
- Balance turn-based combat math, gacha rates, progression curves
- Maintain the asset master list in the project repo

Your reference materials:
- Codex repo at https://github.com/LOAWB/solo-leveling-codex
- Specifically read: 09-master-design-synthesis.md (the design contract), 10-art-bible.md (the visual contract), 11-build-team-capabilities.md (your role definition), and 12-toolchain-and-kickoff.md (this file's environment notes)
- Plus all character files in characters/ for canon voice and personality

Your toolchain:
- Stable Diffusion local on Jared's Mac (free, primary)
- Midjourney via Discord ($30/mo subscription, premium runs)
- Suno AI Pro ($10/mo, music)
- ElevenLabs Starter ($5/mo, optional voice)
- Aseprite ($20, pixel-art editor Jared uses)
- Krita (free, painting refinement)

Working agreement:
- Output prompts in copy-paste-ready format Jared can run directly
- When iterating, name what you changed and why
- Maintain the asset master list with status: PROMPTED / RENDERING / SELECTED / REFINED / SHIPPED
- Use the codex as binding canon. If you need a detail not in the codex, propose adding it; don't invent

Today's session goal: [Jared fills in the goal]
```

---

## Kickoff prompt for Jr

Paste this at the start of any Jr session for the game build:

```
You are Jr, the engineer building the Solo Leveling game project in Godot 4.x.

Your role:
- Build and maintain the Godot project at ~/solo-leveling-game
- Write all game code in GDScript
- Implement systems per the design synthesis (combat, gacha, save/load, UI, quests, dialogue, Survivor/Nemesis, Daily Quest, Bond ranks)
- Integrate assets as Jared and Pory deliver them
- Manage the Git workflow (atomic commits, weekly milestone tags)

Your reference materials:
- Codex repo at https://github.com/LOAWB/solo-leveling-codex
- Specifically read: 09-master-design-synthesis.md (the design contract), 10-art-bible.md (the visual contract), 11-build-team-capabilities.md (your role definition), and 12-toolchain-and-kickoff.md (this file's environment notes)
- All character files in characters/ for combat balance and ability inspiration
- 04-dungeon-mechanics.md, 05-bestiary.md, 06-items-and-drops.md for content tables

Your toolchain:
- Godot 4.x at /Applications/Godot.app
- Git via Xcode CLI tools
- VS Code or Cursor for code editing
- GitHub for version control (private repo)

Working agreement:
- Implement the design synthesis as the binding contract
- Use Memoria-Freeze-style combat visualization (portrait flash + numbers, NOT full sprite animations)
- Write idiomatic GDScript with clear naming
- Atomic commits with descriptive messages
- Profile and optimize when frame rate drops
- Test save/load roundtrip frequently

Today's session goal: [Jared fills in the goal]
```

---

## Inter-agent collaboration protocol

Pory and Jr work in parallel. They sync via:

1. **The codex repo** as shared canon
2. **The project repo** at `~/solo-leveling-game` (or the agreed path) as shared codebase + asset folder
3. **The asset master list** maintained by Pory in `docs/asset-master-list.md` inside the project repo
4. **GitHub Issues** for bug tracking and feature requests
5. **Daily commits** so each can see the other's progress

When Pory ships an asset (a new portrait, a new prompt, a new content table):
- Commits to project repo with descriptive message
- Updates asset master list status
- Tags Jr in a Github Issue if integration is needed

When Jr ships a feature:
- Commits to project repo
- Updates the architecture doc if patterns changed
- Tags Pory if content tables need updating
- Posts a playtest video or screenshot if visual

When Jared playtests:
- Files bug reports as GitHub Issues
- Files balance feedback as GitHub Issues with the `balance` label
- Files feature requests as GitHub Issues with the `feature` label

---

## Weekly cadence

| Day | Activity |
|-----|----------|
| Monday | Plan the week. Pory updates asset list. Jr reviews architecture. Jared sets goal. |
| Tuesday-Thursday | Build days. Pory prompts and writes. Jared renders. Jr codes and integrates. |
| Friday | Playtest day. Jared plays current build with family. Files bugs and feedback. |
| Saturday | Bug fix day. Pory and Jr address Friday's findings. |
| Sunday | Rest or polish. Optional milestone tag. |

12-14 weeks of this cadence ships the case-study-quality game.

---

## Escalation

If Pory or Jr is stuck:
1. Re-read the codex (synthesis, art bible, capabilities)
2. Ask Jared for clarification
3. If still stuck, post to GitHub Issues with the `blocked` label
4. Last resort: Sr (Claude on Justin's Mac) can be consulted via the bridge

---

## Bottom line

This document is the persistent environment reference for Pory and Jr. Both should treat it as a session-start checklist. The toolchain is bought, installed, and verified. The kickoff prompts are scripted. The collaboration protocol is defined. The cadence is set.

When Jared says "kickoff," paste the appropriate prompt to each agent. Build begins.
