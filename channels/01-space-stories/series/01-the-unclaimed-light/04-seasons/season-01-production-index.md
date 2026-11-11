# Season 1 Production Pack — The First Coordinate

Entry point for the Season 1 episode production files.

## Production structure
- 14 episodes.
- 8 sequences per episode, each 5:20.
- 8 beats per sequence, each 40 seconds.
- 10 shots per beat at four seconds each.
- 640 planned shots and a 42:40 assembly target per episode.

## Episode folder contents
Each episode folder contains:
- `script.md` — timed visual production draft, sequence beats, key dialogue and continuity rules.
- `shot-list.csv` — 640 stable shot IDs, in/out timecodes and per-panel image prompts.
- `audio-cues.csv` — 64 ambience cues, 16 dialogue cues and 8 sequence SFX cues, linked to the shot timeline.

## ChatGPT collage rule
Generate each sequence as **one separate image** containing **exactly 80 panels** in a 10-column × 8-row grid. All panels equal-sized, in reading order and separated by visible borders. Each panel shows only the story image plus one small sequence number; the sequence number is the only text allowed. No captions, dialogue, subtitles, titles, labels, logos, watermarks, UI, pseudo-writing, decorative filler or unrelated content. One collage per generation request.

The CSV's panel numbers 001–080 map to global shot IDs. Attach approved character, ship and location references. Reject a sheet if any panel is missing, merged, duplicated, illegible or inconsistent. Image models may fail at this density; if so, split the sequence into smaller grids without changing the global shot IDs. Do not claim a failed collage contains 80 usable panels.

## Generation order
1. Generate and approve character references and the Wayfarer model reference.
2. Generate location references.
3. Generate one collage at a time in ChatGPT using the relevant script sequence and shot CSV.
4. Inspect the exact panel count, sequence order, borders, unwanted text and continuity.
5. Generate audio from exact dialogue and cue-sheet descriptions.
6. Assemble and conform the timeline to measured audio; verify 40–45 minutes.

## Status
The text production packs are committed. Character artwork, location artwork, generated collages, voice renders, final mixes and finished videos are not yet generated.
