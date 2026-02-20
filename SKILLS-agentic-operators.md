# Skills — Designing for Agentic Operators

**Problem space:** Products are increasingly operated by agents — automated systems, AI assistants, workflows, and scripts — not just humans. Design that assumes a human in front of a screen will fail when the operator has no screen, no visual context, and no tolerance for implicit meaning.

**Sources:** SWD Foundations 06, Dual cluster, Semantics 07 + Canon Axiom 9, Constraint 3, Non-Negotiable 4

---

## What an agentic operator is

An agentic operator is anything that can read a system, decide to act, execute a capability, and observe the result — without necessarily being human, synchronous, or visually oriented.

This includes: automated workflows triggered by events, AI assistants operating on behalf of users, scripts that integrate one system with another, orchestration layers that compose multiple products, and inference engines that reason about product state.

The critical point from SWD is that design does not get to choose whether agentic operators exist. Reality already decided. The only choice is whether the design makes agentic operation safe and explicit, or dangerous and implicit.

---

## Skill 1 — Designing capabilities as contracts, not buttons

Buttons are a human rendering of a capability. Agentic operators do not use buttons. They need the capability itself — its inputs, constraints, effects, and outputs — expressed in a form they can reason about.

The skill is separating the capability definition from its rendering. A capability contract states: what preconditions must be true, what inputs are required, what constraints apply, what effects will occur, what outputs are produced. The button is one way to invoke the contract. An API call, a workflow trigger, or an agent instruction are others.

If you cannot express the capability without reference to the button, you have not designed the capability. You have designed the button.

---

## Skill 2 — Making constraints machine-readable

Visual constraints — disabled states, warning indicators, confirmation dialogs — are human-readable encodings of rules. An agentic operator cannot read them. If the only place a constraint exists is in the visual state of a UI component, agents will violate it — not maliciously, but inevitably.

The skill is ensuring that every constraint that governs behavior is expressed in a form that does not require visual interpretation. This means: permission models that can be queried, state machines that can be inspected, action preconditions that can be checked, irreversibility markers that are structurally present — not just visually implied.

SWD's dual-surface parity rule applies directly: anything a human can understand from the UI, a machine must be able to reason about from the semantic layer. If the constraint only exists in the UI, it does not structurally exist.

---

## Skill 3 — Marking irreversibility explicitly

Human interfaces signal irreversibility through confirmation dialogs, warning states, and friction patterns. These signals are designed for human attention and judgment. Agents operate without this friction — they will execute irreversible actions with the same confidence as reversible ones unless irreversibility is marked structurally.

The skill is treating irreversibility as a first-class property of any capability, not a UI pattern. Capabilities that cannot be undone must declare this explicitly in their contract. The agent's responsibility is to honor it. The designer's responsibility is to declare it.

This is not a safety feature. It is honest design.

---

## Skill 4 — Designing observable outcomes

Agentic operators need to know what happened after an action executes. Human interfaces can communicate outcomes through visual feedback — toasts, state changes, error messages. Agents need outcomes expressed as inspectable, structured results: what changed, what the new state is, what errors occurred and why, what is now permitted or forbidden.

The skill is designing the outcome structure alongside the capability, not as an afterthought. Every capability should answer: what does success look like structurally? What does failure look like? What is the state of the affected entity after execution?

An agent that cannot observe outcomes cannot reason about what to do next. If outcomes are only communicated visually, agentic operation is effectively blind.

---

## Skill 5 — Applying the parity test

The dual-surface parity test from SWD is the clearest practical tool for evaluating agentic readiness: for every capability in the product, ask — can an agent execute this safely without seeing the UI?

If the answer is no, the gap is not a technical integration problem. It is a design problem. The meaning is incomplete. Something that should be explicit is implicit. Something that should be structured is visual. The parity test surfaces exactly where the work is.

---

## What these skills protect

A product designed for agentic operators is not a product designed for machines at the expense of humans. It is a product where meaning is honest enough to serve both. Constraints are real because they are structural, not visual. Capabilities are clear because they are contracted, not implied. Outcomes are observable because they are designed to be, not because a human can infer them from a screen.

The Canon's warning applies here with particular force: if an agent can misuse your product more easily than a human can understand it, the design is incomplete.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
