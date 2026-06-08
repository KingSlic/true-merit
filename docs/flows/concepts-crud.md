# Concepts CRUD Flow

## Purpose

The Concepts API allows creation, retrieval, updating, and deletion of Concept records within True Merit.

---

## Create Concept

Endpoint:

POST /concepts

Flow:

Client
-> FastAPI Route
-> Pydantic Request Validation
-> SQLAlchemy Model Creation
-> PostgreSQL Commit
-> Response Serialization
JSON Response

Success Result:

- New Concept stored in database
- UUID assigned
- Timestamp recorded
- Response returned to client

Failure Cases:

- Invalid request body
- Missing required fields
- Database unavailable
- Server error

---

## Get All Concepts

Endpoint:

GET /concepts

Flow:

Client
-> FastAPI Route
-> UUID validation
-> SQLAlchemy Query
-> PostgreSQLL
-> Response Serialization
-> JSON Response

Success Result:
- Requested Concept returned

Failure Cases:
- Invalid UUID (422)
- Concept not found (404)

---

## Update Concept

Endpoint:

PATCH /concepts/{id}

Flow:

Client
-> FastAPI route
-> UUID validation
-> Retrieve Existing Concept
-> Apply Updated Fields
-> Commit Changes
-> Refresh Object
-> Response Serialization
-> JSON Response

Success Result:
- Concept updated

Failure Cases:
- Invalid UUID (422)
- Concept not found (404)
- Database error

---

## Delete Concept

Endpoint:

DELETE /concepts/{id}

Flow:

Client
-> FastAPI Route
-> UUID Validation
-> Retrieve Existing Concept
-> Delete Record
-> Commit Changes
-> Success Response

Success Result:
- Concept removed

Failure Cases:
- Invalid UUID (422)
- Concept not found (404)
- Database error
