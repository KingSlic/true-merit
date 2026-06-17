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

## Learner

A _Learner_ is the entity whose capability history is being measured.

A _Learner_ is not necessarily the same as a User account. A User is an authentication/account concept, while a Learner is the capability-bearing identity.

## Task

A Task measures a learner's capability for a Concept.

Relationships:
- Belongs to a Concept
- Has many Attempts

## Attempt

An Attempt is the record of a specific Learner performing a specific Task.

Relationships:
- Belongs to one Learner
- Belongs to one Task
- Produces many Evidence records


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


## Core Principles

- Learner owns capability history
- Task owns the challenge
- Attempt owns the performance of a Learner on a Task
- Evidence owns observation
- Rubric owns criteria
- Evaluation owns judgment
- Mastery owns concept-level capability state
- Standing owns domain-level contextual capability position
