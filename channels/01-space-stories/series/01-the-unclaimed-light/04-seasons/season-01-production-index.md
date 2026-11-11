# Season 1 Production Pack — The First Coordinate

This index is the entry point for the Season 1 production files.

## Global production contract
- Episode assembly target: 42:40, within the intended 40–45 minute range.
- Each episode uses 8 sequences × 5:20, 64 timed beats × 40 seconds and 640 planned shots × 4 seconds.
- Each episode has 8 separate ChatGPT collage outputs. Each collage is exactly one image containing 80 panels in a 10-column × 8-row grid. The sequence panel numbers are 001–080, with a visible border between every panel.
- Panel content: story image plus one small sequence number only. No captions, dialogue, titles, labels, logos, watermarks, UI or unrelated text.
- All dialogue in screenplay files is canonical; copy it verbatim into audio generation. Do not ask the image model to render text.
- Character and location IDs remain stable. Always attach approved character, ship and location reference images in ChatGPT image generation prompts.
- A collage is a contact sheet. Extract or regenerate individual frames after reviewing it; do not assume all 80 panels are individually production-perfect.

## Episode pack layout
Each episode folder contains:
- `script.md` — timed episode screenplay and continuity notes.
- `shot-list.csv` — 640 shot IDs, timecodes and panel-specific image prompts.
- `audio-cues.csv` — timed dialogue, ambience, SFX and score cues linked to shots.
- `collage-prompts.md` — eight separate 80-panel ChatGPT prompts with panel mapping.

## Quality gate
A generated image model cannot guarantee 80 perfectly legible panels from one prompt. If a single 80-panel image is illegible, split that batch into smaller collages and preserve the same global shot IDs. Never claim a malformed contact sheet contains 80 usable images. Final episode runtime must be checked against rendered audio and edit timings, not estimated from the prompt.

## Status
Production blueprints and per-shot manifests are being added for all 14 Season 1 episodes. Character reference artwork is still to be generated and approved by the creator in ChatGPT before final production.
