# Reference Images Guide

How to use the per-character reference files in this folder.

## What this is

Each markdown file in this folder corresponds to one character. Each lists 10 image references with:
- A short description of what the image shows (pose, scene, emotion, outfit)
- A source URL where the actual image can be found
- A ready-to-paste prompt for Stable Diffusion or Midjourney that approximates the same visual

Public-repo discipline: we link to source pages rather than embed copyrighted manhwa art. For your personal/family build copy, you can manually download the actual image files from the source URLs and store them in a folder Jared keeps locally and gitignored.

## How Pory uses this

When generating portrait or sprite art for a character:
1. Open the character's reference file
2. Read the 10 descriptions for inspiration on poses, expressions, outfits
3. Use the provided prompt seed as a starting point
4. Modify based on the specific portrait variant you're creating (per the art bible's 30-portraits-per-character spec)
5. Iterate until the rendered output matches the canonical look

## How Jared uses this

When evaluating Pory's prompts and rendered output:
1. Cross-reference against the source URL to confirm the rendered art matches canon
2. Hand-touch in Krita or Aseprite if AI output is close but not perfect
3. Tag in the asset master list which reference image inspired the final render

## How Jr uses this

For sprite work and battle visualizations:
1. Reference the action poses and scene descriptions to inform sprite animations
2. Use the boss-encounter scene descriptions to plan combat backgrounds
3. Reference the canonical color palettes when implementing shaders

## Source URL conventions

- `solo-leveling.fandom.com/wiki/[Character]/Gallery` - primary canonical source
- `myanimelist.net/character/[id]` - secondary source, cleaner thumbnails
- `gelbooru.com/index.php?...&tags=[character]+official_art` - aggregated official art sources
- `displate.com/[poster]` - officially licensed commercial art
- `crunchyroll.com/anime-news` - press release artwork
- Twitter/X official accounts (@SLShotz, @sololeveling_pr) - source of new official art

## Personal vs case-study use

For the personal/family build copy: download all source images locally to a gitignored folder. No restrictions on use within your home network.

For the case-study deliverable: do NOT use the downloaded images directly in the shipped game. Use them as visual reference for AI generation only. The shipped case study should contain only your generated/painted art so it remains legally clean for showing to clients.

## File naming

Each character file is named by the character's primary canon name in lowercase with hyphens:
- `sung-jinwoo.md`
- `cha-hae-in.md`
- `beru.md`
- `igris.md`
- ...

Master roster is in `00-roster.md` (this file's neighbor).
