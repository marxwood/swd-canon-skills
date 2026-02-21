# Skills — Auditing Whether a Design System is Genuinely Ontological

**Use case:** Evaluating an existing design system to determine whether it expresses meaning explicitly (ontological) or is a component library with implicit semantics (cosmetic).

**Sources:** SWD DSO cluster, Foundations 03 + Canon Constraints 1, 7, Non-Negotiable 3

---

## The distinction

A component library is a collection of reusable visual elements. An ontological design system is a shared vocabulary of typed concepts with declared states, relationships, and behavioral guarantees.

---

## Audit dimension 1 — Are entities named and typed?

Does the design system name the concepts it represents, or only the components that render them? If removing the component removes the only definition of the concept, the system is purely cosmetic.

---

## Audit dimension 2 — Are states declared, not inferred?

Does the design system define entity states explicitly, or are state variants just visual treatments? If every state variant is defined only by visual appearance and not by conditions or behavioral implications, the system is tracking aesthetics, not state.

---

## Audit dimension 3 — Are constraints machine-readable?

Are the rules governing component behavior documented in a way a non-human consumer could interpret? If all constraint knowledge lives in Figma annotations or verbal team norms, the system has no machine-readable constraints.

---

## Audit dimension 4 — Are semantic changes versioned?

When a component changes behavior or meaning, is that tracked separately from visual changes? If the only versioning is visual with no semantic changelog, the system cannot explain its own history.

---

## Audit dimension 5 — Does the system have derivative separation?

Is there a clear distinction between canonical definitions in the design system and implementations derived from them? If every product team can freely redefine system components without a change process, the system has no canonical layer.

---

## Scoring

Each dimension is present or absent. Zero present = component library. All five present = operational semantic system. Recommended priority for closing gaps: entities first, then states, then constraints, then versioning, then derivative separation. The order matters because each depends on the previous.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
