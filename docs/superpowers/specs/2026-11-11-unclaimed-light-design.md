# The Unclaimed Light — Series Production System Design

**Date:** 2026-11-11  
**Status:** Proposed for approval  
**Repository:** `somildholakia/youtube-video-ideas`  
**Branch:** `feat/unclaimed-light-series-foundation`

## Intent

Establish the first original, long-running space-exploration series in the YouTube Video Ideas repository. The repository is the canonical source of truth for channel identity, series canon, characters, locations, season arcs, episode scripts, image-generation instructions, audio-generation instructions, and production status.

The selected creative direction is **Approach A — The Unclaimed Light**: an original mature-audience science-fiction adventure about an exploration crew following a changing map encoded in gravitational pathways called Lumen Trails. The series uses the broad, non-proprietary appeal of wonder-filled space exploration and a long cosmic journey; it does not reuse protected characters, settings, plots, names, designs, dialogue, music, or signature elements from the cited inspirations.

## Goals

- Create a scalable channel → series → shared character/world bible → season → episode repository hierarchy.
- Establish nine planned seasons, each initially containing 14 episodes, with room to expand.
- Preserve character and world continuity through stable IDs and approved reference images.
- Write scripts with enough visual and audio detail for separate image and audio generation from the same canonical script.
- Make every spoken line, narration passage, sound effect, music cue, and visual shot independently identifiable and synchronizable.
- Batch visual generation into collages of no more than 80 panels per collage.
- Keep the eventual YouTube release original, viewer-focused, and compliant with applicable platform policies.

## Non-goals

- No imitation of Miles from Tomorrowland, Doraemon, or any other existing franchise.
- No claim that a generated collage automatically produces 80 usable, consistent images; generated panels must be inspected and, when needed, regenerated individually.
- No automatic uploading or publishing to YouTube.
- No guarantee of monetization, recommendation, or audience classification.

## Canon decisions

- Working title: **The Unclaimed Light**.
- Genre: space exploration, science-fiction mystery, adventure, psychological and ethical drama.
- Audience target: mature general audience; creative target approximately 16+, not a YouTube age designation.
- Initial plan: 9 seasons × 14 episodes = 126 episodes.
- Target episode runtime: 40–45 minutes; production target 42 minutes.
- Season 1 title: **The First Coordinate**.
- Core premise: a civilian exploration vessel maps unstable gravitational corridors called Lumen Trails. A signal embedded in a seemingly empty system changes after each jump and reveals new coordinates.
- Tone: cinematic wonder, intelligent suspense, emotional consequences, moral ambiguity, occasional dry humour, non-gratuitous peril.
- Every episode resolves a local dramatic question while advancing or complicating the season/series mystery.

## Production architecture

The repository will use `channels/<channel>/series/<series>/` with:
- `00-series-bible/`: premise, universe, chronology, lore, technology, visual style, continuity.
- `01-characters/`: stable character IDs, canonical profile, appearance, voice, reference prompts and approved images.
- `02-worlds-and-locations/`: canonical environment records and reference assets.
- `03-spaceships-and-technology/`: ship, props, devices and technology records.
- `04-seasons/season-XX/`: season bible, 14-episode guide, episode directories.
- `05-production-assets/`: approved music, sound, thumbnails and shared assets.
- Channel-level guidance and upload policy references live outside the series folder.

Each episode folder contains:
- `script.md`: canonical timed screenplay and all source-of-truth cues.
- `shot-list.csv`: one row per shot, stable shot ID, timing, duration, image prompt, cast, location, and linked audio cues.
- `image-prompts.md`: grouped image-generation batches and negative constraints.
- `audio-cues.csv`: exact spoken text, speaker, delivery, time range, SFX/music and mix notes.
- `continuity.md`: facts introduced, changed, or carried forward.
- `production-status.md`: writing, image, audio, edit, QA and release gates.

## Script-to-image and script-to-audio synchronization

The canonical script is the single source for both modalities. Never independently rewrite dialogue in the image or audio brief.

Every visual shot receives a stable identifier such as `S01E01-SH001`. Every spoken/audio event receives a stable identifier such as `S01E01-AU001`. Scripts include:
- absolute episode timecode in `HH:MM:SS.mmm`;
- shot in/out and duration;
- exact dialogue/narration text, speaker ID, delivery, pronunciation notes for invented terms, and pause intent;
- audio-event in/out, type (dialogue, narration, SFX, ambience, music), asset/voice ID, level/mix intent and transition;
- visual action, composition, lens/camera movement, lighting, environment, character IDs, screen direction, and emotional intent;
- explicit links between shot IDs and audio cue IDs.

Target runtime is 42:00. Shot durations are normally 3–5 seconds, default 4 seconds. This yields roughly 504–840 shots; around 630 at the default. Longer holds are allowed only when deliberately justified and flagged as exceptions rather than silently violating the standard.

For robust alignment, dialogue should be written in short, performable units with pauses and breaths marked. The audio-generation process should return actual clip durations; the editor conforms picture timing to the measured audio while preserving shot-duration intent. Timecodes in the script are a locked editorial blueprint, not a substitute for checking generated speech duration.

## Collage generation rule

**Hard limit: no more than 80 image panels in one generated collage.** Split a larger episode into numbered batches (for example, 001–080, 081–160, etc.). Never request 81 or more panels in one collage.

Each collage must:
- use equal-sized panels in a clean, consistent grid;
- separate every panel with a clearly visible, neat border/gutter;
- show only the relevant story image inside each panel;
- include only a small sequence number as the panel's reference label;
- contain no captions, dialogue, subtitles, titles, logos, watermarks, explanatory text, UI, decorative story-irrelevant elements, or extra labels;
- preserve character, costume, prop, location, lighting and screen-direction continuity.

The sequence number is a production reference, not part of the fictional scene. The image prompt for each panel must be derived from its corresponding shot in the canonical script. For a collage with 80 panels, the sequence numbers are 001–080 within that batch; the manifest maps them to global shot IDs. If legibility or consistency degrades at 80 panels, reduce the batch size rather than sacrificing quality. Inspect panels individually and regenerate failures.

## YouTube publishing guardrails

- Create original scripts, visuals, voice performances, music and sound design, or use assets with documented rights and licenses.
- Avoid repetitive, mass-produced or minimally varied episodes; each episode needs meaningful original narrative and editing.
- Review current YouTube policies before publishing, including Community Guidelines, advertiser-friendly content, copyright, privacy, child safety and altered/synthetic-content disclosure.
- Use YouTube's altered/synthetic disclosure when required for realistic content that could mislead viewers; do not assume every obviously fantastical animation needs the same treatment.
- Audience designation is based on actual intended audience and content, not merely on the fact that the work is animated. Do not mark content as made for kids unless it is actually directed to children.
- Do not promise monetization or a specific age rating.

## Approaches considered

1. **The Unclaimed Light (selected):** a connected cosmic mystery with independent planetary stories. Best balance of episodic variety, long-form continuity and original mythology.
2. **The Thousand Worlds Route:** more episodic planet-of-the-week travel; easier to expand but less distinctive as a long arc.
3. **Beyond the Frontier:** harder science-fiction survival and political conflict; strong mature tone but less emphasis on cosmic wonder.

## Delivery phases

1. Repository foundation, canon bible and production templates.
2. Main cast, ship, locations and visual reference system.
3. Nine-season macro arc and 14-episode guide for each season.
4. Season 1 full screenplays, delivered and reviewed episode by episode.
5. Per-episode shot lists, collage manifests, image prompts and audio cue sheets.
6. Continuity QA, rights/policy review, edit and upload package.

## Decisions left to the builder

Use Markdown for narrative source files and CSV for cue manifests. Keep the canonical script readable for a director and the cue files machine-friendly for editors. Use stable IDs and avoid duplicated dialogue text drifting between files; generated cue sheets must be reconciled to the script before production.
