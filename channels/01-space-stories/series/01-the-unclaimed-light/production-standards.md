# Production Standards: Script → ChatGPT Images + Audio

Each episode uses a canonical timed visual production draft as its common source for images and audio. Target runtime is 42:40 (acceptable 40:00–45:00): 8 sequences × 5:20, 64 beats × 40 seconds and 640 planned shots × 4 seconds.

## ChatGPT collage target: 80 panels per single image
For each sequence, generate **one separate single image containing exactly 80 story panels** in a strict 10-column × 8-row grid. Panels are equal-sized, numbered 001–080 in reading order and separated by clean visible borders/gutters. Each panel contains only its story image and one small sequence number. The number is the only permitted text. No captions, dialogue, subtitles, titles, descriptions, labels, logos, watermarks, UI, pseudo-text, decorative filler or unrelated content. One collage per generation request; never combine batches.

Attach approved character, ship and location reference images. The shot-list CSV is the panel-level prompt source. Reject missing, duplicated, merged, illegible or continuity-breaking panels. Image generation may fail to honour an 80-cell grid; if so, split the batch into smaller grids and retain the global shot IDs. Never report a malformed contact sheet as a valid 80-panel collage.

## Audio
Audio IDs use S##E##-AU###. Cue sheets contain timed dialogue, ambience and sequence-specific SFX. Dialogue must match the screenplay exactly. Voice identities should match approved voice references. Measure generated audio duration and conform the edit; timecodes are targets, not proof of final runtime. Expand the current timed visual drafts into dialogue-dense actor-ready scripts before treating them as final recording scripts.

## Continuity and rights
Stable character, ship, location, prop and technology IDs are permanent. Approved refs override improvised descriptions. Track wardrobe, injuries, props, damage, weather, lighting, geography, gravity, screen direction, knowledge and relationships. Use original scripts/assets or documented permissions. Check current YouTube monetisation, altered/synthetic content and made-for-kids requirements before release.
