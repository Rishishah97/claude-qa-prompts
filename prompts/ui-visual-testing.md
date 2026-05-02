# 🎨 UI / Visual Testing Prompts

Use these prompts to generate UI test cases, visual regression strategies, and cross-browser test plans.

---

## 1. Generate UI Test Cases for a Screen

```
You are a QA engineer. Generate UI test cases for the following screen or component.

Screen / Component:
[Describe the screen — its purpose, key elements, and interactions]

Cover:
- Layout and alignment on different screen sizes (mobile, tablet, desktop)
- Typography (font size, weight, truncation on small screens)
- Colour and contrast
- Interactive states (default, hover, focus, active, disabled, loading, error)
- Empty states (no data / first-time user view)
- Data-heavy states (long text, large numbers, many list items)
- Responsive breakpoints
- Dark mode (if supported)
- Right-to-left (RTL) layout (if applicable)

Format: Test ID | Description | Steps | Expected Result | Device/Viewport
```

---

## 2. Create a Visual Regression Testing Strategy

```
Design a visual regression testing strategy for the following application.

Application:
[Describe the app — type, tech stack, number of screens/components]

Current pain points:
[e.g. UI bugs caught late, no visual testing in place, frequent design changes]

Include:
- Recommended visual testing approach (component vs full-page)
- Tool recommendations (e.g. Percy, Chromatic, Playwright visual comparisons, BackstopJS)
- What to capture (key pages, components, states, viewports)
- Baseline management approach
- CI/CD integration strategy
- How to handle intentional vs unintentional visual changes
- Maintenance considerations
```

---

## 3. Generate Cross-Browser Test Plan

```
Create a cross-browser and cross-device test plan for the following web application.

Application:
[Describe the app]

Target audience / market:
[e.g. UK enterprise users / global consumer / mobile-first]

Generate a test plan including:
- Priority browser and version matrix (based on market share)
- OS combinations to test
- Device categories (desktop, tablet, mobile)
- Features most likely to behave differently across browsers
- Testing approach (manual vs automated vs cloud grid like BrowserStack/Sauce Labs)
- Pass/fail criteria for cross-browser sign-off

Format the browser matrix as a table.
```

---

## 4. Review a Design Spec for Testability

```
Review the following design specification or Figma description and identify potential UI testing concerns.

Design Spec:
[Paste or describe the design — components, interactions, states, animations]

Identify:
- Missing states (error, loading, empty, disabled)
- Unclear interaction behaviours
- Accessibility concerns in the design
- Responsive behaviour that needs clarification
- Animation and transition details needed for testing
- Edge cases the design doesn't account for (long text, missing data, etc.)
- Questions to raise with the designer before development starts
```

---

## 5. Generate Test Cases for Forms and Input Validation

```
Generate UI test cases for the following form.

Form name / purpose:
[e.g. User registration form / Checkout form / Profile edit]

Fields:
[List each field with its type, constraints, and validation rules]

Cover:
- Valid input for each field
- Required field validation (submit with each field empty)
- Field-level error messages (correct text, placement, styling)
- Format validation (email, phone, postcode, date)
- Character limits (at limit, over limit)
- Special characters and emoji in text fields
- Copy-paste behaviour
- Autofill behaviour
- Tab order and keyboard navigation
- Form submission success and error states
- Mobile keyboard types (numeric, email, etc.)
```
