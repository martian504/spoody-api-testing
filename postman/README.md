# Spoody — API Testing Project

A hands-on API testing portfolio project focused on validating workout management functionality using Postman, JavaScript, and JSON Server.

## Project Overview

Spoody is a fitness workout tracking API testing project designed to develop practical skills in API testing, test automation, debugging, and quality assurance.

The project demonstrates how REST API endpoints can be tested through structured test cases and automated assertions.

## Technologies and Tools

- **Postman:** API testing and collection execution
- **JavaScript:** Automated test scripts
- **JSON Server:** Local mock REST API
- **JSON:** Request and response data
- **GitHub:** Documentation and version control

## API Functionalities

The project covers workout management operations:

| HTTP Method | Endpoint | Description |
|---|---|---|
| POST | `/workouts` | Create a workout |
| GET | `/workouts/:id` | Retrieve a workout |
| PATCH | `/workouts/:id` | Update workout details |
| DELETE | `/workouts/:id` | Delete a workout |
| GET | `/workouts/:id` | Verify workout deletion |

## Positive API Testing Results

The complete workout management workflow was tested using Postman Collection Runner.

| Metric | Result |
|---|---|
| API requests | 5 |
| Automated assertions | 10 |
| Passed | 10 |
| Failed | 0 |
| Execution errors | 0 |

**Result:** All 10 automated assertions passed.

### Tested Workflow

1. Create a workout using POST.
2. Retrieve the created workout using GET.
3. Update workout details using PATCH.
4. Delete the workout using DELETE.
5. Verify deletion using GET and expect HTTP 404.

Generated workout IDs were stored as Postman collection variables and reused throughout the workflow.

## Test Environment

The project currently uses a local JSON Server instance.

Base URL: `http://localhost:3001`

The API is not publicly deployed.

## Project Structure

- `README.md` — Main project documentation
- `postman/` — Postman collections and documentation
- `LICENSE` — MIT license

Additional test documentation and evidence will be organized as the project develops.

## Next Steps

- Implement negative API test scenarios.
- Test invalid request data.
- Validate error responses.
- Document test cases and defects.
- Expand automated test coverage.

## Learning Objectives

This project is part of a practical learning portfolio aimed at developing:

- REST API testing
- HTTP methods and status codes
- Test case design
- JavaScript assertions
- Test automation
- Debugging and defect reporting
- Technical documentation

## License

This project is licensed under the MIT License.
