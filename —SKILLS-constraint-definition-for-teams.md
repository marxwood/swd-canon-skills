# Skills — Constraint Definition for Teams

**Problem space:** Teams default to building before constraining. Features get specified in terms of what they should do — not what they must not do, what is forbidden, or what conditions are binding. Constraints become implicit, encoded in tribal knowledge, and impossible to enforce consistently.

**Sources:** SWD Foundations 04, Semantics 02 + Canon Constraints 1–10, Axiom 8, Non-Negotiable 4

---

## Why constraint definition is a team discipline

Constraints are not a technical artifact that engineers define after design. They are a semantic artifact that must be defined before any surface is built — because the surface is a rendering of the constraint, not the source of it.

When teams skip constraint definition, they do not avoid constraints — they just leave them implicit. The disabled button is a constraint. The confirmation dialog is a constraint. The validation error is a constraint. All of these exist whether or not they were intentionally designed. The skill is making them intentional.

---

## Skill 1 — Writing constraints before writing requirements

Most requirement formats describe what a feature does. A constraint format describes what a feature must not do, what conditions are binding, and what is forbidden regardless of context.

The practice is: for every feature or capability being specified, write its constraints first. Not as edge cases or error handling — as primary definitions. What is the outer boundary of this capability? What must never happen? What preconditions are binding? What effects are irreversible?

This is not additional overhead. It is the work that prevents the edge cases from being discovered in production.

---

## Skill 2 — Distinguishing constraints from requirements

Requirements describe desired behavior. Constraints describe structural limits. Both are necessary; they are not the same thing.

A requirement says: "the user can publish a post." A constraint says: "a post cannot be published without an assigned author" and "a published post cannot be edited — only archived or versioned." The requirement describes the happy path. The constraint describes the boundary. Teams that only write requirements have products with undefined edges.

The practical test: can this statement be violated and still technically satisfy the requirement? If yes, it is a constraint, not a requirement. Write it separately. Make it binding.

---

## Skill 3 — Naming constraints explicitly in review

Most design and code review processes evaluate whether something works. The skill is adding a constraint layer to review: does this implementation honor all declared constraints? Does this design introduce any new implicit constraints that are not declared?

In practice: make constraints a named section of any design document, specification, or PR description. During review, ask explicitly: what constraints govern this? Are they all honored? Have any new constraints been introduced that are not yet declared?

A review process that only checks behavior will consistently miss constraint violations until they compound into incidents.

---

## Skill 4 — Maintaining a team constraint register

A constraint register is a shared, maintained record of what is forbidden, binding, and irreversible in a system. It is not a design system. It is not a backlog. It is a small, authoritative list of the structural limits that govern the product.

The register does not need to be large. It needs to be authoritative. Every constraint in it should have a name, a statement of what it prohibits, a rationale, and an owner. When a constraint is relaxed, changed, or added, that change is declared explicitly — not inferred from behavior.

Without a register, constraints exist only in the heads of senior team members. They leave, or they forget, and the constraint disappears.

---

## Skill 5 — Distinguishing guidelines from constraints

Teams often have "best practices," "design principles," and "guidelines" that are treated as suggestions. Some of these are suggestions. Some are constraints. The difference matters: a suggestion can be overridden with justification, a constraint cannot be overridden without invalidating the structure.

The skill is sorting these explicitly. For every principle, guideline, or rule the team operates by: is this a constraint (binding, no exceptions without structural consequence) or a guideline (preferred, overridable with documented justification)? Treating constraints as guidelines erodes them. Treating guidelines as constraints creates rigidity without structural basis.

---

## What these skills produce

A team with strong constraint definition has: features that do not have undefined edges, review processes that catch violations before they ship, a constraint register that survives personnel changes, and a clear shared language for the difference between what is possible and what is permitted.

The Canon's tenth constraint applies at team scale: any system claiming alignment without accepting constraints is invalid. The same is true of any product claiming coherence while leaving its constraints implicit.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
