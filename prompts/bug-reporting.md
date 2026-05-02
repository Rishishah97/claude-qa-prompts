# 🐛 Bug Reporting Prompts

Use these prompts to write clear, structured, and developer-friendly bug reports.

---

## 1. Write a Structured Bug Report

**When to use:** You've found a bug and want to write a well-structured report quickly.

```
You are a QA engineer. Write a clear and detailed bug report based on the following information:

What I observed:
[Describe what went wrong]

Where it happened:
[Feature / page / endpoint]

Environment:
[Browser, OS, app version, device, etc.]

Write a bug report with the following fields:
- Title (concise and descriptive)
- Environment
- Severity (Critical / High / Medium / Low)
- Priority (P1 / P2 / P3 / P4)
- Steps to Reproduce (numbered)
- Expected Result
- Actual Result
- Attachments needed (screenshots, logs, etc.)
- Possible Root Cause (if known)
```

---

## 2. Improve a Poorly Written Bug Report

**When to use:** A bug has been reported but the description is vague or incomplete.

```
The following bug report is unclear or incomplete. Rewrite it to be developer-friendly, specific, and actionable.

Original Report:
[Paste the original bug report]

Improve it by:
- Writing a clear, specific title
- Adding detailed reproduction steps
- Clarifying expected vs actual behaviour
- Suggesting severity and priority
- Noting any missing information that should be gathered
```

---

## 3. Classify Bug Severity and Priority

**When to use:** You're unsure how to triage a bug and need help deciding severity/priority.

```
Help me classify the following bug in terms of severity and priority.

Bug Description:
[Describe the bug and its impact]

Context:
- Product type: [e.g. SaaS B2B / consumer mobile app / internal tool]
- Affected users: [e.g. all users / admins only / specific region]
- Workaround available: [Yes / No]
- Release date: [Upcoming / Already live]

Provide:
- Severity: Critical / High / Medium / Low — with reasoning
- Priority: P1 / P2 / P3 / P4 — with reasoning
- Recommended action: [Fix immediately / Fix in next sprint / Backlog]
```

---

## 4. Write a Bug Report from Logs or Error Messages

**When to use:** You have an error log or stack trace and need to turn it into a bug report.

```
You are a QA engineer. Based on the following error log / stack trace, write a structured bug report.

Error Log:
[Paste the error log or stack trace here]

Application context:
[What the user was doing when the error occurred]

Include:
- A descriptive title
- Steps that likely led to this error
- Expected vs actual behaviour
- Severity assessment
- Suggested labels or tags for the ticket
- Questions to ask the dev team if more info is needed
```

---

## 5. Generate a Bug Report Template for Your Team

**When to use:** You want to standardise bug reporting across your QA team.

```
Create a bug report template tailored for a [type of product, e.g. web app / mobile app / API].

The template should be usable in [Jira / GitHub Issues / Linear / Notion / other].

Include fields for:
- Summary / Title
- Environment details
- Reproduction steps
- Expected vs actual result
- Severity and priority
- Attachments / evidence
- Any additional context

Make it easy to fill in quickly but thorough enough to avoid back-and-forth with developers.
```
