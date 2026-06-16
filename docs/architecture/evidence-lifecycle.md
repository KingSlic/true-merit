# Evidence Lifecycle

## Entity Purpose

- Evidence represents a specific observation extracted from a learner's Attempt
- Evidence is the atomic unit of proof used by the system to evaluate capability
- Attempts contain performance
- Evidence contains observations about performance
- Rubrics evaluate Evidence
- Mastery accumulates Evidence-backed judgments over time

## Ownership

- Attempt owns the source performance
- Evidence owns extracted observations
- Rubric owns evidence interpretation
- Mastery owns long-term capability judgments
- Standing owns aggregate capability state

## Relationships

- One Attempt can produce many Evidence records
- One Evidence record belongs to one Attempt
- One Evidence record may be interpreted by multiple Rubrics, but this should be handled carefully to avoid noisy or duplicated evaluation
- Evidence should be immutable in the average case
- The Evidence record should preserve what was observed at the time it was created.
- Rubrics may change over time
- Evidence remains immutable
- New rubric versions may generate new evaluations from existing Evidence, but historical evaluations should remain preserved
- Evidence should not be rewritten to match the Rubric
- The Rubric interpretation should change, not the underlying Evidence

## Evidence Creation

Evidence may be created by multiple sources:

- learner self-assessment
- system extraction
- human audit

Learner-created Evidence represents self-perception.

System-generated Evidence represents assessment.

Human-reviewed Evidence represents verification, correction, or dispute resolution.

The Evidence source should be stored explicitly so the system can distinguish between self-perceived proof,
system-extracted proof, and human-verified proof.

## Core Principles

- Evidence is the proof of capability gleaned from a Learner's Attempt.

- Evidence is atomic.

- Evidence should be treated as an observation, not a score.

- Evidence should generally be immutable.

- Evidence may be reinterpreted by new Rubrics, but the underlying observation should remain stable.

- Without Evidence, there is no Mastery.

- Authority lives in the Evidence.

## Lifecycle

## CRUD Endpoints

## Failure Cases

## Truth Ownership

## Open Questions
