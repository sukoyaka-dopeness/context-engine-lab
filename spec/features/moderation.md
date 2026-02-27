# Feature Spec: Moderation

## Philosophy

Moderation in Context Engine Lab does not delete content. It adjusts pace and surfaces structure.

The goal is to reduce conditions that prevent epistemic engagement — not to enforce conclusions.

---

## Cool-Down Rate Limiting

### Trigger conditions
- High-emotion language pattern detected (escalating rhetoric indicators)
- Rapid successive posting within a defined time window (threshold: TBD at deployment)

### Action
- Time-gap enforcement between posts
- No content deletion
- No account penalty
- No permanent record of trigger event attached to user

### User notification
Neutral tone, non-accusatory:

> *"You're posting quickly. Take a moment before continuing."*

### Rationale
Deletion creates martyrdom dynamics and chilling effects on legitimate speech.  
Pacing interrupts escalation without suppressing content.  
Freedom of expression is maintained. Speed of escalation is reduced.

### Unresolved
Specific time-window threshold and cool-down duration are not defined here.  
These should be determined empirically after deployment observation, not preset arbitrarily.

---

## Tag Review Voting

See [`spec/features/tag-system.md`](tag-system.md) for full detail.

**Summary:**
- Any user can flag a disputed tag
- Community vote triggered at 3 flags (default)
- Vote result displayed as metadata
- No tag deleted by vote alone
- Dispute records archived as teaching material

This is cooperative annotation, not content moderation.

---

## Political Usage Log

All instances of apparent platform weaponization are:

1. Logged (anonymized — no user identification stored)
2. Analyzed periodically for patterns
3. Converted to meta-analysis content:

> *"Here is how this platform has been misused, and what that reveals about epistemic dynamics."*

The log is public. Exploitation becomes education.  
This is consistent with the project's core principle: structural exposure, not condemnation.

---

## Auto Meta-Layer Suggestion

When discussion reaches impasse, the UI surfaces a suggestion rather than intervening directly.

Trigger conditions (two or more must be active):
- Repeated position restatement without new evidence
- Escalating rhetoric-style tags accumulating
- High posting frequency without substantive change
- Explicit user flag: *"This is going in circles"*

UI prompt:

> *"This discussion appears to have reached an impasse pattern. Would you like to see the meta-layer?"*

Options: **[View meta-layer]** / **[Dismiss]**

The suggestion does not reappear for the same thread within a cooldown period after dismissal.

---

## What Moderation Does NOT Do

- Delete factually incorrect content — tagging and evidence weight visualization handle this
- Ban users for holding minority positions
- Adjudicate truth claims
- Favor any political position in enforcement decisions
- Apply different standards based on the direction of bias (symmetry rule applies to moderation)

---

## Unresolved: Coordinated Manipulation (U9)

Distributed bad-faith actors can manipulate the tag system and micro-task system through coordinated participation that appears legitimate at the individual level.

**Current mitigations:** Cool-Down rate limiting, Tag Review Voting  
**Known limitation:** Goodhart's Law applies. Any measurable metric can become a manipulation target.  
**Partial resolution:** Misuse records are converted to educational content, reducing the asymmetric benefit of manipulation.  
**Status:** Ongoing monitoring required. No complete solution identified.

See [`docs/unresolved-issues.md`](../unresolved-issues.md) — U9.
