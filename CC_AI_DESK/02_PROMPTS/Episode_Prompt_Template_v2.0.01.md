# Classies Chronicles — Episode Generation Contract v2.0.01

**Purpose:** Default episode-level prompt contract for producing each Chronicle and the podcast package. This version incrementally refactors v2.0 by adding an explicit source manifest, timeline ledger, canon ledger, news cutoff, safety boundary, and episode-to-episode handoff.

## 1. Episode Identity
```yaml
episode_id: S00E01
season_id: S00
season_title: The Foundation Phase
episode_title: Foundations & Frequencies
chronicle_title: The Signal Before the Story
generation_version: v2.0.01
producer: "Producer / Enka"
language: English
locale: en-GH
timezone: Africa/Accra
```

## 2. Source Manifest
Attach resources in this order:
1. current episode context;
2. current chapter notes;
3. approved Classies archive;
4. character canon;
5. technology canon;
6. Bible reference;
7. course reference;
8. verified headline snapshot;
9. previous episode handoff;
10. production/studio constraints.

For each source record: `source_id`, `path/url`, `authority_class`, `retrieval_date`, `status`.

## 3. Authority and Canon Ledger
Every important claim must be tagged:
- `CONFIRMED_CANON`
- `ARCHIVAL_RECORD`
- `PROPOSED_NEW_CANON`
- `WORKING_INTERPRETATION`
- `SPECULATION`
- `UNKNOWN`

Only the first two may be presented as established history. Proposed canon requires producer approval.

## 4. Timeline Ledger
Record:
- historical event date;
- present-day framing date;
- publication date;
- future/pending dates;
- any deliberate flashback/flash-forward.

Never use a future headline as if it already existed.

## 5. Narrative Contract
Required:
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
- real-world references;
- humour level;
- mystery level.

## 6. Episode-Specific Inputs
```yaml
bible_reference: "Nehemiah 1–7"
course_reference: "Koware Group / Buzzjuice Network / Buzzjuice Courses introduction"
formal_health_safety_lesson: false
chapter_reference: "Pilot Season Chapter 4"
news_window_requested: "2026-08-09 to 2026-10-17"
news_cutoff: "2026-08-31"
news_future_policy: "mark pending; never fabricate"
member_story_inputs: "consented material only"
```

## 7. Story Integration Rule
Bible, education, news and archive material should motivate the story rather than appear as pasted blocks. Real news must remain factually distinct from fictional events.

## 8. Humour Rule
Use warm observational humour and light slapstick. Default to one principal physical-comedy beat in a ~200-second Chronicle. Do not trivialise fear, displacement or serious real-world news.

## 9. AI Intervention Boundary
AI may suggest, draft, reorganise, flag continuity and identify missing sources. AI may not silently create canon, fabricate news, fabricate citations, override consent/licensing or publish.

## 10. Chronicle-First Production Rule
Generate and approve the ~200-second Chronicle before final podcast recording. Derive the ~20-second trailer only from the locked Chronicle.

## 11. Output Package
Generate:
1. story brief;
2. narrative draft;
3. final script;
4. scene list;
5. visual prompt list;
6. audio/SFX list;
7. canon/continuity QA report;
8. 20-second trailer;
9. podcast discussion package;
10. provenance manifest;
11. next-episode handoff.

## 12. QA Gates
**FAIL:** missing critical source; fabricated news; unapproved canon presented as fact; continuity contradiction; consent/licensing failure; missing critical narrative element.

**WARN:** weak transition, optional sensory detail, underdeveloped humour, incomplete continuity reference.

## 13. Next-Episode Handoff
At completion, create a compact handoff containing:
- locked canon created in this episode;
- unresolved mysteries;
- character-state changes;
- technology-state changes;
- unanswered questions;
- approved member hooks;
- references to final media.

This handoff becomes a required resource for the next episode.
