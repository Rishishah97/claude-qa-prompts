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
