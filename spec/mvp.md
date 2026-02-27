# MVP Specification

## Scope

The minimum viable product validates the core interaction loop:  
**Encounter a claim → See its structure → Have a path to test it**

---

## MVP Feature Set

### 1. Tag System
- `claim_type` tagging: empirical / interpretive / normative / conspiratorial
- `epistemic_domain` tagging
- Hybrid claim support: layered tagging with `secondary_layer` and note
- Community tag review voting
- Annotation UI: low-friction, memo-style, sample tags shown by default

### 2. Weight of Evidence Visualization
- Simple view: single-hue blue intensity bar + paper count
- Detail expand: citation sum, replication count, year trend graph
- Forewarning Box on false-balance risk topics

### 3. Falsification Button
- Label: *"What would it take to falsify this?"*
- Output: AI-generated hypothetical prediction with mandatory uncertainty disclosure
- Edge case handling: unfalsifiable claims and normative claims addressed explicitly
- Link to Open Lab submission form

### 4. Forewarning Box
- Displayed at top of false-balance risk threads
- Neutral, educational tone
- No verdict, no ridicule

### 5. Cool-Down Rate Limiting
- Triggered by: high-emotion language patterns, rapid successive posting
- Action: time-gap enforcement only — no content deletion
- User notification: neutral tone

### 6. Badge System (basic)
- `Belief_Updated`
- `Verification_Attempted`
- `Primary_Source_Added`
- `Open_Lab_Posted`

### 7. Initial Topic Set
Five natural science examples plus three overturned-consensus cases:

**Natural science examples (consensus gradient):**
- Anthropogenic climate change
- mRNA vaccine safety
- Quantum gravity candidates (string theory vs. loop quantum gravity)
- Dark energy nature
- Gut microbiome and mental health causality

**Overturned consensus cases (tentativeness demonstration):**
- Peptic ulcers: bacterial causation (Marshall & Warren)
- Continental drift (Wegener)
- Accelerating expansion of the universe (Perlmutter, Schmidt, Riess)

All topics include: research history timeline, dual source presentation, evidence weight metadata, falsification prompt.

---

## Out of Scope for MVP

- Browser extension overlay
- Cross-AI comparison button (infrastructure dependency)
- Full humanities tagging schema (U16)
- Automated consensus source updates (U12)
- Full Open Lab integration with OSF/Zenodo

---

## MVP Success Indicators

| Indicator | Minimum threshold |
|-----------|------------------|
| User-generated tags | Any non-zero sustained rate |
| Primary source click rate | > 10% of topic views |
| Falsification button usage | > 5% of topic views |
| Aggressive language frequency | Downward trend after cool-down implementation |
| Belief update stories posted | Any |

These are behavioral indicators. Epistemic literacy manifests in behavior, not declarations.

---

## Phase Sequence

| Phase | Trigger condition | Primary activity |
|-------|------------------|-----------------|
| 1 | Now | AI-generated content seeding; all items labeled AI-generated |
| 2 | Phase 1 archive substantially complete | SNS inflow — link seeding from live debates |
| 3 | Phase 2 demonstrates stable inflow | User participation layer — tag review, Open Lab, discussion layer |

Phase 2 requires Phase 1 to be substantially complete.  
Phase 3 requires Phase 2 to demonstrate stable inflow.  
Skipping phases is a known risk: the chicken-and-egg problem (U1) worsens if Phase 2 is attempted before content exists.
