# Skills — Governing Semantic Drift

**Problem space:** Meaning in a system changes without anyone deciding to change it. Components accumulate divergent behavior. Rules shift through practice. Teams stop agreeing on what things mean. By the time the drift is visible, the damage is structural.

**Sources:** SWD Foundations 03, DSO 06, DSO 12 + Canon Axiom 6, Constraint 7, Non-Negotiable 7

---

## What semantic drift is

Semantic drift is not a bug. It is the default behavior of any system where meaning is implicit. When meaning lives in people's heads, in visual conventions, in informal team norms — it moves. People leave, contexts change, implementations diverge. The system continues to function visually while becoming incoherent semantically.

SWD names this directly: visual debt is visible and annoying, semantic debt is invisible and catastrophic. The Canon names the structural equivalent: silent evolution is not evolution. Undeclared change is invalid. Both are saying the same thing — drift is not neutral, it is a violation that accumulates interest.

---

## Skill 1 — Recognizing drift before it is visible

Drift has early signals that precede visible inconsistency. The skill is reading them.

Early signals include: teams using the same term to mean different things in different contexts; components that look identical but trigger different behaviors; rules that are stated one way and practiced another; onboarding that relies on oral tradition rather than documented meaning; automation that requires reverse-engineering the UI to understand intent.

None of these feel like emergencies. That is what makes them dangerous. The skill is treating any gap between stated meaning and practiced meaning as an active drift signal — not a cosmetic issue to address later.

---

## Skill 2 — Naming meaning before building anything

Drift begins at the moment something is built without its meaning being declared. The preventive skill is establishing named, typed meaning as a prerequisite for building — not a documentation task that follows it.

In practice: before a component is added to a design system, its concept must be named. Before a state is added to an entity, its conditions and transitions must be declared. Before a constraint is relaxed, the relaxation must be recorded. The act of naming is not overhead. It is the thing that makes the system governable later.

If you cannot name it, you are not ready to build it.

---

## Skill 3 — Distinguishing semantic change from visual change

Most teams have change management for visual and behavioral changes. Almost none have it for semantic changes — changes to what something means, as opposed to how it looks or what it does.

The skill is maintaining this distinction explicitly. A component can change visually without changing semantically. A component can also change semantically without changing visually — and this second case is the dangerous one, because it is invisible to standard review processes.

The question to ask of any change: did the meaning change? If yes, that is a semantic change and requires semantic review — regardless of whether the visual output changed.

---

## Skill 4 — Owning a canonical vocabulary

Drift accelerates when a system has no authoritative vocabulary — when terms can be defined locally, redefined by convention, or used inconsistently across teams without consequence.

The skill is establishing and maintaining a canonical vocabulary: a set of terms whose definitions are owned, versioned, and binding. This does not have to be large. It has to be authoritative. When a term in the vocabulary is used, it means what the vocabulary says it means — not what the local context implies.

The Canon's constraint is absolute: canonical meaning must not be redefined through consensus, usage, or aggregation. The same principle applies at any scale. Vocabulary without ownership is not vocabulary. It is suggestion.

---

## Skill 5 — Making drift correction explicit

When drift is discovered and corrected, the correction must itself be declared — not silently fixed. Silent correction continues the pattern that caused the drift. It does not create a record of what changed, why, or what the correct meaning now is.

Explicit correction means: naming the drift, stating the original intent, declaring the corrected meaning, and versioning the change. This is the same discipline as explicit change control, applied retroactively. It is more expensive than silent correction in the short term. It is the only correction that does not recur.

---

## What these skills protect

A system governed against semantic drift is one where: meaning changes are reviewable, not inferred; components mean what they say they mean; automation can rely on explicit constraints rather than guessing from visual patterns; onboarding is documentation-first, not oral tradition; and structural failures are caught before they become performance failures.

The Canon's closing position applies here directly: reality may diverge, but the Canon remains valid. The same is true of a well-governed semantic system — implementations may drift, but the declared meaning remains the reference. Correction is always possible because the standard is always clear.

---

*Grounded in: [Semantic Web Design](https://github.com/marxwood/semantic-web-design) and the [System Momentum Canon](https://github.com/marxwood/system-momentum-canon)*
