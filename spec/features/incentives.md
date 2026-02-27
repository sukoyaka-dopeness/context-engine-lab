# Feature Spec: Incentives and Motivation

## Design Problem

Standard gamification rewards certainty, speed, and volume.  
This project needs to reward the opposite: uncertainty acknowledgment, care, and belief revision.

The challenge is not to make epistemic discomfort disappear.  
The challenge is to make it meaningful.

---

## Badge System

| Badge | Trigger condition |
|-------|-----------------|
| `Belief_Updated` | User explicitly marks that their position changed |
| `Verification_Attempted` | User submits to Open Lab or links a verification attempt |
| `Primary_Source_Added` | User adds a citable primary source with full metadata |
| `Open_Lab_Posted` | User posts an experiment result to Open Lab |

### Status hierarchy

`Belief_Updated` is the highest-status badge.

This is a deliberate cultural design choice.  
Long-term goal: *"I changed my mind"* becomes a social signal of intellectual credibility, not weakness.  
This must be reinforced consistently across every interface element, every default state, and every piece of copy in the platform.

### What badges do not reward
- Being right the first time
- Having the most citations
- Identifying flaws in someone else's reasoning
- Volume of contributions

---

## Epistemic Pain → Meaning

### The problem with dopamine-based design

Rewarding belief-updating with points, streaks, or level-ups instrumentalizes the experience.  
It converts intellectual honesty into a game mechanic — which is its own form of epistemic distortion.  
Designing away the discomfort also designs away what makes the discomfort informative.

### The reframed approach

Connect the discomfort of belief-updating to the shared experience of researchers:

- Curated accounts from scientists and researchers describing when their hypotheses were falsified
- Displayed contextually when users encounter challenging evidence or reach an impasse
- Framing:

> *"The discomfort you are experiencing is what updating feels like. It is evidence of intellectual honesty."*

This is not dopamine substitution. It is meaning provision through relatedness.  
The discomfort is not converted. It is given context.

### Content requirements for this mechanism

- Accounts must be first-person and specific (not generic "science is hard" platitudes)
- Accounts should span disciplines and career stages
- Accounts should include what the researcher believed before, what changed, and what the update felt like
- AI-generated placeholder accounts are not acceptable here — this mechanism depends on authenticity

### Implementation status

Direction confirmed. Specific content curation, trigger timing, and display format are unresolved (U14).  
Requires user observation to determine optimal conditions.

---

## Intrinsic Motivation Layers

Drawing from citizen science and open-source contribution literature:

| Layer | Mechanism |
|-------|-----------|
| Learning motivation | Research history timelines, paradigm shift cases, replication crisis data |
| Contribution motivation | Correcting AI-generated errors, adding primary sources |
| Social recognition | Badges visible in profile; `Belief_Updated` as highest status signal |
| Epistemic relatedness | Researcher accounts of hypothesis falsification |

These layers are not independent. Learning motivation creates the conditions for contribution motivation. Social recognition reinforces epistemic relatedness.

---

## Open Lab Motivation

Posting to Open Lab is the highest-cost action in the platform.  
Motivation strategy:

- `Open_Lab_Posted` badge (social recognition)
- Shared story format — not data dump, but narrative of attempt
- Pre-filled context from Falsification Button reduces entry cost
- Low-cost entry form: 5 fields maximum
- Integration with OSF/Zenodo provides external credibility signal

**Target user for Open Lab:** Users with existing scientific curiosity who need a low-friction channel to act on it.  
Not all users. Designing for mass Open Lab participation will produce low-quality submissions.

**Status:** Strategy noted. Full implementation deferred to Phase 3.

---

## What This System Does Not Do

- Reward users for convincing others
- Reward users for volume of posts
- Create leaderboards ranked by certainty or citation count
- Penalize users for holding positions that later turn out to be correct
- Simulate scientific progress through point accumulation
