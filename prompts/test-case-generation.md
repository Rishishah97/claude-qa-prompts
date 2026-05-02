# 🧪 Test Case Generation Prompts

Use these prompts to generate comprehensive test cases from requirements, user stories, or feature descriptions.

---

## 1. Generate Test Cases from a User Story

**When to use:** You have a user story or acceptance criteria and need full test coverage.

```
You are a senior QA engineer. Generate a complete set of test cases for the following user story:

User Story:
[Paste your user story here]

Acceptance Criteria:
[Paste acceptance criteria here]

For each test case, include:
- Test Case ID
- Title
- Preconditions
- Test Steps (numbered)
- Expected Result
- Test Type (Positive / Negative / Edge Case)
- Priority (High / Medium / Low)

Cover happy path, negative scenarios, boundary values, and edge cases.
```

---

## 2. Generate Test Cases from a Feature Description

**When to use:** You have a high-level feature description without formal acceptance criteria.

```
You are a QA engineer. Based on the following feature description, generate a comprehensive test plan with test cases.

Feature:
[Describe the feature here]

Tech Stack (if relevant):
[e.g. React frontend, Node.js backend, PostgreSQL]

Include:
- Functional test cases
- UI/UX test cases (if applicable)
- Negative and edge cases
- Any assumptions you've made

Format each test case with: ID, Title, Steps, Expected Result, and Priority.
```

---

## 3. Expand Existing Test Cases

**When to use:** You have basic test cases and want to improve coverage.

```
Review the following test cases and expand them to improve coverage. Add missing edge cases, boundary value tests, and negative scenarios.

Existing Test Cases:
[Paste your existing test cases here]

Feature context:
[Brief description of the feature]

Return the full updated list of test cases in the same format.
```

---

## 4. Generate Test Cases for a Login / Auth Flow

**When to use:** You're testing authentication and want thorough coverage fast.

```
Generate a complete set of test cases for a user authentication flow with the following details:

- Login method: [e.g. email + password / SSO / OTP]
- Platform: [Web / Mobile / API]
- Special rules: [e.g. lockout after 5 attempts, password expiry, MFA]

Cover:
- Valid login scenarios
- Invalid credentials
- Account states (locked, unverified, expired)
- Session management
- Security scenarios (SQL injection, brute force)

Format: Test Case ID | Title | Steps | Expected Result | Priority
```

---

## 5. Generate Regression Test Suite

**When to use:** A new feature or bug fix is going out and you need to know what to regression test.

```
A new change has been made to the following area of the application:

Change Description:
[What was changed and why]

Affected Module(s):
[List modules or components]

Generate a regression test suite that covers:
- Core functionality that could be impacted
- Integration points with other modules
- Previously reported bugs in this area
- Smoke tests to run post-deployment

Format each test case with ID, Title, Steps, Expected Result, and Regression Risk (High / Medium / Low).
```
