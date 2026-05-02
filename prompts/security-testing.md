# 🔐 Security Testing Prompts

Use these prompts to generate security test cases, threat models, and vulnerability checklists.

---

## 1. Generate a Security Test Checklist

```
You are a security-focused QA engineer. Generate a security testing checklist for the following application.

Application type: [e.g. web app / REST API / mobile app]
Auth method: [e.g. JWT / OAuth2 / session cookies]
Key features: [e.g. user login, payments, file uploads, admin panel]

Cover the following areas:
- Authentication and authorisation
- Input validation and injection (SQL, XSS, command injection)
- Session management
- Sensitive data exposure
- CORS and security headers
- File upload security
- Rate limiting and brute force protection
- API security (if applicable)
- OWASP Top 10 coverage

Format as a checklist with Test ID, Description, and Risk Level (High / Medium / Low).
```

---

## 2. Generate OWASP Top 10 Test Cases

```
Generate test cases covering the OWASP Top 10 vulnerabilities for the following application.

Application:
[Describe the app, its key features, and tech stack]

For each OWASP category:
- Explain how it applies to this application
- Provide 2–3 specific test cases
- Include what to test, how to test it, and what a vulnerable response looks like

Focus on practical, manual test cases a QA engineer can execute.
```

---

## 3. Write Auth & Authorisation Test Cases

```
Generate comprehensive authentication and authorisation test cases for the following system.

Auth details:
- Login method: [email+password / SSO / MFA / OAuth]
- User roles: [list roles e.g. admin, user, guest]
- Protected resources: [list key pages or endpoints]

Cover:
- Valid and invalid login attempts
- Account lockout and brute force protection
- Password policies (complexity, expiry, history)
- Token security (expiry, refresh, revocation)
- Role-based access control (can role A access role B's resources?)
- Horizontal privilege escalation (can user A access user B's data?)
- Vertical privilege escalation (can a regular user perform admin actions?)
- Session fixation and hijacking scenarios
```

---

## 4. Review Code or Config for Security Issues

```
Review the following code / configuration for security vulnerabilities.

Code / Config:
[Paste your code, API config, or infrastructure config here]

Check for:
- Hardcoded secrets or credentials
- Insecure dependencies
- Missing input validation
- Unsafe deserialization
- Exposed sensitive data in logs or responses
- Misconfigured security headers
- Overly permissive CORS or IAM policies
- Any other security risks

For each issue found: describe the vulnerability, its risk level, and how to fix it.
```

---

## 5. Create a Threat Model for a Feature

```
Create a threat model for the following feature using the STRIDE framework.

Feature:
[Describe the feature in detail — what it does, who uses it, what data it handles]

For each STRIDE category (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege):
- Identify relevant threats
- Assess likelihood and impact
- Suggest mitigations and security controls

Output as a structured threat model table.
```

---

## 6. Generate API Security Test Cases

```
Generate security-focused test cases for the following API.

API details:
- Base URL: [endpoint]
- Auth: [Bearer token / API key / OAuth]
- Key endpoints: [list them]

Cover:
- Missing or invalid auth tokens (401 responses)
- Expired tokens not accepted
- Tokens from other users rejected (IDOR)
- Mass assignment vulnerabilities (sending extra fields)
- HTTP method tampering (GET instead of POST, etc.)
- Sensitive data in responses (tokens, passwords, PII not exposed)
- Rate limiting on sensitive endpoints (login, password reset)
- Insecure direct object references (accessing other users' resources)
- Verbose error messages leaking stack traces or DB info
- CORS misconfiguration
```

---

## 7. Write a Penetration Test Checklist for a Web App

```
Create a manual penetration testing checklist for the following web application.

Application:
[Describe the app, its features, and user roles]

Organise the checklist by:
- Reconnaissance (information gathering)
- Authentication testing
- Session management
- Input validation (XSS, SQLi, XXE, SSTI)
- Business logic flaws
- Access control (IDOR, privilege escalation)
- Sensitive data exposure
- Security headers and TLS configuration
- Third-party components and dependencies
- File upload and download security

For each item: description, how to test it, and what a vulnerability looks like.
```

---

## 8. Review Infrastructure Config for Security Issues

```
Review the following infrastructure or deployment configuration for security vulnerabilities.

Config:
[Paste your Docker Compose, Kubernetes manifest, Nginx config, AWS policy, or similar]

Check for:
- Running containers or services as root
- Exposed ports that should be internal only
- Missing or overly permissive IAM/RBAC policies
- Secrets stored in environment variables or plain config files
- Missing network policies or security groups
- Outdated or vulnerable base images
- Missing resource limits (CPU/memory)
- Insecure TLS configurations
- Publicly accessible storage buckets or databases

For each issue: severity, description, and remediation steps.
```

---

## 9. Generate Security Regression Test Cases After a Fix

```
Generate security regression test cases to verify the following vulnerability has been correctly fixed.

Vulnerability:
[Describe the security bug — type, how it was exploited, what was changed to fix it]

Write test cases that:
- Confirm the specific attack vector no longer works
- Test related attack variations (to ensure the fix is complete, not just patched)
- Verify no new vulnerabilities were introduced by the fix
- Check edge cases around the fix

Include both positive tests (fix works) and negative tests (related attacks also blocked).
```

---

## 10. Create a Security Test Plan for a Release

```
Create a security test plan for the following upcoming release.

Release scope:
[What is being released — new features, changes, infrastructure updates]

Application type: [Web / API / Mobile]
Risk level: [Low / Medium / High — and why]

Plan should include:
- Security testing scope and objectives
- Types of testing to perform (SAST, DAST, manual pen test, dependency scan)
- Tools to use (e.g. OWASP ZAP, Snyk, Semgrep, Burp Suite)
- High-risk areas to focus on
- Entry and exit criteria
- Who is responsible for each activity
- Timeline and effort estimate
- Sign-off requirements
```
