# Classies Chronicles — Episode Generation Contract v3.0

## Purpose

This is the episode-level orchestration contract.

It sits above the existing Part/Scene generation prompt and prepares the story package that feeds detailed generation.

Pipeline:

Episode Contract
→ Source Validation
→ Story Package
→ Part/Scene Contract
→ Media Generation
→ Chronicle
→ QA
→ Trailer
→ Podcast.

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

Required:

- central question;
- theme;
- primary POV;
- beginning state;
- conflict;
- turning point;
- resolution/partial resolution;
- ending hook;
- continuity anchors;
- educational element;
- real-world references;
- humour level;
- mystery level;
- emotional arc.

## 3. Source Contract

Required source classes where applicable:

- Bible/reference;
- approved course/education source;
- approved current headline(s);
- approved continuity references;
- approved character canon;
- approved technology canon;
- producer story notes.

The generator must never invent a missing source.

## 4. Canon Policy

Every important claim is classified:

- CONFIRMED_CANON
- ARCHIVAL_RECORD
- PROPOSED_NEW_CANON
- WORKING_INTERPRETATION
- SPECULATION
- UNKNOWN

Only CONFIRMED_CANON and ARCHIVAL_RECORD may be presented as established history.

PROPOSED_NEW_CANON requires producer approval.

## 5. News Policy

Real news must be:

- current;
- verified;
- stored in 05_HEADLINES.json;
- cited in the production provenance;
- clearly distinguished from fictional material.

Never fabricate a headline, publisher, URL, quotation or event.

A real headline may inspire a fictional parallel, but the Chronicle must never imply that a fictional character caused or solved the actual real-world event unless that statement is clearly framed as fiction.

## 6. Intervention Policy

AI may:

- suggest;
- draft;
- reorganize;
- identify continuity problems;
- identify missing sources;
- propose new canon.

AI may not silently:

- create canon;
- rewrite source history;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish.

## 7. Humour Policy

Default:

- warm;
- observational;
- light slapstick;
- one principal physical/comedic beat per approximately 200-second Chronicle.

Humour must not trivialize serious real-world reporting.

## 8. Chronicle-First Rule

The approximately 200-second Chronicle must be completed and producer-approved before final podcast recording.

The approximately 20-second trailer must be derived from the approved Chronicle.

## 9. Output Package

Generate:

1. story brief;
2. narrative draft;
3. script;
4. scene list;
5. visual prompt list;
6. audio/SFX list;
7. Chronicle QA report;
8. 20-second trailer;
9. podcast discussion package;
10. provenance manifest.

## 10. Determinism and Audit

Record:

- template version;
- model/provider;
- timestamp;
- source IDs;
- retrieval scope;
- deterministic seed where supported;
- output hash where practical;
- producer approval state.

## 11. QA

FAIL when:

- required source is missing;
- real news is fabricated;
- continuity is contradicted without explicit story reason;
- restricted content is used;
- consent is missing;
- licensing is invalid;
- critical narrative elements are absent.

WARN when:

- optional sensory detail is weak;
- transitions are weak;
- humour is underdeveloped;
- continuity references are incomplete.

## 12. Producer Acceptance Gate

No generated story becomes canon merely because it passes AI QA.

AI QA confirms compliance.

Producer approval confirms story authority.

## 13. Relationship to Part Template

The existing `Episode_Prompt_Template.txt` remains the detailed Part/Scene contract.

This file does not replace it.
