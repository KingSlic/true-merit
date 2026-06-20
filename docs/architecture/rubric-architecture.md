# Rubric Architecture

## Purpose

Rubrics define how Evidence should be interpreted.

Rubrics establish standards for capability evaluation.

A Rubric provides the framework used to determine whether Evidence demonstrates a capability.

Rubrics own expectations.

They do not own observations.

---

## Rubric Ownership

Rubrics belong to Tasks.

A Task defines the challenge.

A Rubric defines how success should be evaluated.

Multiple Tasks may share similar Rubrics.

A Task may contain multiple Rubrics.

---

## Rubric Versioning

Rubrics should be versioned.

Evaluation standards evolve over time.

Historical evaluations must remain tied to the Rubric version used at the time of judgment.

New Rubric versions should create new evaluations rather than overwrite previous judgments.

Truth should accumulate rather than disappear.

---

## Capability Types

Capability Types define what is being evaluated.

Examples include:

- Reconstruction
- Transfer
- Reasoning
- Independence
- Failure Awareness

Capability Types should remain relatively stable.

They represent long-term capability categories rather than temporary evaluation criteria.

---

## Criteria

Criteria are observable indicators of capability.

Criteria translate abstract capabilities into measurable signals.

Criteria provide evaluators with specific evidence to look for.

Examples include:

- Correct terminology usage
- Causal reasoning
- Execution flow understanding
- Failure case identification
- Independent problem solving

Criteria may vary between Rubrics.

---

## Criteria Definitions

Capability Type:

"What capability are we evaluating?"

Criterion:

"What observable behavior indicates that capability?"

Capability Types are broad.

Criteria are specific.

Capability Types remain relatively stable.

Criteria may evolve.

---

## Rubric Relationships

```text
Task
  ↓
Rubric
  ↓
Evaluation
  ↓
Mastery
```

Tasks own challenges.

Rubrics define standards.

Evaluations apply standards.

Mastery accumulates judgments.

A single Rubric may evaluate many Evidence records.

A single Evidence record may be evaluated by multiple Rubrics.

---

## Rubric Principles

- Rubrics define standards.
- Rubrics own expectations.
- Criteria are observable indicators of capability.
- Capability Types are stable.
- Criteria may evolve.
- Rubrics should be versioned.
- Rubrics enable explainable evaluation.
- Rubrics preserve evaluation consistency.
