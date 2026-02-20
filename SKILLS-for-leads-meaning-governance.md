# Skills — For Leads and Principals Governing Meaning

**Role:** Technical leads, principal designers, and senior engineers who are responsible for the semantic integrity of a product or system over time — not just the quality of individual contributions, but the coherence of the whole.

**Sources:** SWD Ops cluster, DSO 12 + Canon Axiom 7, Constraints 6–8, Non-Negotiables 2, 7, 8

---

## What meaning governance actually is

Meaning governance is the practice of ensuring that what things mean in a system is decided, owned, consistent, and maintainable over time. It is not documentation for its own sake. It is not process theater. It is the answer to a practical question that every senior person in a product organization eventually faces: why are we making the same decisions twice, contradicting what we decided six months ago, and arguing about things that should have been settled?

The answer is almost always: because no one owned the meaning, so no one maintained it.

---

## Skill 1 — Owning the semantic model, not just the architecture

Leads typically own architectural decisions. Meaning governance requires owning one layer above that: the semantic model — the set of entities, relationships, capabilities, and constraints that define what the product actually is.

The skill is treating this model as a maintained artifact, not an implicit shared understanding. It should be explicit enough that a new team member can read it and understand the product's conceptual structure — not just its technical architecture. When a feature is added, the question is not only "does this fit the architecture?" but "does this conform to the semantic model, or does it require the model to change?"

---

## Skill 2 — Making semantic authority visible

In every system, someone is the de facto authority on what things mean. In well-governed systems, this authority is explicit and named. In poorly governed systems, it is diffuse and contested — or worse, it defaults to whoever spoke last in the meeting.

The skill is making authority visible: who owns the definition of each major entity, who approves semantic changes, who resolves conflicts when teams disagree about what something means. This does not require a bureaucratic hierarchy. It requires names attached to responsibilities. SWD's governance principle applies: if users cannot tell who owns meaning, governance does not exist.

---

## Skill 3 — Running semantic change review

Semantic changes are not a subset of code review or design review. They are a distinct category that requires a distinct process. A semantic change is anything that modifies what an entity means, changes the conditions of a capability, redefines a constraint, or introduces a new term that will be used across the system.

The skill is maintaining a lightweight but explicit semantic review process: changes of this type are flagged, reviewed by the semantic authority, and recorded. The record includes what changed, why, and what downstream effects to expect. Without this process, semantic changes happen constantly and silently — through drift, inference, and unreviewed implementation decisions.

---

## Skill 4 — Versioning meaning changes

When the semantic model changes, existing consumers of that model — implementations, documentation, automations, integrations — may be affected. The skill is treating semantic model changes as versioned events, not as invisible corrections.

This does not require complex versioning infrastructure. It requires: a change log for semantic changes, a clear statement of what changed between versions, and a process for evaluating which consumers need to be updated. Without versioning, semantic history is lost, and teams lose the ability to trace why something means what it currently means.

---

## Skill 5 — Distinguishing stewardship from ownership

The Canon's definition of a custodian applies here directly: a custodian preserves invariants, rejects invalid changes, and does not own the Canon — they steward it. The same distinction applies to meaning governance. The lead who governs meaning does not own it in the sense of having unilateral authority. They steward it in the sense of being responsible for its integrity.

The skill is holding this distinction under pressure. When stakeholders want to redefine a term for convenience, the governance role is to evaluate whether the redefinition is structurally valid — not to block change, but to ensure change is explicit, consistent, and recorded. Authority-as-stewardship is the model. Authority-as-control is the misuse the Canon warns against.

---

## What effective meaning governance produces

A team led by someone with these skills has: a semantic model that is maintained rather than inferred, change decisions that are traceable, disagreements that can be resolved by reference to declared meaning rather than by negotiation, and a system that accumulates coherence over time rather than contradictions.

The governance failure the Canon identifies — where responsibility is diffused and correction collapses — is the direct failure mode that these skills prevent.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
