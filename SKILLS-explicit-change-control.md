# Skills — Explicit Change Control in Fast-Moving Teams

**Use case:** Teams that ship frequently and face pressure to move fast — where undeclared changes are accumulating as structural debt.

**Sources:** Canon Axiom 6, Constraint 7, Non-Negotiable 7 + SWD DSO 12, Foundations 03

---

## The core tension

Fast-moving teams experience explicit change control as friction. The Canon's position is uncomfortable but precise: there is no implicit evolution of canonical truth. Undeclared change is invalid. Silent drift is not progress — it is debt accrual at a rate that compounds with velocity.

---

## Skill 1 — Distinguishing semantic changes from non-semantic changes

A visual update that does not alter meaning, states, or behavioral guarantees is a non-semantic change. It ships with a standard commit. A change that modifies what something means is a semantic change. It requires an explicit record. Most teams find semantic changes are a small fraction of total changes. The overhead is lower than it appears.

---

## Skill 2 — Writing the minimum viable change record

A change record must answer three questions: what changed, why it changed, and what the previous state was. A one-paragraph ADR or structured commit message with a semantic-change tag is sufficient. The format matters less than the habit. Zero records for semantic changes are debt. Long records for simple changes are waste.

---

## Skill 3 — Building the change signal into the workflow

Explicit change control fails when it is a separate process. It succeeds when the signal is embedded in the work. Add a "semantic change?" question to the PR template. Add a "meaning changed" label to the issue tracker. These are prompts that surface the question at the moment it is cheapest to answer.

---

## Skill 4 — Treating constraint relaxation as a versioned event

When a constraint is relaxed — a rule that was binding becomes optional — that is a structural event affecting every consumer. Treat it as a versioned event: what changed, what was previously prohibited that is now permitted, what downstream effects to verify.

---

## Skill 5 — Building a lightweight semantic changelog

A running record of meaning changes, separate from commit logs or release notes. Covers what semantic changes have happened, in what order, with what rationale. The investment is small. The compound return is large. Start it, maintain it forward.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
