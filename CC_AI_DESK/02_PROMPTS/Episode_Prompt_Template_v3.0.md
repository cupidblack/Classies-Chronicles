# Classies Chronicles — Episode Generation Contract v3.0

**Template ID:** `cc.episode.v3.0`  
**Status:** DEFAULT EPISODE TEMPLATE — FOUNDATION PHASE  
**Purpose:** Generate a traceable, continuity-safe, Chronicle-first Classies Chronicles episode package.

---

## 0. Generation principle

The episode generator must treat the archive as a story-world source system, not as a blank prompt.

**Never silently invent canon.**

Every important claim must be classified as:

- `CONFIRMED_CANON`
- `ARCHIVAL_RECORD`
- `PROPOSED_NEW_CANON`
- `WORKING_INTERPRETATION`
- `SPECULATION`
- `UNKNOWN`

Only `CONFIRMED_CANON` and `ARCHIVAL_RECORD` may be presented as established history.

---

# STEP 1 — Episode identity

Fill:

- episode_id:
- season_id:
- season_title:
- chapter_number:
- chapter_title:
- episode_number:
- episode_title:
- chronicle_title:
- generation_version:
- producer:
- language:
- locale:
- timezone:
- target_chronicle_seconds:
- target_trailer_seconds:
- target_podcast_minutes:

---

# STEP 2 — Episode context resources

Attach or reference:

- `00_CONTEXT_STATUS.json`
- `01_METADATA.json`
- `02_BIBLE_REFERENCE.md`
- `03_COURSE_LESSON_REFERENCE.md`
- `04_CONTINUITY_REFERENCE.md`
- `05_HEADLINES.json`
- `07_STORY_NOTES.md`

Also attach:
- previous episode's approved context;
- previous Chronicle;
- previous trailer;
- previous podcast script/rundown where relevant;
- approved archive references;
- reusable canon references.

---

# STEP 3 — Archive continuity

Required inputs:

- season notes;
- chapter notes;
- previous Classies Chronicles references;
- archive story references;
- character canon;
- technology canon.

Create a continuity table:

| Claim | Source | Classification | Use |
|---|---|---|---|
| ... | ... | ... | ... |

If a bridge is uncertain, flag it instead of inventing it.

---

# STEP 4 — Bible integration

Fill:

- bible_reference:
- selected_passage_or_motif:
- thematic_connection:
- podcast_reflection_seconds:

Rule:
Bible material should inform the story's theme and reflection. It should not be pasted into the Chronicle as artificial exposition.

---

# STEP 5 — Education / course integration

Fill:

- organisation:
- network:
- course:
- lesson:
- learning_objective:
- episode_sequence_position:

For S00E01:
- introduce Koware Group;
- introduce Buzzjuice Network;
- introduce Buzzjuice Courses;
- do not teach the formal Health & Safety lesson;
- reserve registration/orientation primarily for the next episode.

The Chronicle must remain a story rather than an advertisement.

---

# STEP 6 — News integration

Fill:

- requested_date_window:
- actual_retrieval_cutoff:
- locations:
- headline_sources:
- selected_headlines:
- fictional_story_use:

Rules:
1. Never fabricate future news.
2. Never turn real-world allegations into fictional facts.
3. If a real headline inspires a fictional scene, explicitly separate the real report from the fiction.
4. E01 may use no headline if it improves narrative focus.

---

# STEP 7 — Episode narrative contract

Required:

- central_question:
- theme:
- primary_pov:
- beginning_state:
- inciting_event:
- conflict:
- midpoint_turn:
- turning_point:
- partial_resolution:
- ending_hook:
- continuity_anchors:
- educational_element:
- bible_motif:
- real_world_references:
- humour_level:
- mystery_level:

---

# STEP 8 — Chronicle-first rule

Generate in this order:

1. Chronicle brief
2. Chronicle story treatment
3. 200-second Chronicle draft
4. Chronicle QA
5. Producer review
6. Locked Chronicle
7. 20-second trailer derived ONLY from locked Chronicle
8. Podcast rundown
9. Podcast script / discussion package
10. Final production package

Do not generate the trailer independently before the Chronicle is locked.

---

# STEP 9 — Character and power controls

For every unusual ability, record:

- ability:
- current_stage:
- source:
- control_level:
- duration:
- limitation:
- continuity_status:

Never allow a future power to appear as mastered before its canon stage.

Default rule:

> High EduBeam exposure = high power / low control.

> Personal Awareness practice = lower power / higher control.

---

# STEP 10 — Humour

Default Chronicle humour:
- warm;
- observational;
- character-based;
- light slapstick.

Approximately one principal physical-comedy beat per 200-second Chronicle.

Do not use humour to trivialise:
- real-world tragedy;
- serious allegations;
- fear;
- displacement;
- safety incidents.

---

# STEP 11 — AI co-host rules

AI may:
- suggest;
- draft;
- reorganise;
- flag continuity;
- identify missing sources;
- ask the host questions;
- provide concise transitions.

AI may not silently:
- create canon;
- rewrite source history;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish.

The AI co-host is a participant, not the protagonist.

---

# STEP 12 — Podcast structure

Default sequence:

1. Cold Open / Signal
2. Jingle + Welcome
3. Bible reflection
4. Episode / topic overview
5. Brief Chronicle trailer
6. Main podcast discussion
7. Chronicles of Cupid Black
8. Open discussion on topic + Chronicle
9. Community / crowdfunding / participation
10. Next episode preview
11. Invitation to support future seasons
12. Closing mystery
13. Community shorts / credits

---

# STEP 13 — QA gates

### FAIL
- required source missing;
- fabricated news;
- continuity contradiction without explicit approved story reason;
- unapproved canon presented as fact;
- consent issue;
- licensing issue;
- critical narrative element missing;
- Chronicle not approved before trailer/podcast lock.

### WARN
- weak transition;
- weak sensory detail;
- humour too low;
- continuity reference incomplete;
- source provenance incomplete.

---

# STEP 14 — Output manifest

Every run should record:

- template_version;
- generation_timestamp_utc;
- model/provider;
- input source IDs;
- archive scope;
- retrieval cutoff;
- deterministic seed where supported;
- output hashes where practical;
- producer approval state.

---

# STEP 15 — Default episode handoff checklist

Before handing the package to production:

- [ ] Context complete
- [ ] Bible reference complete
- [ ] Course reference complete
- [ ] Headlines verified or marked pending
- [ ] Continuity checked
- [ ] Canon checked
- [ ] Story notes locked
- [ ] Chronicle brief complete
- [ ] 200-second Chronicle drafted
- [ ] Chronicle QA passed
- [ ] Producer review complete
- [ ] Trailer derived from locked Chronicle
- [ ] Podcast rundown complete
- [ ] AI co-host mode selected
- [ ] ENVY/Pavilion communications test complete
- [ ] Narration plan complete
- [ ] Final archive manifest complete
