# 🔍 Exploratory Testing Prompts

Use these prompts to design exploratory testing charters, session notes, and risk-based testing strategies.

---

## 1. Create an Exploratory Testing Charter

```
You are a QA engineer planning an exploratory testing session. Write a testing charter for the following area.

Feature / Area to explore:
[Describe the feature or area of the application]

Session duration: [e.g. 60 minutes]
Tester experience level: [Beginner / Intermediate / Expert]

Charter should include:
- Mission statement ("Explore X to discover Y")
- Areas and functions to explore
- Risks and concerns to investigate
- Things to specifically look out for (edge cases, error states, data conditions)
- What is out of scope
- How to log findings during the session
```

---

## 2. Generate Exploratory Test Ideas Using Heuristics

```
Generate exploratory test ideas for the following feature using common testing heuristics.

Feature:
[Describe the feature]

Apply these heuristics (where relevant):
- SFDIPOT (Structure, Function, Data, Integrations, Platform, Operations, Time)
- Goldilocks (too much, too little, just right)
- CRUD (Create, Read, Update, Delete)
- Boundary values and equivalence partitioning
- Error guessing
- User personas (novice, expert, malicious user, distracted user)

For each heuristic, generate 3–5 specific test ideas.
```

---

## 3. Write an Exploratory Testing Session Report

```
Help me write a structured session report from the following exploratory testing notes.

Raw Notes:
[Paste your rough session notes, observations, and findings]

Session details:
- Feature explored: [feature name]
- Duration: [time]
- Tester: [your name or role]

Format the report with:
- Session summary
- What was covered (and what wasn't)
- Bugs found (with severity)
- Risks and concerns identified
- Questions and follow-up actions
- Recommendations for future sessions
```

---

## 4. Risk-Based Exploratory Test Planning

```
Help me prioritise exploratory testing for the following release using a risk-based approach.

Release scope:
[Describe what's changing in this release]

Application context:
[Type of app, user base, criticality of features]

Identify:
- Highest risk areas (based on complexity, change size, past defects, business impact)
- Suggested time allocation per risk area
- Personas or user types most likely to be affected
- Integration points and dependencies to probe
- Recommended testing order

Output a prioritised exploratory testing plan for the release.
```

---

## 5. Generate Personas for Exploratory Testing

```
Generate realistic user personas to guide exploratory testing for the following application.

Application:
[Describe the app and its key user types]

For each persona include:
- Name and role
- Goals and motivations
- Technical ability level
- Device and environment (browser, OS, connection speed)
- Behaviours that differ from the "happy path" user
- Specific scenarios this persona would expose

Generate 4–6 personas including at least one power user, one novice, and one adversarial user.
```

---

## 6. Generate Boundary and Edge Case Ideas

```
Generate boundary and edge case test ideas for the following feature using structured techniques.

Feature:
[Describe the feature and its key inputs, rules, and behaviours]

Apply these techniques:
- Boundary value analysis (min, min+1, max-1, max, just outside bounds)
- Equivalence partitioning (valid and invalid input classes)
- Decision table testing (combinations of conditions)
- State transition testing (if the feature has different states)
- Error guessing (common mistakes and failure modes)

Output a prioritised list of test ideas grouped by technique.
```

---

## 7. Write a Retrospective for a Testing Cycle

```
Help me write a QA retrospective for the following testing cycle.

Testing cycle summary:
[Describe the sprint or release — what was tested, how long, team size]

Known outcomes:
- Bugs found during testing: [number and severity breakdown]
- Bugs found in production: [number]
- Test coverage achieved: [%]
- Blockers encountered: [describe]

Format the retrospective with:
- What went well
- What didn't go well
- Root cause analysis of any escaped bugs
- Process improvement suggestions
- Action items with owners and due dates
```

---

## 8. Generate Negative Testing Ideas for a Feature

```
Generate creative negative test ideas for the following feature.

Feature:
[Describe the feature in detail]

Think like a user who is:
- Making genuine mistakes (typos, wrong format, wrong order)
- Using the system in an unintended way
- Trying to break or stress the system
- Using edge case data (empty, null, max length, special chars, emojis)
- On a bad network or slow device
- Switching between actions rapidly

Generate at least 15 negative test ideas, each with a brief description of what to try and what a good failure looks like.
```

---

## 9. Create a Bug Bash Plan

```
Plan a bug bash session for the following product / release.

Product:
[Describe the application and the features to focus on]

Team size: [number of participants]
Duration: [e.g. 2 hours]
Participant mix: [developers, designers, PMs, support, QA]

Plan should include:
- Goals and scope for the session
- How to divide areas across participants
- Environment and test account setup instructions
- Bug reporting format to use during the session
- Voting / prioritisation approach for findings
- Post-session triage process
- Suggested reward or incentive (optional)
```

---

## 10. Generate Test Ideas from User Feedback or Support Tickets

```
Generate exploratory test ideas based on the following user feedback, support tickets, or reviews.

User Feedback / Tickets:
[Paste the feedback, complaints, or support ticket summaries]

From this feedback, generate:
- Specific test scenarios to reproduce reported issues
- Related areas to probe that the feedback hints at
- Edge cases the feedback suggests users encounter
- Questions to investigate during exploratory sessions
- Suggestions for permanent test cases to add to the regression suite

Prioritise by frequency of mention and severity of impact.
```
