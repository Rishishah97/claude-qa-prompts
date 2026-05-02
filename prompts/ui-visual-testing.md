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

---

## 6. Generate Test Cases for Modals and Overlays

```
Generate UI test cases for the following modal, dialog, or overlay component.

Modal / Dialog:
[Describe its purpose, trigger, content, and actions]

Cover:
- Opens correctly from all trigger points
- Focus is trapped inside the modal while open
- Closes on: close button, backdrop click, Escape key
- Background content is not interactive while modal is open
- Screen reader announces modal correctly (role="dialog", aria-modal)
- Scroll behaviour (modal scrolls independently if content is long)
- Mobile behaviour (full screen vs centred overlay)
- Nested modals (if applicable)
- Loading and error states within the modal
- Confirmation before destructive actions (e.g. delete)
```

---

## 7. Generate Snapshot and Visual Regression Test Cases

```
Generate a list of visual regression test cases for the following application using snapshot testing.

Application / Component Library:
[Describe the app or component library]

Tool: [Percy / Chromatic / Playwright / BackstopJS]

Define snapshots to capture for:
- Each key page at desktop, tablet, and mobile viewports
- Components in all interactive states (default, hover, focus, error, disabled, loading)
- Dark mode vs light mode
- Data edge cases (empty, single item, max items, long strings)
- Internationalisation (different text lengths for EN, DE, FR, AR)

For each snapshot: name, URL or component, viewport, state, and any setup required.
```

---

## 8. Evaluate UI Consistency Against a Design System

```
Evaluate the following UI implementation against the design system / style guide.

Design system tokens / rules:
[Describe or paste spacing, colour, typography, and component rules]

UI implementation details:
[Describe or paste the implemented component or page]

Check for:
- Correct use of colour tokens (no hardcoded hex values)
- Typography scale compliance (font sizes, weights, line heights)
- Spacing and layout grid adherence
- Component variants used correctly (not custom one-offs)
- Icon usage consistency
- Border radius and shadow consistency
- Animation timing adherence

Output a list of deviations with severity and recommended fix.
```

---

## 9. Write Test Cases for Drag and Drop Interactions

```
Generate test cases for a drag and drop interaction in the following feature.

Feature:
[Describe the drag and drop — what is being dragged, where it can be dropped, and the outcome]

Cover:
- Successful drag and drop to a valid target
- Drag to an invalid target (visual feedback and rejection)
- Drag and drop via keyboard (using arrow keys and Enter/Space)
- Screen reader announcements during drag and drop
- Touch / mobile drag behaviour
- Cancelling a drag (Escape key or releasing outside a valid zone)
- Visual state during drag (drag ghost, drop zone highlight)
- Performance with many draggable items
- Nested drag targets
```

---

## 10. Generate Tests for Infinite Scroll and Pagination

```
Generate test cases for the following infinite scroll or pagination implementation.

Feature:
[Describe the list or grid — what data it shows, how many items per page, and the load mechanism]

Type: [Infinite scroll / Load more button / Numbered pagination]

Cover:
- Initial load shows correct number of items
- Next page / more items load correctly on trigger
- Loading indicator appears during fetch
- No duplicate items across pages
- Correct behaviour at the last page / end of data
- Empty state when no items exist
- Error state when loading fails (retry option)
- Back navigation preserves scroll position and page state
- URL updates with page number (for pagination)
- Keyboard and screen reader accessibility
```
