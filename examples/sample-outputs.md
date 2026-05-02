# 📄 Sample Outputs

Real examples of Claude's output using the prompts in this repo. Use these as a reference for what to expect.

---

## Example 1: Test Case Generation

**Prompt used:** [Generate Test Cases from a User Story](../prompts/test-case-generation.md#1-generate-test-cases-from-a-user-story)

**Input:**
> User Story: As a registered user, I want to reset my password via email so that I can regain access to my account if I forget my password.
> Acceptance Criteria: User receives a reset link within 2 minutes. Link expires after 60 minutes. New password must meet complexity rules.

**Claude's Output:**

| Test ID | Title | Steps | Expected Result | Type | Priority |
|---------|-------|-------|-----------------|------|----------|
| TC-001 | Successful password reset | 1. Click "Forgot Password" 2. Enter valid email 3. Check inbox 4. Click reset link 5. Enter new valid password | Password updated, user redirected to login | Positive | High |
| TC-002 | Reset email not received for unregistered email | Enter unregistered email on forgot password page | No email sent, generic message shown (no user enumeration) | Negative | High |
| TC-003 | Reset link expires after 60 minutes | Request reset link, wait 61 minutes, click link | Error shown: "Link has expired. Please request a new one." | Edge Case | High |
| TC-004 | Password fails complexity rules | Enter a password of only 4 characters | Inline validation error shown, form not submitted | Negative | Medium |
| TC-005 | Reset link can only be used once | Use reset link, reset password, click link again | Error shown: "Link has already been used." | Edge Case | Medium |
| TC-006 | Reset email arrives within 2 minutes | Request reset link and start timer | Email received within 2 minutes | Positive | Medium |

---

## Example 2: Bug Report

**Prompt used:** [Write a Structured Bug Report](../prompts/bug-reporting.md#1-write-a-structured-bug-report)

**Input:**
> The checkout button disappears when I add more than 10 items to the cart on mobile.

**Claude's Output:**

**Title:** Checkout button disappears when cart contains more than 10 items on mobile

**Environment:**
- Device: iPhone 14 Pro
- OS: iOS 17.2
- Browser: Safari 17
- App Version: 3.4.1

**Severity:** High
**Priority:** P2

**Steps to Reproduce:**
1. Log in to the app on a mobile device
2. Browse products and add 10 items to the cart
3. Add an 11th item to the cart
4. Navigate to the cart page

**Expected Result:**
The "Proceed to Checkout" button is visible and tappable regardless of cart item count.

**Actual Result:**
The "Proceed to Checkout" button disappears from the cart page when 11 or more items are in the cart. Users cannot complete a purchase.

**Attachments Needed:** Screenshot of cart with 10 items (button visible) vs 11 items (button missing), browser console logs.

**Possible Root Cause:** The cart UI may have a max-height constraint or overflow issue causing the button to render off-screen on smaller viewports when the item list grows.

---

## Example 3: API Test Cases

**Prompt used:** [Generate API Test Cases from an Endpoint Description](../prompts/api-testing.md#1-generate-api-test-cases-from-an-endpoint-description)

**Input:**
> POST /api/v1/users — creates a new user. Requires: name (string), email (string), role (admin/user). Returns 201 on success.

**Claude's Output:**

| Test ID | Description | Request | Expected Status | Expected Response |
|---------|-------------|---------|-----------------|-------------------|
| API-001 | Create user with valid data | `{"name":"Jane","email":"jane@test.com","role":"user"}` | 201 | User object with generated ID |
| API-002 | Missing required field (email) | `{"name":"Jane","role":"user"}` | 400 | `{"error":"email is required"}` |
| API-003 | Invalid role value | `{"name":"Jane","email":"jane@test.com","role":"superadmin"}` | 400 | `{"error":"role must be admin or user"}` |
| API-004 | Duplicate email | POST with email already in DB | 409 | `{"error":"email already exists"}` |
| API-005 | No auth token | POST without Authorization header | 401 | `{"error":"Unauthorized"}` |
| API-006 | Name as integer | `{"name":12345,"email":"j@test.com","role":"user"}` | 400 | `{"error":"name must be a string"}` |
| API-007 | Empty request body | `{}` | 400 | Validation errors for all required fields |
| API-008 | Name with special characters | `{"name":"<script>alert(1)</script>","email":"j@test.com","role":"user"}` | 400 or sanitised | No XSS stored or executed |
