# Transferable Skills — Semantic Web Design & System Momentum Canon

This document defines the skills that emerge from Semantic Web Design (SWD) and the System Momentum Canon. These are not two skill sets. They are one discipline operating at two layers: SWD is the design theory, the Canon is its structural formalization. The skills below span both, in the order you need them.

---

## The foundational shift

Before the skills, the shift. Every skill in this document depends on accepting one thing:

**Meaning is the primary artifact. Everything else is a projection.**

SWD calls it meaning-first design. The Canon calls it structural truth. They are the same claim at different levels of abstraction. A screen is a projection of meaning. A UI flow is a projection of a state graph. A component library is a projection of an ontology. A governance manual is a projection of canonical constraints.

If you design projections without designing the thing they project from, the system will drift. Every skill here exists to prevent that.

---

## Skill 1 — Entity-First Thinking

**Source:** SWD Foundations + Semantics cluster

The ability to identify, name, and model the things that persist in a system — independent of how they are displayed.

An entity is anything that has identity, can change state, participates in relationships, and can be acted upon. Everything in a product is already an entity. The skill is making that explicit rather than letting it be inferred from screens.

In practice this means: before designing any surface, ask what entity this surface is about. Name it precisely. Define its states. Map its relationships. Once that is clear, the surface becomes derivable. Without it, every new screen is a handcrafted exception.

This applies equally to designers, engineers, and anyone who governs a system. If you cannot name the entities, you do not yet understand the system.

---

## Skill 2 — Constraint-First Design

**Source:** SWD Foundations 04 + Canon Constraints 1–10

The ability to define what is not allowed before defining what to build.

Most design and engineering practice starts with goals: what should this do, what should this look like. Constraint-first design starts with boundaries: what must not happen, what cannot be changed, what is forbidden regardless of outcome.

The Canon is explicit: optimization without constraints amplifies invalid structures. SWD says the same thing differently — a capability declaration without constraints is interaction theater. You are not designing behavior; you are decorating it.

In practice: before specifying a feature, write its constraints. Before building a capability, state what it must not do. Before releasing a design, ask what has been prohibited — not just what has been permitted.

This is the inversion that separates rigorous system thinking from wishful goal-setting.

---

## Skill 3 — Structural Validity Thinking

**Source:** Canon Axioms 1–3 + SWD Foundations 02–03

The ability to separate whether something is structurally valid from whether it is working.

A system can perform well and be structurally invalid. Widespread adoption does not imply correctness. Success does not retroactively legitimize a violated constraint. These are not abstract principles — they are the most common failure mode in complex systems: things that work for a long time while accumulating structural debt, until they collapse.

The skill is asking a different question before evaluating performance: is the structure itself valid? Does it conform to its invariants? Are its constraints being honored? If not, performance is noise. You are optimizing a broken thing.

Applied to SWD: does the design system express meaning, or just visual consistency? Applied to the Canon: does the system conform to canonical constraints, or just claim alignment?

---

## Skill 4 — Design as Contract

**Source:** SWD Foundations 04 + Canon Non-Negotiables

The ability to express what a product or feature guarantees — not just what it shows.

A contract is a set of enforceable statements: what exists, what can be done, what must not happen, what is guaranteed after an action, what can be inspected. This is already in every UI, but encoded implicitly — in disabled buttons, confirmation dialogs, error states, empty states. SWD makes those encodings explicit. The Canon makes them binding.

The skill is learning to write contracts before rendering surfaces. A capability contract names its inputs, constraints, effects, and outputs. A state contract names its preconditions, allowed transitions, and forbidden paths. Once these exist, the UI becomes a rendering layer — changeable without breaking coherence.

This is not more work. It is work that scales. Visual-only design accrues debt silently. Contract-based design makes debt visible.

---

## Skill 5 — Hierarchical Truth Management

**Source:** Canon Canonical Hierarchy + SWD DSO cluster

The ability to maintain a clear, non-negotiable source of truth at the top of a system, and ensure everything below it is derived from — not equivalent to — that source.

In SWD terms: the semantic core is the source. Components, surfaces, and flows are projections. A projection cannot redefine its source. In Canon terms: the Core is the invariant layer. Institutional realizations, domain extensions, and implementations project downward from it. No lower-level artifact may project truth upward.

The practical version of this skill is recognizing truth drift — when a derivative starts being treated as the source. When a component library becomes the definition of the design system. When an implementation's behavior becomes the definition of the product. When a team's practice becomes the definition of the rule.

Managing hierarchical truth means continuously asking: what is this derived from, and is the derivation still valid?

---

## Skill 6 — Responsibility Localization

**Source:** Canon Axiom 7 + SWD Ops 01

The ability to ensure that judgment and accountability always have a named location — a person, a team, a function — and that diffused responsibility is recognized as a structural failure.

The Canon is absolute on this: where responsibility is diffused, correction collapses. SWD says the same thing from the governance angle: if meaning has no owner, definitions drift, rules conflict, and trust erodes.

This is one of the most transferable skills in leadership and system design. It does not mean centralizing authority. It means ensuring every decision has a decider, every constraint has a custodian, every semantic change has a reviewer. Distributed systems can have localized responsibility. The two are not in conflict.

In practice: for any rule, constraint, or definition in your system, you should be able to name who is responsible for it. If you cannot, the system is already drifting.

---

## Skill 7 — Dual-Surface Awareness

**Source:** SWD Dual cluster

The ability to design for human and machine operators simultaneously, from the same semantic core.

Every serious product today is operated by humans, scripts, workflows, and agents. A design that only serves human comprehension creates asymmetry — machines will infer meaning from visual conventions, and they will infer it wrong.

The parity rule from SWD is sharp: anything a human can do, a machine must be able to reason about. Anything a machine can do, a human must be able to understand. Breaking this creates blind spots in both directions.

The skill is holding both surfaces in mind during design, not adding machine-readability as an afterthought. Constraints must be explicit, not hidden in UI conventions. Irreversible actions must be marked. Permission models must be inspectable. States must be named.

This is not designing for machines. It is designing honestly.

---

## Skill 8 — Graph Navigation Thinking

**Source:** SWD GraphNav cluster

The ability to replace linear, hierarchical mental models of navigation with relational ones.

Hierarchies assume a single correct path. Real products violate this constantly — entities relate in multiple ways, users arrive from anywhere, goals change mid-session. Navigation designed as a tree collapses under real use. Navigation designed as a graph reflects how people actually think and how agents actually reason.

The shift in practice: stop asking where does this page live in the hierarchy, start asking what is this connected to and what edges make sense from here. Every view should answer: what entity is this about, what relationships are relevant, what actions make sense now, where can I go that preserves meaning.

This applies to information architecture, documentation systems, knowledge bases, and any product where discovery matters.

---

## Skill 9 — Explicit Change Control

**Source:** Canon Axiom 6 + Constraint 7 + SWD DSO 12

The discipline of making change declared rather than drifted into.

The Canon is absolute: silent evolution is not evolution. There is no implicit change to canonical truth. SWD frames it as semantic drift — when components look the same but mean different things, when states are renamed without acknowledging the behavioral change, when constraints are relaxed without a record.

The skill is treating undeclared change as invalid by default. All changes must be explicit, intentional, and declared. This means versioning decisions, writing change rationale, and building systems where meaning changes are reviewable — not inferred from diffs.

Applied broadly: this is the discipline behind good ADRs, changelog practices, semantic versioning, and any governance model that wants to survive contact with time.

---

## Skill 10 — Misuse Pattern Recognition

**Source:** Canon 07–15 + SWD Foundations 03 + Epilogue

The ability to recognize when a framework, rule system, or constraint set is being used as a shield, shortcut, or source of authority — rather than as a genuine constraint.

The Canon devotes significant space to this because well-intentioned actors are the most dangerous misusers. Outsourcing decisions to the Canon. Using it to justify authority. Treating it as intelligence. Claiming alignment without accepting constraints. These are not bad-faith attacks; they are the natural failure modes of anyone who wants to use a rigorous system without doing the rigorous work.

SWD names the equivalent: visual consistency as a substitute for semantic consistency. Component libraries claimed as design systems. Governance processes that document meaning without owning it.

The skill is recognizing these patterns in yourself and your systems before they calcify. A framework that is used to avoid judgment has already been misused. A constraint that is invoked to claim authority has already been violated.

---

## Skill 11 — Binary Validity Judgment

**Source:** Canon Non-Negotiable 10 + SWD Foundations 02

The discipline of not accepting partial validity as a category.

Within scope, something is either valid or it is not. Partial alignment does not exist. You cannot be mostly canonical. You cannot be somewhat semantically coherent. Validity is binary — not as an aesthetic preference, but because partial validity is the mechanism by which violations accumulate.

The practical skill is learning to resist the pressure to accept "close enough." In code review: does this conform to the constraint or not? In design review: does this expose meaning explicitly or does it encode it implicitly? In governance: does this change have explicit authorization or not?

Accepting partial validity once creates a precedent. Precedents become norms. Norms become the new baseline. Binary judgment is not inflexibility — it is what keeps the baseline from drifting.

---

## Skill 12 — Separating Adoption from Validity

**Source:** Canon Axiom 3 + SWD Foundations 01

The ability to resist social proof when evaluating structural correctness.

Widespread use does not imply validity. Consensus does not legitimize a canonical violation. Success cannot retroactively correct a broken structure. These are not contrarian positions — they are the recognition that adoption is a behavioral signal and validity is a structural property, and the two are independent.

In practice: the most dangerous structural violations are the ones that work. They accumulate adoption, they build institutional momentum, they become load-bearing. When they eventually fail, they fail catastrophically — because no one was willing to call them invalid while they were succeeding.

The skill is maintaining the question: is this structurally valid — separate from whether it is performing, whether people like it, whether it has stakeholder buy-in. Performance answers are not validity answers.

---

## How to use these skills

These twelve skills are not a checklist. They are a coherent mental model that reinforces itself: entity-first thinking makes constraint-first design possible. Constraint-first design enables binary validity judgment. Binary validity judgment prevents adoption from being mistaken for validity. Hierarchical truth management gives explicit change control something to protect. Responsibility localization gives governance somewhere to live.

The entry point depends on where you are working. If you are designing products, start with Skill 1 and Skill 7. If you are governing systems, start with Skill 5 and Skill 6. If you are building frameworks or canons, start with Skill 2 and Skill 10.

The goal is not coverage by sequence. The goal is coverage by connectivity — until the model holds as a whole.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
