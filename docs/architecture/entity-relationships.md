# Entity Relationships

Concept
└── Task
    └── Attempt
        └── Evidence
            └── Rubric Evaluation
                    └── Mastery State

Mastery States
└── Standing


## Concept

A Concept represents a unit of knowledge or skill.

Relationships:
- Has many Tasks

## Task

A Task measures a learner's capability for a Concept.

Relationships:
- Belongs to a Concept
- Has many Attempts

## Attempt

A learner response to a Task.

Relationships:
- Belongs to a Task
- Produces Evidence

## Evidence

Observable proof extracted from an Attempt.

Relationships:
- Produced by an Attempt
- Evaluated by a Rubric

## Rubric

Defines evaluation criteria.

Relationships:
- Evaluates Evidence
- Updates Mastery State

## Mastery State

Current demonstrated capability level.

Relationships:
- Updated by Rubric evaluations
- Contributes to Standing

## Standing

Aggregate view of learner capability across Concepts.
