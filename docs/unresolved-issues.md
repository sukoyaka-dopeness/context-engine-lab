# Unresolved Issues

These are not bugs awaiting fixes. They are structural features of an honest epistemic project.  
The list is public, versioned, and open for discussion.

*Last updated: 2026-02 (Claude relay)*

---

## Open Problems

### U1 — Structural Reach Problem
**Problem:** The people most likely to benefit from epistemic literacy training are least likely to seek it out. SNS inflow strategy (linking from live debates) partially addresses this, but the chicken-and-egg problem remains: inbound links require prior trust in the platform, which requires prior content accumulation.  
**Mitigation:** Phase 1 AI content seeding establishes the archive before inflow is attempted.  
**Status:** Partially mitigated. Fundamentally unresolved.  
**Relevant research:** Motivated reasoning literature (Kunda 1990; Mercier & Sperber 2011)

---

### U3 — False Balance Risk
**Problem:** Presenting two sources implies equivalence, regardless of evidence weight.  
**Mitigation adopted:** Weight of Evidence Visualization + Forewarning Box + Consensus Messaging (conditional)  
**Remaining concern:** The consensus bar itself can be read as politically biased in domains where the existence of consensus is contested.  
**Partial resolution:** When this risk materializes on a specific topic, it is labeled explicitly — and the false-balance problem itself becomes a topic.  
**Status:** Partially mitigated. Complete resolution may be impossible.

---

### U5 — AI Authority Drift
**Problem:** Any curating system becomes an epistemic authority. Disclaimers do not eliminate this. Curation is authority — framing, inclusion decisions, and tag structures all carry implicit endorsement.  
**Mitigation adopted:** Cross-AI Comparison Button, Public Error Log, AI Non-Authority footer on all AI-generated content.  
**Status:** Managed, not resolved.

---

### U7 — Epistemic Pain Design Ethics
**Problem:** Designing an experience to make belief-updating feel meaningful is itself a form of behavioral influence, even when well-intentioned.  
**Reframed question:** Can discomfort be given meaning without being instrumentalized?  
**Direction adopted:** Connect discomfort to researcher accounts of hypothesis falsification. Provide meaning context, not reward substitution. The discomfort is not converted — it is given context.  
**Status:** Direction confirmed. Implementation details unresolved.

---

### U9 — Troll and Weaponization Containment
**Problem:** Tag system and badge system can be gamed by coordinated bad-faith actors. Distributed micro-task system is vulnerable to organized manipulation — individual tasks appear legitimate, but accumulation produces directional bias.  
**Mitigation adopted:** Cool-Down Rate Limiting, Tag Review Voting, misuse logged and converted to educational material.  
**Remaining concern:** Goodhart's Law applies to all metrics in this system. When a measure becomes a target, it ceases to be a good measure.  
**Status:** Partially mitigated. Requires ongoing monitoring.

---

### U11 — Self-Tagging Adoption Rate
**Problem:** Getting users to voluntarily tag their own epistemic position requires both understanding of the system and willingness to self-expose.  
**Mitigation adopted:** Annotation UI designed for low friction — memo/annotation feel, not judgment feel; sample tags shown by default.  
**Status:** UI approach adopted. Actual adoption rate unknown until deployment.

---

### U12 — Consensus Source Update Automation
**Problem:** Consensus levels change. How to keep consensus data current without introducing editorial bias through selective updating?  
**Options under consideration:** Trusted API integration / periodic crawl / manual update with dated disclosure.  
**Status:** Unresolved. Requires both technical and editorial policy decision.

---

### U13 — Visualization Color Bias
**Problem:** Green/red color coding for evidence weight carries implicit positive/negative judgment and creates accessibility problems for users with color vision differences.  
**Resolution adopted:** Single-hue blue, intensity scaled by evidence weight. Stronger evidence = deeper blue. No second color introduced.  
**Status:** Resolved.

---

### U14 — User Experiment Motivation Strategy
**Problem:** Posting to Open Lab has high user cost. Intrinsic motivation (curiosity, contribution, social recognition) must be cultivated, not assumed.  
**Direction:** Badge reinforcement + shared stories + low-cost entry form (5 fields maximum).  
**Status:** Direction noted. Concrete implementation deferred pending user observation.

---

### U15 — Natural Science Examples Expansion
**Problem:** Current example set covers five topics. Criteria for expansion are unclear.  
**Criteria under consideration:** Consensus gradient diversity, active replication debate, paradigm shift potential, public salience.  
**Status:** Open for community contribution.

---

### U16 — Humanities Tagging Schema
**Problem:** How to convert historical interpretation into structured tags without forcing binary truth framing.  
**Direction:** Philosophy Deconstruction Template (see `content/templates/philosophy-deconstruction-template.md`).  
**Status:** Template drafted. Schema logic incomplete.

---

### U17 — Initial Topic Selection
**Problem:** Urban legends were proposed as a low-stakes starting point for methodology training. However, urban legends are adjacent to conspiracy theories and can politicize rapidly.  
**Resolution adopted:** Initial topics focus on cases where scientific consensus was overturned — moments where the method worked and beliefs were correctly updated. Examples: Marshall & Warren (peptic ulcers), Wegener (continental drift), Perlmutter, Schmidt & Riess (accelerating expansion).  
**Status:** Resolved.

---

### U18 — Context Package UI Design
**Problem:** Micro-task context packages need detailed UI specification.  
**Requirements:** Collapsible, non-mandatory, visible on demand, updatable post-hoc. Empty package must explicitly state "This task does not require context."  
**Status:** Concept confirmed. Detailed UI spec not yet written.

---

### U19 — AI-Generated Content Quality Standards
**Problem:** Phase 1 relies on AI-generated content. What are the minimum quality thresholds before publishing?  
**Options under consideration:** Minimum source count required / claim type tagging required / human review before publishing / publish-and-flag model.  
**Status:** Unresolved. Policy decision required before Phase 1 launch.

---

## Resolution Summary

| Issue | Status |
|-------|--------|
| U3 False Balance Risk | Partially mitigated |
| U5 AI Authority Drift | Managed |
| U7 Epistemic Pain Ethics | Direction confirmed |
| U9 Weaponization | Partially mitigated |
| U13 Color Bias | **Resolved** — single-hue blue |
| U17 Initial Topics | **Resolved** — overturned consensus cases |
| U1, U11, U12, U14, U15, U16, U18, U19 | Open |

---

*To propose an approach to any unresolved issue, open a Discussion thread — not a PR. Solutions require deliberation before implementation.*
