# Postman API Collections

This folder contains Postman collections used for functional API testing of the **Spoody Workout Management API**.

## Project Overview

Spoody is a practice API testing project focused on workout tracking and management.

The project uses Postman to send HTTP requests, validate API responses, and automate test assertions.

## Tools and Technologies

- Postman — API requests and automated tests
- JSON Server — Local mock REST API
- JavaScript — Postman test scripts
- JSON — Request and response data
- GitHub — Version control and documentation

## API Endpoints Tested

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/workouts` | Create a workout |
| GET | `/workouts/:id` | Retrieve a workout |
| PATCH | `/workouts/:id` | Update a workout |
| DELETE | `/workouts/:id` | Delete a workout |
| GET | `/workouts/:id` | Verify the workout was deleted |

## Positive API Testing

A complete CRUD workflow was executed using Postman Collection Runner.

**Execution results:**
- Requests executed: 5
- Automated assertions: 10
- Passed: 10
- Failed: 0
- Errors: 0

The workflow verified that a workout could be created, retrieved, updated, deleted, and subsequently return HTTP 404 when requested again.

## Test Automation

Postman scripts were used to:

- Validate HTTP status codes.
- Verify response fields and values.
- Confirm workout IDs.
- Store generated workout IDs in collection variables.
- Reuse workout IDs across requests.
- Validate successful deletion.

## Test Environment

- Base URL: `http://localhost:3001`
- API: JSON Server
- Test execution: Postman Collection Runner

The API runs locally and is not publicly hosted.

## Next Phase

Negative API testing is planned to evaluate invalid inputs, nonexistent resources, and API error handling.

Results will be documented after execution.
