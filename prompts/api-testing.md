# 🔌 API Testing Prompts

Use these prompts to generate API test scenarios, validate contracts, and identify edge cases for REST and GraphQL endpoints.

---

## 1. Generate API Test Cases from an Endpoint Description

**When to use:** You have an API endpoint and want full test coverage.

```
You are a senior QA engineer specialising in API testing. Generate a comprehensive set of test cases for the following API endpoint.

Endpoint:
- Method: [GET / POST / PUT / PATCH / DELETE]
- URL: [e.g. /api/v1/users/{id}]
- Auth required: [Yes / No — Bearer token / API key / OAuth]
- Request body (if applicable): [Paste JSON schema or example]
- Expected response: [Paste JSON schema or example]

Generate test cases covering:
- Happy path (valid inputs, expected 2xx responses)
- Invalid inputs (missing fields, wrong types, bad format)
- Boundary values (min/max field lengths, limits)
- Auth scenarios (missing token, expired token, wrong permissions)
- Error handling (4xx and 5xx responses)
- Edge cases specific to this endpoint

Format: Test ID | Description | Request | Expected Status Code | Expected Response | Notes
```

---

## 2. Generate Test Cases from an OpenAPI / Swagger Spec

**When to use:** You have an OpenAPI spec and want test scenarios generated from it.

```
You are a QA engineer. Based on the following OpenAPI specification, generate test cases for each endpoint.

OpenAPI Spec (or excerpt):
[Paste your OpenAPI/Swagger YAML or JSON here]

For each endpoint generate:
- At least one positive test case
- At least two negative test cases
- Auth and permission tests (if applicable)

Output as a table: Endpoint | Method | Test Description | Input | Expected Status | Expected Response
```

---

## 3. Validate Request / Response Contract

**When to use:** You want to check whether an API response matches the expected contract.

```
You are a QA engineer performing contract testing. Review the following API response and tell me if it matches the expected contract.

Expected Contract:
[Paste the expected JSON schema or agreed response format]

Actual Response Received:
[Paste the actual API response]

Identify:
- Missing fields
- Incorrect data types
- Unexpected fields
- Null values where values are expected
- Any other contract violations

Provide a clear pass/fail verdict with a breakdown of issues found.
```

---

## 4. Generate Negative and Edge Case API Tests

**When to use:** You want to stress-test an API beyond the happy path.

```
Generate negative and edge case test scenarios for the following API endpoint.

Endpoint details:
- Method: [GET / POST / PUT / PATCH / DELETE]
- URL: [endpoint URL]
- Key input fields: [list the main request parameters or body fields]
- Business rules: [any specific rules e.g. "quantity must be > 0", "email must be unique"]

Focus on:
- Empty / null / missing required fields
- Wrong data types (string instead of int, etc.)
- Boundary values (0, -1, max int, empty string, very long strings)
- Special characters and injection attempts
- Concurrent or duplicate requests
- Rate limiting and throttling scenarios

Format each test as: Test ID | Scenario | Input | Expected Status Code | Expected Error Message
```

---

## 5. Write a Postman / API Test Script

**When to use:** You want Claude to write a test script you can use directly in Postman or a test framework.

```
Write a Postman test script (or [Jest / Mocha / PyTest] test) for the following API endpoint.

Endpoint:
- Method: [GET / POST / etc.]
- URL: [endpoint]
- Auth: [type of auth]
- Request body: [example JSON]
- Expected response: [example JSON]

The script should:
- Send the request
- Assert the status code is [expected code]
- Assert specific response fields and values
- Include at least one negative test case
- Be clean, readable, and commented

Output only the code.
```

---

## 6. GraphQL API Test Cases

**When to use:** You're testing a GraphQL API and need tailored test coverage.

```
You are a QA engineer. Generate test cases for the following GraphQL query/mutation.

Query / Mutation:
[Paste your GraphQL query or mutation]

Schema context (if available):
[Paste relevant schema types]

Generate test cases covering:
- Valid queries with expected data returned
- Invalid or malformed queries
- Missing required arguments
- Permission and auth scenarios
- Large/complex nested queries (performance edge cases)
- Null handling

Format: Test ID | Description | Query/Variables | Expected Response | Notes
```
