# Classies Chronicles — Episode Generation Contract v3.0

## Purpose

Episode-level orchestration contract for building the story package before Part/scene generation.

The pipeline is:

**EPISODE CONTEXT → SOURCE RETRIEVAL → CONTINUITY CHECK → STORY PACKAGE → CHRONICLE → QA → TRAILER → PODCAST → ARCHIVE**

## 1. Episode identity

Required:
- episode_id
- season_id
- chapter_id/title
- episode_title
- chronicle_title
- generation_version
- producer
- language
- locale
- target duration

## 2. Narrative contract

Every Chronicle must define:
- central question;
- theme;
- POV;
- beginning state;
- conflict;
- turning point;
- resolution/partial resolution;
- ending hook;
- continuity anchors;
- educational element;
- real-world references;
- humour level;
- mystery level.

## 3. Source contract

Required source classes where applicable:
- Bible/reference;
- approved course source;
- approved current headline;
- continuity archive;
- character canon;
- technology canon;
- producer story notes;
- previous approved episode.

Never invent a source to fill a field.

## 4. Canon classification

Every important claim must be classed:
- CONFIRMED_CANON
- ARCHIVAL_RECORD
- PROPOSED_NEW_CANON
- WORKING_INTERPRETATION
- SPECULATION
- UNKNOWN

Only confirmed/archival material may be presented as established history.

Proposed new canon requires producer approval.

## 5. Episode context entry

Fill these before generation:

```yaml
episode:
  id:
  season:
  chapter:
  title:
  chronicle_title:
  target_duration:
  primary_location:
  timeframe:

narrative:
  central_question:
  theme:
  pov:
  beginning_state:
  conflict:
  turning_point:
  resolution:
  ending_hook:
  humour_level:
  mystery_level:

sources:
  bible:
  course:
  headlines:
  continuity:
  character_canon:
  technology_canon:
  previous_episode:
  archive_bundle:

production:
  host:
  voice_actor:
  ai_cohost:
  guests:
  studio_status:
  consent_status:
  licensing_status:

approval:
  story_package:
  chronicle:
  trailer:
  podcast:
```

## 6. Previous-episode resources

Attach:
- previous approved Chronicle;
- previous approved trailer;
- previous continuity reference;
- previous episode metadata;
- unresolved questions.

If there is no previous episode, explicitly state `FOUNDATION_PHASE_START`.

## 7. Archive resources

Attach relevant archive files only. Do not flood the generation context with unrelated archives.

The archive is evidence, not permission to invent.

## 8. News policy

- Retrieve fresh news when publication is near.
- Never fabricate future-dated headlines.
- Separate factual reporting from fictional adaptation.
- Do not attribute real-world crimes or disasters to fictional characters as fact.
- Preserve source/date/provenance.

## 9. Humour

Default:
- warm;
- observational;
- light slapstick;
- approximately one principal physical-comedy beat per ~200-second Chronicle.

Humour must not trivialize serious real-world events.

## 10. AI intervention policy

AI may:
- suggest;
- draft;
- reorganize;
- identify missing sources;
- flag continuity;
- ask questions;
- assist as co-host.

AI may not silently:
- create canon;
- rewrite source material;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish.

## 11. Chronicle-first gate

The approximately 200-second Chronicle must be approved before:
- final trailer;
- final podcast recording.

The 20-second trailer must be derived from the locked Chronicle.

## 12. Output package

Generate:
1. story brief;
2. context package;
3. narrative draft;
4. scene/part plan;
5. script;
6. visual/audio notes;
7. Chronicle QA;
8. 20-second trailer;
9. podcast discussion package;
10. provenance manifest.

## 13. QA

FAIL if:
- required source is missing;
- real news is fabricated;
- continuity is contradicted without approval;
- restricted content appears;
- consent is missing;
- licensing is invalid;
- critical narrative elements are absent.

WARN if:
- transitions are weak;
- humour is underdeveloped;
- sensory detail is weak;
- continuity needs clarification.

## 14. Determinism / audit

Record:
- template version;
- generation timestamp;
- model/provider;
- source IDs;
- retrieval scope;
- seed where supported;
- output hash where practical;
- approval state.

## 15. Part-generation compatibility

The Part template remains the detailed scene/Part contract. This document prepares the episode package that feeds it.
