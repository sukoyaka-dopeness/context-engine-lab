# Feature Spec: Tag System

## Purpose

Make the structure of a claim visible without making a judgment about its truth.

---

## Tag Dimensions

### `claim_type`

| Value | Description |
|-------|-------------|
| `empirical` | Testable, falsifiable, subject to evidence |
| `interpretive` | Framework-dependent, methodology-sensitive |
| `normative` | Value-laden, prescriptive |
| `conspiratorial` | Unfalsifiable by design, appeals to hidden agency |

**Hybrid claims:**  
Use layered tagging. A claim may have a `primary_claim_type` and a `secondary_layer` with a note explaining the hybrid structure. Forcing single-type classification on hybrid claims produces false clarity and should be avoided.
```yaml
primary_claim_type: empirical
secondary_layer: normative
note: "The empirical framing assumes a normative baseline of [X]"
```

### `epistemic_domain`

`natural_science` / `social_science` / `humanities` / `interdisciplinary`

### `rhetoric_style`

Examples (not exhaustive):

| Tag | Description |
|-----|-------------|
| `peer_reviewed_citation` | Argument supported by peer-reviewed source |
| `appeal_to_authority` | Argument rests on authority rather than evidence |
| `anecdotal` | Argument rests on individual case or story |
| `false_dilemma` | Two options presented as exhaustive when others exist |
| `gish_gallop` | Volume of claims used to overwhelm rather than argue |
| `motte_and_bailey` | Switching between defensible and indefensible versions of a claim |
| `cherry_picking` | Selective use of evidence ignoring contrary data |

New rhetoric style tags can be proposed via Issue with label `tag-proposal`.

### `historical_pattern`

| Tag | Description |
|-----|-------------|
| `paradigm_shift_candidate` | Claim may overturn current consensus |
| `prior_consensus_reversed` | This claim type was once mainstream and was revised |
| `replication_crisis_affected` | Field or finding has known replication problems |
| `longstanding_consensus` | Claim has been stable across extended period |
| `emerging_field` | Insufficient evidence base for strong pattern classification |

---

## UI Design

**Default state:**
- Three most common tags for this topic shown as one-click options
- Sample tags always visible to guide first-time users
- Annotation feel, not judgment feel — memo-style interface

**Advanced state:**
- Free-text tag entry with category selector
- Layered tagging interface for hybrid claims

**Friction design:**  
Low friction is the default. The system should make tagging feel like adding a margin note, not filling out a form.

---

## Tag Review Voting

When a tag is disputed:

1. Any user can flag: *"Is this tag correct?"*
2. Community vote is triggered when minimum threshold is reached (default: 3 flags)
3. Voting result is displayed as metadata on the tag
4. Disputed tags and their resolution records are archived as teaching material

**This is cooperative annotation, not moderation.**  
No tag is deleted by vote alone. Dispute records are preserved and may become content.

---

## AI-Generated Tags

Initial tags on AI-seeded content are AI-generated.  
Label: *[AI-tagged — review welcomed]*

These are treated as first-draft hypotheses, not ground truth.  
Correcting an AI-generated tag is a primary contribution type and triggers `Primary_Source_Added` badge consideration if a source is included.
