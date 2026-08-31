# Classies Chronicles — Part Generation Template v1.65.63

**Template ID:** `cc.prompt.v1.65.63`  
**Increment:** +0.00.01 from v1.65.62  
**Purpose:** Generate one narrated Part while preserving episode-level continuity, provenance, canon classification and QA.

## Header

```yaml
template_id: cc.prompt.v1.65.63
template_version_used: v1.65.63
part_id:
episode_id:
season_id:
chapter_id:
generation_timestamp_utc:
prepared_by:
run_variant: Master Optimized | Concise | Safety-Hardened
deterministic_generation_seed:
locale:
timezone:
language:
target_wordcount:
content_hash_expected:
```

## Source bundle

```yaml
episode_context:
season_notes:
chapter_notes:
episode_notes:
part_notes:
bible_reference:
course_lesson_reference:
news_headline_reference:
character_canon:
technology_canon:
previous_episode_resources:
archive_resources:
```

**Purpose:** This consolidates all continuity and provenance inputs into one traceable source bundle.

## Canon classification

Every material story claim must carry one of:
`CONFIRMED_CANON`, `ARCHIVAL_RECORD`, `PROPOSED_NEW_CANON`, `WORKING_INTERPRETATION`, `SPECULATION`, `UNKNOWN`.

## Narrative controls

```yaml
pov:
dates_covered:
location:
scene_goal:
conflict:
turning_point:
emotional_state:
humour_level:
mystery_level:
sensory_tags:
```

## Immutable rules

- Do not silently invent canon.
- Do not fabricate news.
- Do not contradict approved continuity.
- Do not convert fictional technology into real science.
- Do not provide reproducible dangerous self-experimentation.
- Do not override consent or licensing.
- Preserve the requested narrative voice and chronology.

## Output

Return:
1. Part title;
2. narrated prose/script;
3. dialogue;
4. scene cues;
5. SFX/visual notes;
6. canon classification notes;
7. continuity warnings;
8. provenance summary;
9. QA status.

## QA

`FAIL` for missing critical sources, fabricated news, major continuity contradiction or unsafe prohibited content.

`WARN` for optional weakness.

This version intentionally preserves the v1.65.62 architecture while clarifying the consolidated episode-context source bundle and explicit safety/fictionality boundary.
