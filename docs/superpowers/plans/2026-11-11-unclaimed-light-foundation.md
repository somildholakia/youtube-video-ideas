# The Unclaimed Light Repository Foundation Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Establish a maintainable GitHub source of truth for The Unclaimed Light, including the series bible, nine-season roadmap, character/asset continuity rules, and synchronized script-to-image/audio production templates.

**Architecture:** A channel-first hierarchy contains series-level canon, reusable character/world/ship references, season folders, and episode production packages. Markdown is the human-readable source of truth; CSV manifests carry stable shot/audio IDs and timecodes for downstream editing.

**Tech Stack:** GitHub repository, Markdown, CSV, PNG/JPG reference assets (added as approved), stable textual IDs.

**Spec:** `docs/superpowers/specs/2026-11-11-unclaimed-light-design.md`

## Global Constraints

- Selected creative direction: The Unclaimed Light.
- 9 planned seasons, 14 episodes per season initially.
- Target episode duration: 40–45 minutes; planning target 42:00.
- Shot duration target: 3–5 seconds, default 4 seconds.
- Maximum 80 panels in a single image collage.
- Every collage panel has a neat border and only a small sequence number; no other text or content beyond the story image.
- The canonical script drives both image and audio generation.
- No franchise character, setting, plot, dialogue, visual identity, or music copying.
- Do not claim YouTube compliance guarantees monetization or recommendation.

## Review Focus

- Shot/audio timecodes must remain parseable and stable across episode files.
- Collage batches must never exceed 80 panels.
- Dialogue text must not drift between canonical script and audio manifest.
- Character reference IDs must remain stable across seasons.
- Mature-audience positioning must not be mistaken for a platform age designation or a basis for made-for-kids classification.

---

### Task 1: Repository entry point and channel structure

**Files:**
- Create: `README.md`
- Create: `channels/01-space-stories/README.md`
- Create: `channels/01-space-stories/channel-bible/channel-overview.md`
- Create: `channels/01-space-stories/youtube-guidelines/production-checklist.md`

- [ ] Write a failing structure check by enumerating required paths and checking their presence in the proposed tree.
- [ ] Verify the initial empty repository does not yet contain the required files.
- [ ] Add repository overview, naming conventions, channel purpose, and upload QA checklist.
- [ ] Verify required path list and links are consistent.

### Task 2: Series bible and canon

**Files:**
- Create: `channels/01-space-stories/series/01-the-unclaimed-light/00-series-bible/*.md`

- [ ] Define premise, universe, Lumen Trail rules, timeline, lore, technology, tone, visual language and continuity rules.
- [ ] Establish canon boundaries and a change-log convention.
- [ ] Verify the bible does not depend on existing franchise-specific names or designs.

### Task 3: Character/world/ship continuity system

**Files:**
- Create: `01-characters/README.md`, `character-index.md`, `character-template.md`
- Create: `02-worlds-and-locations/README.md`, `world-template.md`
- Create: `03-spaceships-and-technology/README.md`, `asset-template.md`

- [ ] Define stable IDs, approval status, canonical appearance, voice, image prompt and reference image slots.
- [ ] Define environment and technology records.
- [ ] Verify every new recurring character has a registration path and cannot silently replace an existing ID.

### Task 4: Season roadmap

**Files:**
- Create: `04-seasons/README.md`
- Create: `season-01/season-bible.md`, `episode-guide.md`
- Create: `season-02/...` through `season-09/...` roadmap and episode guide files.

- [ ] Define the nine-season overarching mystery and escalation.
- [ ] Provide 14 distinct episode concepts per season with title, logline, local conflict, character focus, canon reveal, and ending hook.
- [ ] Verify 126 unique episode IDs and titles.

### Task 5: Script, shot, image and audio synchronization standard

**Files:**
- Create: `production-standards/script-format.md`
- Create: `production-standards/image-collage-standard.md`
- Create: `production-standards/audio-sync-standard.md`
- Create: `production-standards/shot-list-template.csv`
- Create: `production-standards/audio-cues-template.csv`
- Create: `production-standards/episode-production-template/...`

- [ ] Define canonical script format, exact dialogue preservation, IDs, timecode format, and audio-event fields.
- [ ] Define collage batches of at most 80 panels with border and sequence-number-only rule.
- [ ] Verify CSV headers, ID examples, and timecode examples are consistent.

### Task 6: Season 1 episode packages

**Files:**
- Create: 14 episode directories with script, shot list, image prompts, continuity and production status.

- [ ] Populate episode-level story beats and production scaffolds.
- [ ] Write complete, timed 40–45-minute scripts sequentially, beginning with Episode 1; never label an outline or condensed draft as a complete 42-minute screenplay.
- [ ] Generate matching shot/audio manifests from each approved script and validate durations and IDs.

### Task 7: Verification and GitHub delivery

- [ ] Check folder paths, all 126 episode entries, unique IDs, CSV schemas, collage maximum, and script/audio references.
- [ ] Review canon continuity and YouTube policy checklist.
- [ ] Commit the completed foundation on the feature branch.
- [ ] Report actual file counts, completed scripts, and remaining production work. Do not merge or publish without separate approval.

