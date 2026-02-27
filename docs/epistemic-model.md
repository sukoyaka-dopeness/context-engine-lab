# Epistemic Model

## Multi-Tag System

Every claim in Context Engine Lab is tagged across four dimensions:

### 1. `epistemic_domain`
- `natural_science`
- `social_science`
- `humanities`
- `interdisciplinary`

### 2. `claim_type`
- `empirical` — testable, falsifiable, subject to evidence
- `interpretive` — dependent on framework, methodology, historical context
- `normative` — value-laden, prescriptive
- `conspiratorial` — unfalsifiable by design, appeals to hidden agency

> **Note on hybrid claims:** Most contested claims are not cleanly one type. A claim tagged `empirical` may carry significant `normative` load. The tag system supports layered classification — a `primary_claim_type` and a `secondary_layer` with a note explaining the hybrid structure. Forcing single-type classification on hybrid claims produces false clarity.

### 3. `rhetoric_style`
How a claim is argued, independent of its content:
- `peer_reviewed_citation`
- `appeal_to_authority`
- `anecdotal`
- `false_dilemma`
- `gish_gallop`
- `motte_and_bailey`
- `cherry_picking`

*(List is illustrative, not exhaustive. New rhetoric styles can be proposed via Issue.)*

### 4. `historical_pattern`
Whether this claim type has historical precedents:
- `paradigm_shift_candidate`
- `prior_consensus_reversed`
- `replication_crisis_affected`
- `longstanding_consensus`
- `emerging_field`

---

## Temporal-Regional Metadata

Each topic records:

| Field | Description |
|-------|-------------|
| `temporal_distribution` | When this claim was prominent, contested, or resolved |
| `regional_variants` | How consensus or controversy varies by geography or culture |
| `intensity_index` | Current level of active debate |

---

## Primary Source Dual Presentation

Topics present at minimum two primary sources (A and B) with the following metadata:

| Field | Description |
|-------|-------------|
| `peer_review` | Whether the source is peer-reviewed |
| `year` | Publication year |
| `citations` | Citation count (approximate) |
| `replication_status` | Replicated / Failed / Not yet attempted / Meta-analysis exists |

**Important:** Dual presentation does not imply equivalence.  
Evidence weight visualization makes asymmetry visible. See below.

---

## Weight of Evidence Visualization

### Simple View (default)
- Horizontal bar showing consensus level
- Paper count indicator
- **Color: single-hue blue, intensity scaled by evidence weight**
- Rationale: single-hue intensity avoids the positive/negative connotation of green/red while remaining immediately readable. Accessible to users with color vision differences.

### Detail View (click to expand)
- Total citation sum across supporting sources
- Replication count
- Year trend graph (is evidence accumulating or stalling?)
- Link to relevant meta-analyses

**Design rationale:**  
One-glance asymmetry awareness with low cognitive load. Detail available for those who want it. No forced engagement.

---

## Consensus Messaging (Light Version)

When consensus is high and domain is natural science:

> *"[X]% of peer-reviewed papers support this position. Source: [meta-analysis citation]. Last updated: [date]."*

Requirements:
- Meta-analysis source must be cited
- Last updated date must be displayed
- Not shown in humanities, philosophy, or low-consensus domains

*(See [`docs/philosophy.md`](philosophy.md) for full consensus display policy.)*

---

## Forewarning Box

Displayed at the top of threads with false-balance risk:

> *"This topic is sometimes presented as a debate between equally supported positions. The evidence base for each position differs significantly. See the evidence weight visualization below."*

Neutral, educational tone. No ridicule. No verdict.

**Why it works:**  
Pre-emptive warning (inoculation effect) is empirically demonstrated to reduce false-balance impression.

---

## Claim Layer Decomposition

For hybrid claims, layered tagging is used:
```yaml
primary_claim_type: empirical
secondary_layer: normative
note: "The empirical framing assumes a normative baseline of [X]"
```

This makes hybrid structure visible rather than forcing false clarity onto claims that do not have it.
