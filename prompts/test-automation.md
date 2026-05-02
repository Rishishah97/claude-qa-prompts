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
