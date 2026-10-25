# Spoody API — Functional Test Cases

## 1. Test Overview

**Project:** Spoody Workout Management API  
**Testing tool:** Postman  
**API environment:** JSON Server (localhost:3001)  
**Testing type:** Positive functional API testing  
**Execution method:** Postman Collection Runner

**Objective:** Verify that the workout management API supports creating, retrieving, updating, and deleting workout records.

## 2. Positive Test Scenarios

### TC-001 — Create Workout

**Method:** POST  
**Endpoint:** `/workouts`

**Test data:**
```json
{
  "userId": 1,
  "exercise": "Push Up",
  "durationMinutes": 20,
  "sets": 4,
  "repetitions": 15
}
```

**Expected result:**
- HTTP 201 Created.
- Workout record is created.
- Response contains a generated workout ID.

**Observed result:** HTTP 201 Created; workout returned with an ID.

**Status:** PASS

### TC-002 — Get Workout by ID

**Method:** GET  
**Endpoint:** `/workouts/{{workoutId}}`

**Expected result:**
- HTTP 200 OK.
- Correct workout is returned.
- Exercise name matches "Push Up".
- Response includes a workout ID.

**Observed result:** HTTP 200 OK; three automated assertions passed.

**Status:** PASS

### TC-003 — Update Workout

**Method:** PATCH  
**Endpoint:** `/workouts/{{workoutId}}`

**Test data:**
```json
{
  "durationMinutes": 30,
  "sets": 5,
  "repetitions": 20
}
```

**Expected result:**
- HTTP 200 OK.
- Updated workout values are returned.
- Workout ID remains unchanged.

**Observed result:** HTTP 200 OK; three automated assertions passed.

**Status:** PASS

### TC-004 — Delete Workout

**Method:** DELETE  
**Endpoint:** `/workouts/{{workoutId}}`

**Expected result:**
- HTTP 200 OK.
- Workout is deleted.

**Observed result:** HTTP 200 OK; deletion assertion passed.

**Status:** PASS

### TC-005 — Verify Workout Deleted

**Method:** GET  
**Endpoint:** `/workouts/{{workoutId}}`

**Expected result:**
- HTTP 404 Not Found.
- Deleted workout cannot be retrieved.

**Observed result:** HTTP 404 Not Found; deletion verification assertions passed.

**Status:** PASS

## 3. Test Execution Summary

| Metric | Result |
|---|---|
| Test scenarios | 5 |
| Automated assertions | 10 |
| Passed assertions | 10 |
| Failed assertions | 0 |
| Execution errors | 0 |

**Overall result: PASS**

The complete CRUD workflow was executed successfully using Postman Collection Runner.

## 4. Test Automation Approach

Postman JavaScript scripts were used to validate response status codes and workout data.

The workout ID returned by the POST request was saved as a collection variable and reused in subsequent requests.

This allowed the complete workflow to execute without manually copying workout IDs.

## 5. Limitations

Testing was performed against a local JSON Server mock API.

The results demonstrate functional testing of the mock API, not validation of a production backend.

## 6. Planned Negative Testing

The next phase will investigate invalid request data, missing required fields, nonexistent workout IDs, and error response behavior.

Negative test results will be documented separately after execution.
