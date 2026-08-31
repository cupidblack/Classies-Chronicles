# Classies Chronicles — Episode Generation Contract v2.1

**Template ID:** cc.episode.v2.1  
**Status:** DEFAULT EPISODE-LEVEL TEMPLATE  
**Purpose:** Prepare a complete episode story package before Part/scene generation.

## 0. Operating principle

The generator must follow:

**Retrieve → Validate → Reconcile → Story Contract → Generate → QA → Approve → Produce**

AI is an editorial assistant, not the final authority.

## 1. Episode identity

Fill:

```yaml
episode_id:
season_id:
season_title:
chapter_id:
chapter_title:
episode_number:
episode_title:
chronicle_title:
generation_version:
producer:
language:
locale:
timezone:
target_chronicle_seconds: 200
target_trailer_seconds: 20
target_podcast_minutes: 35-45
publication_target: ASAP
```

## 2. Episode context

Provide:

- current episode context file
- metadata
- Bible reference
- course reference
- continuity reference
- headlines
- story notes
- production checklist

## 3. Retrieval resources

Attach or retrieve, in this order:

### Required
1. Previous approved episode package, if one exists.
2. Current season/chapter notes.
3. Relevant archive story files.
4. Character canon.
5. Technology/world canon.
6. Current episode context.

### Optional
- prior trailers
- prior podcast transcript
- visual style references
- approved community contributions
- approved participant material

### Retrieval scope

Default:

`CURRENT_EPISODE`

Expand only when explicitly requested:

`CURRENT_SEASON`
`ALL_APPROVED_EPISODES`
`GLOBAL_CHRONICLES`

Never silently broaden scope.

## 4. Source contract

Every source must have:

```yaml
source_id:
source_type:
title:
version_or_date:
authority:
permission_status:
publication_status:
notes:
```

Valid source classes:

- BIBLE_REFERENCE
- COURSE_REFERENCE
- HEADLINE
- CONTINUITY
- CHARACTER_CANON
- TECHNOLOGY_CANON
- STORY_NOTE
- PREVIOUS_EPISODE
- COMMUNITY_CONTRIBUTION

## 5. Canon contract

Classify important claims:

- CONFIRMED_CANON
- ARCHIVAL_RECORD
- PROPOSED_NEW_CANON
- WORKING_INTERPRETATION
- SPECULATION
- UNKNOWN

Rules:

- Only CONFIRMED_CANON and ARCHIVAL_RECORD may be presented as established history.
- PROPOSED_NEW_CANON requires producer approval before becoming permanent.
- WORKING_INTERPRETATION must remain identifiable as interpretation.
- UNKNOWN is allowed and often desirable.

## 6. Narrative contract

Required:

```yaml
central_question:
theme:
primary_pov:
beginning_state:
conflict:
turning_point:
partial_resolution:
ending_hook:
continuity_anchors:
educational_element:
real_world_references:
humour_level:
mystery_level:
```

A valid Chronicle must remain a story. Bible, education and news elements must support the story rather than appear as unrelated inserts.

## 7. Chronology gate

Before generation:

1. identify the last confirmed event;
2. identify the next confirmed event;
3. place the episode between them;
4. list unresolved continuity questions;
5. prohibit invented bridges unless explicitly approved.

If chronology is uncertain, flag it.

## 8. Headline freshness gate

Never fabricate future news.

The headline file must include:

```yaml
as_of:
publication_cutoff:
requested_window:
usable_verified_window:
future_window_status:
```

If the requested window extends beyond today's date, only the verified portion may be used.

Refresh the headline file before publication if the episode is delayed.

## 9. Chronicle-first production gate

The Chronicle is created first.

Pipeline:

```text
Episode Context
    ↓
Story Contract
    ↓
Chronicle Brief
    ↓
200-second Chronicle Script
    ↓
Narration
    ↓
Visuals + SFX
    ↓
Chronicle QA
    ↓
Producer Approval
    ↓
20-second Trailer
    ↓
Podcast Recording
    ↓
Podcast Edit
```

The final podcast programme must not be locked before the Chronicle is approved.

## 10. Duration gate

For a 200-second Chronicle:

- target narration: approximately 480–530 words
- adjust according to actual narrator pace
- do not use a 2,400–2,600-word script for a 200-second target

For a 20-second trailer:

- target approximately 45–55 spoken words
- use only material derived from the approved Chronicle

## 11. Humour policy

Default:

- warm
- observational
- light slapstick
- one principal physical/comedic beat per ~200-second Chronicle

Do not use humour to trivialize:

- death
- serious crime
- disasters
- abuse
- real-world victims

## 12. Community contribution gate

If member content is used:

```yaml
member_id:
content_id:
consent_status:
consent_scope:
publication_permission:
credit_preference:
withdrawal_status:
```

No consent = no narrative use.

Withdrawal of consent must remove the material from future processing.

## 13. AI participation contract

AI modes:

- LISTEN — silent
- ASSIST — responds when prompted
- CO-HOST — participates within episode boundaries
- AUTONOMOUS_PROPOSAL — may suggest, never publish

AI may:

- suggest
- draft
- reorganize
- flag continuity issues
- identify missing sources
- generate alternative scenes

AI may not silently:

- create canon
- fabricate news
- fabricate sources
- override consent
- override licensing
- publish

## 14. Output package

Generate:

1. episode story brief
2. story notes
3. narrative draft
4. 200-second script
5. scene list
6. visual prompt list
7. audio/SFX list
8. canon-change report
9. QA report
10. 20-second trailer derived from approved Chronicle
11. podcast discussion package
12. provenance manifest

## 15. QA

### FAIL

- fabricated news
- missing critical source
- chronology contradiction without approval
- missing consent
- invalid licensing
- Chronicle duration grossly outside target
- trailer not derived from approved Chronicle
- new canon silently promoted to fact

### WARN

- weak transition
- weak humour
- incomplete continuity reference
- optional visual detail missing

## 16. Provenance

Record:

```yaml
template_version:
model_provider:
generation_timestamp_utc:
source_ids:
retrieval_scope:
producer:
approval_state:
output_hash:
```

## 17. Default E01 values

```yaml
episode_id: S00E01
episode_title: Foundations & Frequencies
chronicle_title: The Signal Before the Story
bible_reference: Nehemiah 1-7
course_reference: Buzzjuice Network / Courses introduction
formal_health_safety_lesson: false
primary_theme: signal, discernment, responsibility
primary_pov: Cupid Enka
chronicle_target_seconds: 200
trailer_target_seconds: 20
podcast_target_minutes: 35-45
```

## 18. Default review question

Before approval, ask:

> Does this episode make the audience want the next episode without pretending to have answered questions that the canon intentionally leaves open?
