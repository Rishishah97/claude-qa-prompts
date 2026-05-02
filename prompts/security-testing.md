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
