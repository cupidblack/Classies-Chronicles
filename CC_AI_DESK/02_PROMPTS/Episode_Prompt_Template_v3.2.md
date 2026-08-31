# Classies Chronicles — Episode Generation Contract v3.2

## Purpose
This is the canonical episode-level orchestration contract. It prepares an episode package that feeds the existing detailed Part/Scene generation contract.

**Pipeline:**

`Episode Contract → Source/Continuity Preflight → Story Package → Part/Scene Contract → Chronicle → QA → Trailer → Podcast → Archive`

## A. Episode identity
Required:
- episode_id
- season_id/title
- chapter_id/title
- episode_title
- chronicle_title
- previous_episode
- generation_version
- producer
- language/locale/timezone
- production status

## B. Episode scope
Define:
- main podcast topic;
- central narrative question;
- theme;
- primary POV;
- beginning state;
- conflict;
- turning point;
- resolution type;
- ending hook;
- emotional arc;
- humour level;
- mystery level.

## C. Source manifest
Every source must have:
- source_id;
- source type;
- location/path;
- authority;
- availability;
- permission/licensing state;
- retrieval scope;
- notes.

Required source classes:
1. Bible reference;
2. course/education reference;
3. current-news reference where used;
4. season/chapter notes;
5. previous episode;
6. character canon;
7. technology/world canon;
8. archive references;
9. producer story notes.

## D. Continuity preflight
Before generation:
1. load previous episode;
2. load current season/chapter notes;
3. load relevant archive;
4. identify chronological date;
5. identify all named characters;
6. identify canon claims;
7. identify unresolved questions;
8. flag contradictions;
9. do not invent bridges for unresolved conflicts.

## E. Canon policy
Classify important claims:
- CONFIRMED_CANON
- ARCHIVAL_RECORD
- PROPOSED_NEW_CANON
- WORKING_INTERPRETATION
- SPECULATION
- UNKNOWN

Only the first two may be presented as established history without qualification.

## F. Real-world boundary
Real news remains factual and sourced. Fictional Chronicle material must not claim that fictional characters caused or solved real-world events unless explicitly framed as fiction.

News may inspire a **thematic mirror** or fictionalized parallel.

## G. Bible integration
The Bible reference should influence theme, character reflection or moral framing naturally. Do not force scripture into dialogue merely to satisfy a checklist.

## H. Course integration
Use only the course material assigned to the episode. Do not teach a later formal lesson prematurely.

For S00E01:
- introduce Koware Group;
- introduce Buzzjuice Network;
- introduce Buzzjuice Courses;
- defer formal Health & Safety instruction.

## I. Chronicle-first gate
The approximately 200-second Chronicle must be completed and producer-approved before the podcast is treated as final programme content.

Trailer must be derived from the approved Chronicle.

## J. Output package
Generate in order:
1. Story Brief
2. Narrative Draft
3. Chronicle Script
4. Scene/Timing List
5. Visual Prompt List
6. Audio/SFX List
7. Chronicle QA
8. 20-second Trailer
9. Podcast Discussion Package
10. Provenance Manifest
11. Post-episode persona observations

## K. Retrieval controls
Default scope: `CURRENT_EPISODE`.

Allowed scopes:
- CURRENT_EPISODE
- CURRENT_SEASON
- ALL_APPROVED_EPISODES
- GLOBAL_CHRONICLES

The AI must never silently broaden retrieval.

## L. Consent/licensing
Retrieval permission and publication permission are separate.

Subscription status, course participation or crowdfunding tier may affect eligibility for participation, but does not automatically create canon or publication rights.

## M. AI intervention policy
AI may suggest, draft, reorganize and flag.

AI may not silently:
- create canon;
- rewrite archives;
- fabricate news;
- fabricate citations;
- override consent;
- override licensing;
- publish.

## N. Humour
Default: warm, observational, light slapstick.

Target: approximately one principal physical/comedic beat per 200-second Chronicle.

Humour must never trivialize serious real-world news or the character's vulnerability.

## O. Audit header
```json
{
  "template_version_used": "3.2",
  "generation_timestamp_utc": null,
  "model_provider": null,
  "source_ids": [],
  "retrieval_scope": "CURRENT_EPISODE",
  "deterministic_seed": null,
  "output_hash_sha256": null,
  "producer_approval_state": "PENDING"
}
```

## P. QA
FAIL:
- missing required source;
- fabricated news/citation;
- continuity contradiction without explicit reason;
- consent/licensing failure;
- critical narrative element missing.

WARN:
- weak sensory detail;
- weak transitions;
- weak humour;
- incomplete continuity reference.

## Q. Producer gate
AI QA is not story approval.

Producer explicitly approves:
- story outline;
- Chronicle;
- canon changes;
- consent/licensing state;
- final archive state.
