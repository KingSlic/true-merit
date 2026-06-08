# True Merit

## Overview

True Merit is an assessment-first learning platform designed around a simple principle:

> The system should never lie to the learner.

Most learning systems measure recognition and completion. True Merit focuses on demonstrated capability through evidence, reconstruction, transfer, and performance under pressure.

The goal is not to measure whether a learner has seen information before.

The goal is to measure whether they can actually use it.

---

## Why True Merit Exists

Traditional learning systems often reward:

* Completion
* Attendance
* Recognition
* Memorization

These signals can create the illusion of understanding.

True Merit attempts to evaluate capability directly by collecting evidence of performance and tracking mastery over time.

---

## Current Technology Stack

### Backend

* FastAPI
* Python
* SQLAlchemy
* PostgreSQL
* Alembic

### Development Environment

* Docker
* Swagger / OpenAPI

---

## Current Features

### Concepts

Implemented complete CRUD functionality for Concept entities.

Supported operations:

* Create Concept
* Retrieve Concept
* Update Concept
* Delete Concept

### Tasks

Implemented complete CRUD functionality for Task entities.

Supported operations:

* Create Task
* Retrieve Task
* Update Task
* Delete Task

### Persistence

* PostgreSQL database integration
* SQLAlchemy ORM models
* Alembic migrations
* Pydantic validation

---

## Architecture

Current request flow:

Client

↓

FastAPI

↓

Pydantic Validation

↓

SQLAlchemy ORM

↓

PostgreSQL

↓

Response Serialization

↓

Client

---

## Current Development Status

Implemented:

* Concept CRUD
* Task CRUD
* PostgreSQL persistence
* SQLAlchemy integration
* Alembic migrations
* OpenAPI documentation

In Progress:

* Evidence system
* Attempt tracking
* Rubrics
* Mastery evaluation

Planned:

* Skill graph
* Standing system
* Capability scoring
* Evidence-driven progression

---

## Project Philosophy

True Merit is built around capability rather than completion.

The system is designed to evaluate whether a learner can:

* Explain
* Reconstruct
* Defend
* Transfer

their understanding rather than simply recognize information.

---

## Status

Active development.
