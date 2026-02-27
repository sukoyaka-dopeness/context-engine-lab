# UI Spec: Meta-Layer Transition

## Purpose

When first-order discussion reaches genuine impasse, make the structure of the impasse visible — without forcing it.

The meta-layer does not resolve disagreements.  
It makes visible why the disagreement is structured the way it is.

---

## Trigger Conditions

The system monitors for impasse indicators. Transition is suggested when **two or more** of the following are active simultaneously:

| Indicator | Description |
|-----------|-------------|
| Position restatement | Same position restated without new evidence introduced |
| Rhetoric escalation | Rhetoric-style tags accumulating (e.g. `appeal_to_authority`, `false_dilemma`) |
| Posting velocity | High frequency without substantive content change |
| User flag | Explicit flag submitted: *"This is going in circles"* |

Two-indicator threshold prevents premature triggering on normal discussion friction.  
Single-indicator triggering would make meta-escape too available.

---

## UI Prompt

Displayed as a non-intrusive banner above the discussion thread:
```
┌─────────────────────────────────────────────────────────┐
│ This discussion appears to have reached an impasse      │
│ pattern. Would you like to see the meta-layer?          │
│                                                         │
│ [View meta-layer]                 [Dismiss]             │
└─────────────────────────────────────────────────────────┘
```

**Behavior after dismissal:**  
The prompt does not reappear for the same thread within a defined cooldown period.  
It may reappear if new impasse indicators accumulate after the cooldown.

**Behavior after viewing:**  
Meta-layer opens below the prompt. Thread remains visible above.  
User can return to thread at any time.

---

## Meta-Layer Content

When the user opens the meta-layer, three sections are displayed:

### Section 1: Why this discussion may be stalled

Plain-language description of the detected pattern:

> *"Positions in this discussion appear to differ on underlying values or frameworks, not on the evidence itself. New evidence is unlikely to resolve this disagreement without first clarifying what each position is built on."*

Identified rhetoric tags from the thread are listed here as data, not accusations.

### Section 2: What the underlying disagreement may be about

Diagnosis of the impasse type:

| Impasse type | Prompt shown |
|-------------|-------------|
| Empirical dispute | *"The core disagreement is about evidence. See the evidence weight visualization."* → link |
| Framework dispute | *"The core disagreement is about which framework to apply. See the philosophy deconstruction view."* → link |
| Definition dispute | *"The core disagreement may be about what terms mean. See the claim layer decomposition."* → link |
| Mixed | Multiple prompts shown |

### Section 3: Options

| Option | Action |
|--------|--------|
| See evidence weight | Opens Weight of Evidence visualization for the core claim |
| Explore ethical frameworks | Opens Philosophy Deconstruction view |
| See forewarning | Opens Forewarning Box if false-balance risk applies |
| Flag as unresolvable | Adds thread to Aporia Archive |

---

## Aporia Archive

Threads flagged as unresolvable are added to the Aporia Archive.

Archive entry includes:
- Thread summary (auto-generated, AI-labeled)
- Detected impasse type
- Rhetoric tags accumulated during discussion
- Date range of discussion

**Purpose:**  
Recurring impasse patterns on the same topic become content.  
The archive entry reads:

> *"This topic has generated recurring impasse patterns. Here is the structural analysis of why disagreement persists."*

Unresolvable disagreements are not failures. They are data about the structure of the topic.

---

## Constraints

**Meta-layer is never the default view.**  
First-order discussion must occur before meta-layer is available.

**Meta-layer is never pre-emptively suggested.**  
It is only surfaced after impasse indicators are detected.

**Meta-layer does not declare a winner.**  
It describes structure. It does not adjudicate between positions.

**Frequency constraint:**  
If meta-layer is dismissed repeatedly in the same thread, the system does not escalate pressure.  
Repeated dismissal is itself data — it may indicate that the user prefers first-order engagement, or that the impasse detection is producing false positives.

---

## Meta-Layer as Content

Impasse patterns that recur across multiple threads on the same topic are archived and surfaced as a topic-level note:

> *"Discussions of this topic frequently reach this type of impasse. The structural reason is: [detected pattern]."*

This converts discussion failures into meta-content — demonstrating that the difficulty of a topic is itself informative, and consistent with the project's core principle of structure exposure.
