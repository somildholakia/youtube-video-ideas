# Season 1 Production Pack — The First Coordinate

Entry point for all 14 Season 1 episode folders.

## Per-episode production structure
- `script.md` — timed visual screenplay and continuity notes.
- `shot-list.csv` — 640 planned four-second shots, stable shot IDs, timestamps and panel-specific prompts.
- `audio-cues.csv` — 88 timed ambience, dialogue and SFX cues per episode.
- `collage-prompts.md` — eight separate ChatGPT collage prompts with exact panel-to-shot mapping.
- `README.md` — episode-specific production hand-off.

## Season totals
- 14 episodes and 112 sequences.
- 896 timed beats.
- 8,960 planned shots.
- 112 planned collage outputs (8 per episode), each a separate single image with exactly 80 panels in a 10-column × 8-row grid.
- 1,232 audio cue rows across the season.
- Assembly target: 42:40 per episode; actual audio and export runtime must be measured.

## Mandatory ChatGPT collage rule
Generate one collage image per sequence, exactly 80 equal-sized panels in a 10×8 grid, reading left-to-right and top-to-bottom, separated by clean visible borders. Each panel contains only its story image and a small sequence number; that number is the only text allowed. No captions, dialogue, subtitles, titles, descriptions, labels, logos, watermarks, UI, pseudo-writing, decorative filler or unrelated content. Do not merge batches.

Attach approved character, ship and location references. Shot-list CSV is the panel-level prompt source. Reject missing, duplicated, merged, illegible or continuity-breaking panels. Image generation may fail to honour an 80-cell grid; if so, split the sequence into smaller grids and retain global shot IDs. Never claim a malformed sheet contains 80 usable panels.

## Generation order
1. Generate and approve character reference images and the Wayfarer model reference.
2. Generate and approve the Season 1 location references.
3. Generate one collage at a time in ChatGPT from the matching batch prompt and shot manifest.
4. Inspect panel count, order, borders, unwanted text and continuity.
5. Generate audio from the exact dialogue and cue-sheet descriptions.
6. Expand current visual drafts into full actor-ready scripts, conform the edit to measured audio and verify 40–45 minutes.

## Completion status
Repository text packs are committed. The scripts are timed visual production drafts, not fully dialogue-dense final shooting scripts. Character/location artwork, collages, voices, final mixes and finished videos are not generated as part of this GitHub update.
