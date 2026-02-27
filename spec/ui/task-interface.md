# UI Spec: Task Interface

## Unified Interface Principle

All micro-tasks — whether context-dependent or context-independent — use the same interface structure.

**Rationale:**
- Eliminates user cost of determining task type before starting
- Empty context package signals "context not required" without requiring explanation
- Allows context to be added retroactively as content matures without interface redesign

---

## Interface Structure
```
┌─────────────────────────────────────────────────────────┐
│ TASK                                                    │
│                                                         │
│ [Task description]                                      │
│                                                         │
│ ▶ Context  [click to expand]                            │
│                                                         │
│ [Action area]                                           │
│                                                         │
│ [Submit]                                                │
└─────────────────────────────────────────────────────────┘
```

The context section is always present. Its content varies.  
Collapsed by default. Expanding is an offer, not a requirement.

---

## Context Package: When Present

For context-dependent tasks (rhetoric style judgment, claim type tagging, interpretive classification):
```
▶ Context  [click to expand]
  ───────────────────────────────────────────────
  Topic summary
  One sentence. What this topic is about.

  Prior rhetoric patterns on this topic (2–3 examples)
  How this claim type has been argued historically.

  Reference
  [Link] — For users uncertain about their judgment.
  ───────────────────────────────────────────────
```

**Design notes:**
- All three elements are present when context exists
- Reading the context is never required to submit
- The reference link opens in a new tab — does not interrupt the task

---

## Context Package: When Empty

For context-independent tasks (link verification, citation year check, source existence confirmation):
```
▶ Context  [click to expand]
  ───────────────────────────────────────────────
  This task does not require topic context.
  ───────────────────────────────────────────────
```

This explicit message prevents user confusion and signals that the absence of context is intentional, not an error.

---

## Task Type Examples

### Layer 1 — Context-independent (distributable)

| Task | Description |
|------|-------------|
| Link verification | Does this URL resolve to the cited source? |
| Citation year check | Is the publication year listed correctly? |
| Source existence | Does this paper exist in the cited journal? |

### Layer 2 — Context-dependent (context package required)

| Task | Description |
|------|-------------|
| Rhetoric style tagging | Which rhetoric style tag fits this argument? |
| Claim type classification | Is this claim empirical, interpretive, normative, or conspiratorial? |
| Hybrid claim detection | Does this claim have a secondary layer? |
| Timeline entry verification | Is this historical event accurately described? |

---

## Action Area Variants

The action area changes by task type while the surrounding structure remains identical.

**Tag selection task:**
```
[empirical]  [interpretive]  [normative]  [conspiratorial]
or: [ Add a different tag ]
```

**Verification task:**
```
( ) Confirmed    ( ) Cannot confirm    ( ) Incorrect — see notes
[ Notes field — optional ]
```

**Timeline entry task:**
```
( ) Accurate    ( ) Inaccurate    ( ) Needs source
[ Source field — optional ]
```

---

## Submission Behavior

- Submit button is always available — users are never blocked from submitting
- Submitting without opening context is valid
- Submitting without notes is valid for all task types
- After submission: brief confirmation, then next task or return to topic

---

## Retroactive Context Addition

When a task was initially context-independent and context is later added:

- The context package populates on next user encounter
- Previously submitted responses are not invalidated
- A flag is added to prior submissions: *"Context was added after this response was submitted"*

This preserves the integrity of the response record while acknowledging the changed conditions.
