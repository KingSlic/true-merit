# Attempt Lifecycle

## 1. Purpose

An 'Attempt' represents a learner's response to a Task.

Tasks define what the learner is being asked to do. Attempts capture what the learner actually submits.

Without Attempts, True Merit can define Concepts and Tasks, but it cannot collect evidence of capability.

---

## 2. Attempt Fields

A minimal Attempt should include:

- `id`
- `task_id`
- `response`
- `confidence`
- `created_at`

### id

Unique identifier for the Attempt.

### task_id

Foreign key linking the Attempt to the Task being answered.

### response

The learner's submitted answer, explanation, reconstruction, or performance artifact.

### confidence

The learner's self-reported confidence in their response

### created_at

Timestamp recording when the Attempt was created.

---

## 3. Relationships

A Task can have many Attempts.

An Attempt belongs to one Task.

This creates the relationship:

```txt
Task
└── Attempt
