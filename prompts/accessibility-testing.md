# ♿ Accessibility Testing Prompts

Use these prompts to generate WCAG-aligned accessibility test cases, audits, and remediation guidance.

---

## 1. Generate Accessibility Test Cases for a Page

```
You are an accessibility QA specialist. Generate test cases for the following web page or screen.

Page / Screen:
[Describe the page — its purpose, key elements, interactions]

Standard: WCAG 2.1 Level AA

Cover:
- Keyboard navigation (tab order, focus visibility, no keyboard traps)
- Screen reader compatibility (NVDA, JAWS, VoiceOver)
- Colour contrast (text, UI components, focus indicators)
- Images and non-text content (alt text, decorative images)
- Form labels and error messages
- Headings and semantic structure
- Links and buttons (descriptive labels, purpose clear from context)
- Motion and animation (prefers-reduced-motion support)
- Responsive and zoom behaviour (up to 400%)

Format: Test ID | WCAG Criterion | Description | Steps | Expected Result | Pass/Fail
```

---

## 2. Audit a Component for Accessibility Issues

```
Perform an accessibility audit on the following UI component.

Component code or description:
[Paste HTML/JSX or describe the component in detail]

Check against WCAG 2.1 AA for:
- Semantic HTML usage
- ARIA roles, labels, and attributes (correct and necessary usage)
- Keyboard operability
- Focus management
- Colour contrast
- Screen reader announcements
- Touch target size (for mobile)

For each issue found: WCAG criterion violated, severity (Critical / Serious / Moderate / Minor), description, and recommended fix.
```

---

## 3. Write Accessibility Acceptance Criteria

```
Write accessibility acceptance criteria for the following feature.

Feature:
[Describe the feature]

User types who may be affected:
[e.g. screen reader users, keyboard-only users, low vision users, motor impaired users]

Write clear, testable acceptance criteria covering:
- Keyboard accessibility
- Screen reader support
- Visual contrast and layout
- Error handling and feedback
- Any ARIA requirements

Format as Given/When/Then or standard acceptance criteria statements.
```

---

## 4. Generate a Screen Reader Test Script

```
Write a manual test script for testing the following page or flow with a screen reader.

Page / Flow:
[Describe the page or user journey]

Screen reader to test with: [NVDA + Chrome / JAWS + Edge / VoiceOver + Safari]

The script should:
- List each step the tester should take
- Describe what the screen reader should announce at each step
- Highlight key elements to verify (headings, buttons, forms, alerts, modals)
- Include expected announcements and pass/fail criteria

Make it usable by a tester who is not an accessibility expert.
```

---

## 5. Prioritise and Fix Accessibility Issues

```
Review the following accessibility issues and help me prioritise and fix them.

Issues found:
[List or paste your accessibility audit findings]

For each issue:
- Assign a priority (Critical / High / Medium / Low) based on user impact
- Explain who is affected and how
- Provide a specific code fix or remediation guidance
- Reference the relevant WCAG success criterion

Then provide a prioritised remediation plan grouped by sprint or effort level.
```
