# Request Lifecycle

## Purpose

This document explains the standard backend request lifecycle in True Merit.

It describes how a client request moves through FastAPI, validation, database interaction, and response serialization.

---

## Standard Flow

Client
-> FastAPI Route
-> Pydantic Validation
-> Database Session
-> SQLAlchemy ORM
-> PostgreSQL
-> Commit / Query Result
-> ORM Object
-> Pydantic Response Schema
-> JSON Response
-> Client

---

## Step-by-Step Explanation

### 1. Client Sends Request

A client sends an HTTP request to a True Merit API endpoint

Examples:

- POST /concepts
- GET /concepts
- PATCH /concepts/{id}
- DELETE /concepts/{id}

---

### 2. FastAPI Routes The Request

FastAPI matches the request method and URL path to the correct route function.

Example:

POST /concepts is routed to the function responsible for creating a Concept.

---

### 3. Pydantic Validates Input

Pydantic validates the incoming requets body and path parameters.

If validation fails, FastAPI returns a 422 response before the request reaches database logic.

---

### 4. Database Session Is Created

The backend provides a database session to the route.

This session is the active connection between the request-handling code and PostgreSQL through SQLAlchemy.

---

### 5. SQLAlchemy Creates or Queries ORM Objects

SQLAlchemy is used to create, retrieve, update, or delete ORM model instances

Examples:

- Creating a Concept model instance
- Querying for a Concept by ID
- Updating Concept fields
- Deleting a Concept record

---

### 6. PostgreSQL Stores or Retrieves Data

PostgreSQL is the source of truth for persisted application data.

SQLAlchemy communicates with PostgreSQL to commit changes or retrieve records.

---

### 7. Commit Finalizes Mutations

For create, update, and delete operations, the database transaction must be committed before changes become persistent.

Without commit, changes may exist only temporarily in the session but are not permanently stored.

---

### 8. Refresh Updates ORM State

After creating or updating a record, the ORM object may be refreshed so it reflects database-generated values such as IDs or timestamps.

---

### 9. Pydantic Serializes the Response

The ORM object is converted into the expected response schema.

This ensures the client receives structured JSON rather than raw database objects.

---

### 10. Client Receives JSON Response

FastAPI returns the serialized response to the client

The client receives either:

- A success response
- A validation error
- A not-found error
- A server error

---

## Common Success Responses

### Create

A new entity is stored and returned.

### Read

One or more entities are retrieved and returned.

### Delete

An entity is removed and deletion is confirmed.

---

## Common Failure Responses

### 422 Validation Error

Returned when the request body or path parameter does not match the expected schema.

Example:

- Invalid UUID
- Missing required field
- Wrong data type

---

### 404 Not Found

Returned when the request is valid but the requested resource does not exist.

Example:

- Concept ID is valid but no matching Concept exists

---

### 500 Server Error

Returned when an unexpected backend failure occurs.

Example:

- Database unavailable
- Unhandled exception
- Misconfigured backend logic

---

## Ownership Boundaries

### FastAPI Owns

- Routing
- Request handling
- Response dispatch

### Pydantic Owns

- Input validation
- Output schema enforcement

### SQLAlchemy Owns

- ORM object mapping
- Database session interaction

### PostgreSQL Owns

- Persisted data truth

### Application Logic Owns

- Business rules
- Error handling
- Relationship behavior

