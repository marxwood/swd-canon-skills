# Skills — For Engineers Working in Canonical Constraint Systems

**Role:** Engineers building systems where structural validity is explicitly defined — systems governed by a canon, an ontology, or a formal constraint set — who need to maintain the separation between implementation and canonical truth.

**Sources:** Canon Axioms 1, 5, 6, 10 + Constraints 1, 3, 4, 7 + SWD Foundations 04, 05, DSO 01

---

## The engineering framing

In a canonical constraint system, the implementation is not the source of truth. The Canon (or the declared semantic model) is. The implementation's job is to realize canonical constraints correctly — not to redefine them, extend them, or optimize around them.

This is a different engineering discipline than building to specifications, because specifications describe desired behavior. Canonical constraints describe structural limits that the implementation must not violate — regardless of whether violating them would "work."

---

## Skill 1 — Keeping implementations replaceable

The Canon's fifth axiom is explicit: all implementations are replaceable. Dependence on a specific implementation constitutes structural failure. Engineering decisions that create tight coupling between the canonical structure and a specific tool, platform, or stack are canonical violations — even if they improve performance.

The skill is building to the constraint interface, not to the tool. When an architectural decision couples canonical validity to a specific implementation, that decision must be flagged as a structural risk. The question to ask before any major technical decision: if this tool were replaced tomorrow, would the canonical constraints survive the replacement?

---

## Skill 2 — Never inferring canonical meaning from implementation behavior

Implementations drift. Behavior changes. Bugs introduce unexpected states. When implementation behavior diverges from declared canonical meaning, the implementation is wrong — not the Canon.

The skill is maintaining the declared meaning as the reference, and treating divergences in implementation behavior as violations to be corrected — not as evidence that the meaning should be updated to match the behavior. Post-hoc justification from implementation behavior is a canonical violation. The Canon's Constraint 4 is absolute: canonical alignment cannot be claimed after the fact.

This requires engineers to maintain access to the canonical source and to consult it when behavior is ambiguous — not to infer canonical intent from what the system currently does.

---

## Skill 3 — Making constraint violations auditable

When an implementation violates a canonical constraint — whether by accident, under pressure, or by necessity — that violation must be recorded. Not silently accepted and not silently fixed. Recorded with: what the violation is, what constraint it violates, why it was accepted, and what correction requires.

The engineering discipline here mirrors the Canon's explicit change control requirement. Silent violation is not acceptable. Recorded violation with an explicit correction path is a managed debt. The difference between the two is what makes long-lived systems maintainable.

---

## Skill 4 — Treating canonical changes as breaking changes

If the canonical model changes — new constraints, modified invariants, redefined terms — all implementations that depend on that model must be evaluated for compatibility. Canonical changes are not configuration changes. They are breaking changes by definition.

The skill is building the engineering workflow to treat them as such: canonical changes trigger a compatibility audit, not just a code update. When a constraint is added or modified, every implementation that touches the constrained behavior must be reviewed.

---

## Skill 5 — Separating semantic validity from test coverage

Test coverage verifies that implementations behave as specified. It does not verify that the specification conforms to canonical constraints. A system can have 100% test coverage and be canonically invalid.

The skill is maintaining a separate layer of structural validation — tests or checks that verify canonical constraint conformance, not just behavioral correctness. These are not the same category and should not be merged. Behavioral tests ask: does this work? Structural tests ask: is this valid?

---

## What these skills build toward

An engineering culture with these skills produces systems where: canonical constraints are respected across implementation changes, violations are never silent, implementations can be replaced without losing structural validity, and the canonical model remains the reference regardless of how many versions the implementation has gone through.

The Canon's irreversibility axiom has an engineering corollary: a structural violation that survives long enough in an implementation will be treated as a feature. Catching it before that point is the skill.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
