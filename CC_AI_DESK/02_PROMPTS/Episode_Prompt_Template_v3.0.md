# Classies Chronicles — Episode Generation Contract v3.0

**Template ID:** `cc.episode.v3.0`  
**Status:** DEFAULT EPISODE GENERATION CONTRACT  
**Last updated:** 2026-08-31

## Purpose

This is the authoritative episode-level orchestration contract. It prepares a complete episode package before detailed scene/Part generation.

The default pipeline is:

`EPISODE CONTEXT → RETRIEVE SOURCES → CONTINUITY CHECK → STORY PACKAGE → CHRONICLE → QA → TRAILER → PODCAST → ARCHIVE`

## 1. Episode identity

Required fields:

- `episode_id`
- `season_id`
- `chapter_id`
- `episode_title`
- `chronicle_title`
- `generation_version`
- `producer`
- `language`
- `locale`
- `timezone`
- `target_chronicle_duration`
- `target_podcast_duration`

## 2. Episode context inputs

Attach or reference:

1. `00_CONTEXT_STATUS.json`
2. `01_METADATA.json`
3. `02_BIBLE_REFERENCE.md`
4. `03_COURSE_LESSON_REFERENCE.md`
5. `04_CONTINUITY_REFERENCE.md`
6. `05_HEADLINES.json`
7. `07_STORY_NOTES.md`
8. previous approved episode resources;
9. relevant archive chapters;
10. reusable character/technology canon;
11. approved community/member contributions where consent permits.

## 3. Narrative contract

Every Chronicle must define:

- central question;
- theme;
- primary POV;
- beginning state;
- conflict;
- turning point;
- partial resolution;
- ending hook;
- continuity anchors;
- educational element;
- Bible/reference motif;
- approved real-world headline motifs, if used;
- humour level;
- mystery level;
- emotional arc.

## 4. Source contract

Required source classes where applicable:

- Bible/reference;
- approved course/education source;
- verified current headline(s);
- approved continuity references;
- approved character canon;
- approved technology canon;
- producer story notes;
- consented community/member contributions.

The generator must never invent a source merely to fill a field.

## 5. Canon policy

Every significant claim must be classified:

- `CONFIRMED_CANON`
- `ARCHIVAL_RECORD`
- `PROPOSED_NEW_CANON`
- `WORKING_INTERPRETATION`
- `SPECULATION`
- `UNKNOWN`

Only the first two may be presented as established history without qualification.

## 6. News integrity policy

- Never fabricate a headline, date, source, quotation or event.
- A real headline may inspire a fictional Chronicle event, but the fiction must be recognizable as fiction.
- Do not claim Cupid caused or solved a real-world event unless an explicitly fictional framing is used.
- Future dates must be marked `PENDING` rather than filled with invented news.
- Serious real-world tragedies must not be trivialized with slapstick.

## 7. Community and consent policy

Member participation can influence stories only when the member has an active, explicit consent state for Chronicle use.

Consent must gate retrieval/indexing as well as final publication.

If consent is withdrawn, the person's Chronicle source should be removed from the active retrieval set and no new story should be generated from it.

## 8. Humour policy

Default tone:

- warm;
- observational;
- light slapstick;
- one principal physical/comedic beat in an approximately 200-second Chronicle.

Humour must release tension without destroying suspense or making serious subjects trivial.

## 9. AI intervention policy

AI may:

- research;
- retrieve;
- suggest;
- draft;
- reorganize;
- identify continuity issues;
- propose story alternatives;
- assist the live discussion within the selected co-host mode.

AI may not silently:

- create new canon;
- rewrite a source;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish;
- convert speculation into fact.

## 10. AI co-host mode switch

Every podcast run must declare one:

- `CONTROLLED` — AI contributes only within the producer-defined prompt and topic boundaries.
- `OPEN_ASSIST` — AI may reasonably respond and contribute to the discussion while still respecting safety, consent, licensing and factuality rules.
- `OFFLINE` — no live AI contribution; pre-recorded or edited AI material may still be used.

The mode can be changed by the producer during production.

## 11. Continuity protocol

1. Retrieve the previous approved episode.
2. Retrieve relevant archive chapters.
3. Retrieve character and technology canon.
4. Build a continuity ledger.
5. Mark conflicts.
6. Resolve only conflicts supported by higher-authority evidence.
7. If uncertain, flag rather than invent.

## 12. Chronicle-first gate

The final production sequence is:

1. Story brief
2. Narrative draft
3. Script
4. Scene list
5. Visual/audio plan
6. Chronicle draft
7. Chronicle QA
8. Producer approval
9. 20-second trailer derived from approved Chronicle
10. Podcast recording
11. Podcast edit/QA
12. Archive

The podcast must not be treated as final programme content before Chronicle approval.

## 13. Required output package

Generate:

1. `CHRONICLE_BRIEF.md`
2. `CHRONICLE-200s-DRAFT.txt`
3. `TRAILER-20s-DRAFT.txt`
4. `SCENE_AND_VISUAL_PLAN.md`
5. `AUDIO_SFX_PLAN.md`
6. `CHRONICLE_QA_REPORT.md`
7. `PODCAST_DISCUSSION_PACKAGE.md`
8. `PROVENANCE_MANIFEST.json`
9. updated episode context
10. production checklist/workflow updates

## 14. Generation audit

Record:

- template version;
- model/provider;
- timestamp;
- source IDs;
- retrieval scope;
- consent scope;
- generation mode;
- AI co-host mode;
- producer approval state;
- output hashes where practical.

## 15. Default episode input form

```yaml
episode_id: S00E01
season_id: S00
chapter_id: CH04
episode_title: Foundations & Frequencies
chronicle_title: The Signal Before the Story
central_question: "How do we build a trustworthy foundation when knowledge, technology and perception exceed our control?"
theme: "Power, knowledge and responsibility"
primary_pov: Cupid Enka
bible_reference: Nehemiah 1-7
course_reference: Buzzjuice Network and Buzzjuice Courses introduction
headline_window: "2026-08-09 through 2026-10-17"
headline_status: "verified-to-current-date; future portion pending"
humour_level: light
mystery_level: high
ai_cohost_mode: CONTROLLED
chronicle_target_seconds: 200
podcast_target_minutes: 35-45
producer_approval: PENDING
```
