# Classies Chronicles — Episode Generation Contract v2.0

## Purpose

This is the episode-level orchestration contract.

The existing Part Generation Prompt remains the detailed scene/Part contract. This document sits above it and prepares the story package that feeds the Part generator.

## 1. Episode Identity

Required:
- episode_id
- season_id
- episode_title
- chronicle_title
- generation_version
- producer
- language
- locale

## 2. Narrative Contract

Every Chronicle must define:
- central question;
- theme;
- primary POV;
- beginning state;
- conflict;
- turning point;
- resolution or partial resolution;
- ending hook;
- continuity anchors;
- educational element;
- real-world references;
- humour level;
- mystery level.

### Critical elements

Missing a critical element = FAIL.

### Non-critical elements

Missing a non-critical element = WARN.

## 3. Source Contract

Required source classes:
- Bible/reference;
- approved course/education source;
- approved current headline(s), where used;
- approved continuity references;
- approved character canon;
- approved technology canon;
- producer story notes.

The generator must not invent a source merely to fill a field.

## 4. Canon Policy

Each important claim must be classed as:
- CONFIRMED_CANON
- ARCHIVAL_RECORD
- PROPOSED_NEW_CANON
- WORKING_INTERPRETATION
- SPECULATION
- UNKNOWN

Only CONFIRMED_CANON and ARCHIVAL_RECORD may be presented as established history.

PROPOSED_NEW_CANON requires producer approval before becoming permanent.

## 5. Intervention Policy

AI may:
- suggest;
- draft;
- reorganize;
- flag continuity issues;
- identify missing sources.

AI may not silently:
- create new canon;
- rewrite a source;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish.

## 6. Thematic Content Policy

Bible, education, news and story motifs should be integrated naturally.

They should not become separate blocks that feel mechanically inserted.

The Chronicle must remain a story.

## 7. Humour Policy

Default:
- warm;
- observational;
- light slapstick;
- one principal physical/comedic beat per approximately 200-second Chronicle.

Humour must not destroy suspense or trivialize serious real-world news.

## 8. Continuity Policy

Use retrieved archive references.

If continuity is uncertain:
- flag it;
- do not invent a bridge.

## 9. Output Package

Generate:
1. story brief;
2. narrative draft;
3. script;
4. scene list;
5. visual prompt list;
6. audio/SFX list;
7. Chronicle QA report;
8. 20-second trailer derived from the approved Chronicle;
9. podcast discussion package;
10. provenance manifest.

## 10. Chronicle-First Rule

The podcast must not be recorded as final programme content until the approximately 200-second Chronicle is approved.

The 20-second trailer is derived from the finished Chronicle.

## 11. Determinism and Audit

Every generation run should record:
- template version;
- model/provider;
- timestamp;
- input source IDs;
- retrieval scope;
- deterministic seed where supported;
- output hash where practical;
- producer approval state.

## 12. QA

FAIL if:
- required source is missing;
- real news is fabricated;
- continuity is contradicted without an explicit story reason;
- restricted content is used;
- consent is missing where required;
- licensing is invalid for intended distribution;
- critical narrative elements are absent.

WARN if:
- optional sensory detail is weak;
- a scene could use stronger transition;
- humour is underdeveloped;
- a continuity reference is incomplete.

## 13. Relationship to Existing Part Template

The existing `Episode_Prompt_Template.txt` remains the detailed Part-generation contract.

This episode-level contract does not replace it.

Pipeline:

Episode Contract
→ Story Package
→ Part/Scene Contract
→ Media Generation
→ Chronicle
→ QA
→ Trailer
→ Podcast.
