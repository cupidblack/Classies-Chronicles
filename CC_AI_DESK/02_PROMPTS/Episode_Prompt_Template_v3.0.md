# Classies Chronicles — Episode Generation Contract v3.0

**Template ID:** cc.episode.v3.0  
**Purpose:** Default orchestration template for generating each Classies Chronicles episode package.

## 1. How to use

Complete this contract before asking an AI to generate story content.

The episode generator must:

1. read the completed context;
2. retrieve the referenced previous episode and archive;
3. reconcile continuity;
4. classify canon claims;
5. research only available real-world sources;
6. produce the story package;
7. run QA;
8. stop for producer approval before locking new canon.

## 2. Machine-readable header

```yaml
template_id: cc.episode.v3.0
template_version: v3.0
episode_id: S00E01
season_id: S00
episode_title: "Foundations & Frequencies"
chronicle_title: "The Signal Before the Story"
producer: ""
generation_timestamp_utc: ""
locale: en-GH
timezone: Africa/Accra
language: English
generation_mode: creative
retrieval_scope: CURRENT_EPISODE
chronicle_target_seconds: 200
trailer_target_seconds: 20
podcast_target_minutes: "35-45"
producer_approval: false
```

## 3. Episode identity

- Episode ID:
- Season:
- Chapter:
- Episode title:
- Chronicle title:
- Publication target:
- Primary POV:
- Narrative tense:
- Intended audience:

## 4. Story objective

- Main key topic:
- Central question:
- Theme:
- Beginning state:
- Conflict:
- Turning point:
- Resolution/partial resolution:
- Ending hook:
- Humour level:
- Mystery level:

## 5. Source package

### Bible
- File:
- Passage:
- Thematic use:

### Course
- File:
- Lesson/module:
- What is introduced now:
- What must be deferred:

### Headlines
- File:
- Research cutoff:
- Locations:
- Verified headlines:
- Fictionalization policy:

### Continuity
- Previous episode:
- Chapter notes:
- Archive files:
- Character canon:
- Technology canon:

### Previous-episode resources

List exact links/paths to the previous episode's final transcript, Chronicle, trailer, manifest and relevant canon changes.

### Archive resources

Attach/reference the Classies Chronicles archive. The generator must prefer archive evidence over invention.

## 6. Canon control

Every significant new claim must be labelled:

- CONFIRMED_CANON
- ARCHIVAL_RECORD
- PROPOSED_NEW_CANON
- WORKING_INTERPRETATION
- SPECULATION
- UNKNOWN

Only CONFIRMED_CANON and ARCHIVAL_RECORD may be presented as established history.

## 7. Real-world news rule

Never fabricate a headline, date, quotation, statistic, source or event.

If the requested date range extends beyond the research date, mark the future portion **PENDING** and do not invent it.

Real-world reporting must remain distinct from fictional events.

## 8. Narrative integration

Bible, course content, news and archive material should be integrated into the story rather than inserted as disconnected blocks.

The Chronicle remains the primary story artifact.

## 9. Character controls

Check:

- identity chronology;
- personality;
- current ability stage;
- emotional state;
- relationships;
- props;
- recurring phrases;
- unresolved mysteries.

Do not give a character knowledge they have not earned.

## 10. Humour policy

Default:

- warm;
- observational;
- light slapstick;
- approximately one principal physical/comedic beat per ~200-second Chronicle.

Humour must not trivialize serious real-world events.

## 11. AI Desk policy

AI may suggest, draft, reorganize, question and flag.

AI may not silently:

- create permanent canon;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish.

For live podcast use, AI remains silent until explicitly cued.

## 12. Required output package

Generate:

1. episode story brief;
2. Chronicle draft;
3. scene/shot list;
4. narration script;
5. visual prompt list;
6. SFX/music list;
7. Chronicle QA report;
8. 20-second trailer derived only from approved Chronicle;
9. podcast discussion package;
10. episode provenance manifest;
11. canon-change proposal.

## 13. Chronicle-first production gate

Do not treat the podcast as final until the Chronicle is approved.

Pipeline:

**Episode Contract → Story Package → Chronicle → Chronicle QA → Producer Approval → Trailer → Podcast → Final QA → Archive**

## 14. QA

### FAIL
- missing critical source;
- fabricated news;
- continuity contradiction without explicit story reason;
- unsafe actionable technical instructions;
- missing consent/licensing;
- missing critical narrative elements.

### WARN
- weak transition;
- weak humour;
- incomplete provenance;
- unclear character motivation;
- excessive exposition.

## 15. Producer approval block

```yaml
story_approved: false
chronicle_approved: false
trailer_approved: false
podcast_approved: false
canon_changes_approved: false
publication_approved: false
approval_notes: ""
```
