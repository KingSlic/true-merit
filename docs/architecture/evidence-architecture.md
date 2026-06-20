# Evidence Architecture

## Purpose

Evidence exists to preserve observations about learner performance.

Evidence records what happened during an Attempt.

Evidence does not determine what those observations mean.

Interpretation belongs to Evaluation.

Evidence exists so that judgments can be revisited, challenged, re-evaluated, and reinterpreted over time.

---

## Evidence Ownership

Evidence belongs to an Attempt.

An Attempt produces Evidence.

Evidence cannot exist without an originating Attempt.

An Attempt may produce many Evidence records.

---

## Evidence Truths

Evidence records reality.

Evidence does not own interpretation.

Evidence remains immutable.

Evidence may be evaluated many times.

Evidence may support multiple evaluations.

Evidence may outlive any individual evaluation.

---

## Evidence Creation

Evidence is created whenever an Attempt generates an observable signal.

Examples include:

- Learner responses
- Code submissions
- Explanations
- Reconstructions
- Transfer attempts
- Failure analyses
- Confidence statements

Evidence should be atomic whenever possible.

Each record should preserve a single meaningful observation.

---

## Evidence Immutability

Evidence represents historical reality.

Historical reality must not change.

Evidence records should never be edited after creation.

If additional information becomes available, new Evidence records should be created.

Truth should accumulate rather than mutate.

---

## Evidence Relationships

```text
Attempt
  ↓
Evidence
  ↓
Evaluation
  ↓
Mastery
```

Attempts generate Evidence.

Evaluations interpret Evidence.

Mastery accumulates interpreted Evidence over time.

Evidence acts as the bridge between performance and judgment.

---

## Evidence vs Attempt

Attempt owns performance.

Evidence owns observations.

Attempt answers:

"What happened?"

Evidence answers:

"What did we observe?"

An Attempt may contain many observations.

Each observation should be preserved independently.

---

## Evidence vs Evaluation

Evidence preserves observations.

Evaluation preserves judgment.

Evidence answers:

"What was observed?"

Evaluation answers:

"What does it mean?"

Evidence should remain unchanged even when evaluations change.

---

## Evidence Versioning Philosophy

Evidence itself should not be versioned.

Evidence represents a historical fact.

If reality changes, a new Evidence record should be created.

Versioning belongs to Rubrics and Evaluations, not Evidence.

The past should remain auditable.

---

## Evidence Principles

- Evidence begins with observation.
- Evidence is not judgment.
- Evidence is immutable.
- Evidence supports explainability.
- Evidence should remain interpretable by future systems.
- Evidence enables re-evaluation.
- Evidence preserves the path to mastery.
