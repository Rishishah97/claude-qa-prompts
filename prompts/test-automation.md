# 🤖 Test Automation & Code Review Prompts

Use these prompts to write automation scripts, review test code quality, and improve your test framework.

---

## 1. Write an Automated Test from a Manual Test Case

```
Convert the following manual test case into an automated test.

Manual Test Case:
[Paste your manual test case with steps and expected results]

Framework: [Playwright / Cypress / Selenium / Pytest / Jest / other]
Language: [JavaScript / TypeScript / Python / Java]
App type: [Web / API / Mobile]

Write clean, maintainable test code that:
- Follows the Page Object Model (if UI test)
- Uses descriptive test and variable names
- Includes appropriate assertions
- Handles waits and async behaviour correctly
- Is ready to run with minimal setup

Output only the code with inline comments.
```

---

## 2. Review Existing Test Code for Quality

```
Review the following test code and provide feedback on quality, maintainability, and best practices.

Test Code:
[Paste your test code here]

Framework / Language: [e.g. Cypress / JavaScript]

Evaluate:
- Test structure and readability
- Use of assertions (are they meaningful and specific?)
- Hardcoded values and magic numbers
- Test independence (do tests rely on each other?)
- Flakiness risks (timing issues, dynamic selectors, race conditions)
- Missing negative or edge case coverage
- Code duplication and reuse opportunities
- Naming conventions

Provide a score out of 10 and actionable improvement suggestions with refactored code examples.
```

---

## 3. Generate a Page Object Model (POM) Class

```
Generate a Page Object Model class for the following page.

Page name: [e.g. LoginPage]
Framework: [Playwright / Selenium / Cypress]
Language: [TypeScript / Python / Java]

Page elements:
[List the key UI elements — e.g. email input, password input, login button, error message]

Actions on this page:
[List the actions — e.g. login with valid credentials, login with invalid credentials, click forgot password]

Write a clean POM class with:
- Element locators as private properties
- Public action methods
- Assertions within action methods where appropriate
- JSDoc or docstring comments
```

---

## 4. Identify and Fix Flaky Tests

```
Analyse the following test and help me identify why it might be flaky and how to fix it.

Test Code:
[Paste the flaky test code]

Known failure pattern:
[Describe when and how it fails — e.g. "fails on CI 1 in 5 runs", "fails after a slow network"]

Check for:
- Race conditions and improper waits (e.g. fixed sleep vs dynamic waits)
- Element selectors that are fragile or dynamic
- Test data dependencies or shared state
- Order-dependent tests
- Environment-specific issues

Provide a fixed version of the test with an explanation of each change.
```

---

## 5. Generate a Test Automation Strategy

```
Create a test automation strategy for the following project.

Project:
[Describe the application, team size, release cadence, and current test coverage]

Tech stack: [Frontend, backend, mobile frameworks]
CI/CD: [e.g. GitHub Actions, Jenkins, CircleCI]
Current pain points: [e.g. slow test suite, high flakiness, no API tests]

Include:
- Recommended test pyramid (unit / integration / E2E split)
- Tools and frameworks to use and why
- What to automate vs keep manual
- Folder structure and naming conventions
- CI/CD integration approach
- Metrics to track (coverage, pass rate, execution time)
- Rollout plan (phased approach)
```

---

## 6. Generate a Cypress E2E Test Suite

```
Write a Cypress end-to-end test suite for the following user journey.

User Journey:
[Describe the full flow step by step — e.g. register → verify email → login → complete profile]

App URL: [base URL]
Auth method: [how to handle login in tests]

Write tests that:
- Use cy.intercept() to stub or assert API calls where appropriate
- Use custom commands for repeated actions (e.g. cy.login())
- Follow the Page Object or App Actions pattern
- Have meaningful describe/it block names
- Run independently (no shared state between tests)
- Include assertions on UI and network responses

Output clean TypeScript code.
```

---

## 7. Write a Playwright API + UI Combined Test

```
Write a Playwright test that combines API setup with UI verification for the following scenario.

Scenario:
[Describe the test — e.g. create a resource via API, then verify it appears in the UI]

Base URL: [app URL]
API endpoint: [endpoint to call for setup/teardown]
Auth: [token or session details]

The test should:
- Use the API to set up test data (not the UI)
- Perform UI actions to verify the feature
- Use the API to clean up test data after the test
- Be written in TypeScript with Playwright best practices

Output the full test file.
```

---

## 8. Generate a Test Data Factory

```
Create a test data factory for the following entities used in automated tests.

Entities:
[List the data models — e.g. User, Order, Product — with their key fields and types]

Language / Framework: [TypeScript / Python / Java]

The factory should:
- Generate realistic random data using a library like Faker
- Allow overrides for specific fields
- Support creating related entities (e.g. Order with User and Products)
- Have a clean, reusable API
- Include examples of usage in tests

Output the factory code with usage examples.
```

---

## 9. Write a CI/CD Pipeline for Test Automation

```
Write a CI/CD pipeline configuration to run the following test suite automatically.

Test suite:
[Describe the tests — type, framework, language, approximate count]

CI tool: [GitHub Actions / GitLab CI / CircleCI / Jenkins]
Trigger: [on PR / on merge to main / scheduled / all of the above]

Pipeline should:
- Install dependencies and cache them
- Run linting and type checks before tests
- Run tests in parallel where possible
- Generate and publish a test report
- Fail the build on test failures
- Send a notification on failure (Slack / email)
- Run a subset of tests on PR and full suite on merge

Output the complete pipeline YAML.
```

---

## 10. Audit a Test Suite for Coverage Gaps

```
Audit the following test suite and identify coverage gaps.

Existing tests:
[Paste a list or summary of your current automated tests]

Application features:
[List the key features and user journeys of the application]

Identify:
- Features with no automated test coverage
- User journeys only partially covered
- Missing negative and error path tests
- Integration points not covered
- Tests that duplicate each other (candidates for removal)
- Recommended priority order for filling gaps

Output a gap analysis table and a prioritised action plan.
```
