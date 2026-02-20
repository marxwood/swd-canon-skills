# Skills — Auditing a Product's Dual-Surface Parity

**Use case:** Evaluating whether a product's human surface and machine surface are operating from the same semantic core — or whether meaning has split between them, creating asymmetry, blind spots, and risk.

**Sources:** SWD Dual cluster, Foundations 06, Semantics 07 + Canon Axiom 4, Constraint 1, Non-Negotiable 4

---

## What dual-surface parity means

A product has dual-surface parity when: the rules governing what humans see and can do are identical to the rules governing what machines can reason about and execute. One semantic core. Two surfaces. Strict correspondence.

Parity breaks when: constraints exist only in the visual layer, meaning is encoded in UI conventions that machines cannot read, or machine interfaces expose capabilities that the human surface intentionally gates. Either direction of asymmetry is a parity violation.

---

## Audit dimension 1 — Constraint coverage

**Question:** For every behavioral constraint visible in the human surface, is there a corresponding machine-readable constraint?

**What to look for:** Disabled states correspond to explicitly declared permission conditions. Gating patterns (confirmation dialogs, warning states) correspond to declared irreversibility or risk markers. Validation errors correspond to formal constraint definitions.

**The test:** Take any visible constraint in the UI. Ask: could an agent know this constraint exists without rendering the UI? If the only source of the constraint is the visual state of a component, parity is broken.

---

## Audit dimension 2 — Capability symmetry

**Question:** Are the capabilities available to machine operators the same set as those available to human operators (modulo surface-appropriate rendering)?

**What to look for:** API endpoints that expose capabilities not accessible through the UI (shadow capabilities — risk surface for agents). UI capabilities that are not exposed in the machine layer (asymmetric availability — limits safe automation).

**The test:** Map the full capability set from the human surface against the full capability set from the machine surface. Any capability present in one but not the other is an asymmetry that needs justification or correction.

---

## Audit dimension 3 — State observability

**Question:** Can a machine operator determine the current state of any entity without rendering the human surface?

**What to look for:** Entity states that can be queried programmatically. State change events that are emitted to machine consumers. State history that is accessible through the machine interface.

**The test:** For any entity in the product, can you determine its state, its allowed transitions, and its history — without using the human-facing UI? If not, agents operating on that entity are flying blind.

---

## Audit dimension 4 — Irreversibility marking

**Question:** Are irreversible actions explicitly marked in the machine surface, or only signaled through UI friction?

**What to look for:** Capability contracts that include an explicit irreversibility flag. API responses that include outcome clarity (what changed, what is now permanent). Documentation of which actions cannot be undone.

**The test:** List all actions in the product that are irreversible (delete, publish, archive, transfer). For each: is irreversibility declared in the machine interface, or only implied by the UI? An agent that cannot detect irreversibility will execute irreversible actions with the same confidence as reversible ones.

---

## Audit dimension 5 — Permission model transparency

**Question:** Is the permission model inspectable from the machine surface?

**What to look for:** Endpoints or contracts that allow a machine operator to determine what it is permitted to do before attempting to do it. Explicit permission errors that explain why an action was forbidden, not just that it was.

**The test:** Can an agent operating on the product determine its own permission boundaries without trial and error? If an agent can only discover permissions by attempting actions and observing failures, the permission model is human-legible but not machine-transparent.

---

## Interpreting the audit

Full parity across all five dimensions is the goal, not a baseline assumption. Most products have partial parity — some dimensions are addressed, others are not. The priority is: constraints first (highest risk when absent), then irreversibility marking, then state observability, then capability symmetry, then permission transparency.

A product with broken parity is not necessarily unsafe today — it may have no agentic operators yet. But agentic operators are coming. The question is whether parity will be built intentionally before they arrive, or reverse-engineered after incidents occur.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
