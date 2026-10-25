# Negative API Testing — Spoody

## Objective

Evaluate how the Spoody mock workout API responds to invalid or incomplete requests using Postman and JavaScript assertions.

## Test Cases

| Test ID | Scenario | Expected / Observed Result | Status |
|---|---|---|---|
| NEG-01 | Retrieve a nonexistent workout | 404 Not Found | Passed |
| NEG-02 | Create a workout with missing fields | Mock API accepted the request with 201 Created | Passed — behavior documented |
| CLEANUP-01 | Delete the incomplete workout | 200 OK | Passed |
| VERIFY-01 | Retrieve the deleted workout | 404 Not Found | Passed |

## Key Finding — Missing Field Validation

The POST `/workouts` endpoint accepted a workout without `durationMinutes`, `sets`, or `repetitions`.

JSON Server does not enforce required-field validation by default. Therefore, this behavior is documented as a mock API validation limitation, not a confirmed production defect.

A production API with mandatory fields would be expected to reject incomplete requests according to its defined validation requirements.

## Automation

Postman collection variables were used to store dynamically generated workout IDs. Cleanup and verification requests reused these IDs to support repeatable testing.

## Results

- Requests executed: 4
- Assertions passed: 7
- Assertions failed: 0
- Request errors: 0

All four requests were executed successfully in a single Postman collection run.
