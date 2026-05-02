# ⚡ Performance & Load Testing Prompts

Use these prompts to design performance test strategies, generate load test scenarios, and analyse results.

---

## 1. Generate a Performance Test Plan

```
You are a performance testing engineer. Create a performance test plan for the following application.

Application:
[Describe the app — type, tech stack, expected user base]

Key user journeys to test:
[List the critical flows e.g. login, checkout, search]

Include:
- Performance test objectives and success criteria
- Types of tests to run (load, stress, spike, soak, endurance)
- Key metrics to measure (response time, throughput, error rate, CPU/memory)
- Test environment requirements
- Suggested tools (e.g. k6, JMeter, Locust, Gatling)
- Risks and assumptions
```

---

## 2. Write a k6 Load Test Script

```
Write a k6 load test script for the following scenario.

Endpoint:
- Method: [GET / POST]
- URL: [endpoint URL]
- Auth: [type]
- Request body (if POST): [JSON]

Load profile:
- Ramp up to [X] virtual users over [Y] seconds
- Hold load for [Z] minutes
- Ramp down

Success criteria:
- 95th percentile response time < [Xms]
- Error rate < [X%]

Output clean, commented k6 JavaScript code.
```

---

## 3. Identify Performance Bottlenecks from Results

```
Analyse the following performance test results and identify bottlenecks, anomalies, and recommendations.

Test Results:
[Paste your test results, metrics, or summary here]

Application context:
[Brief description of the system under test]

Provide:
- Summary of findings
- Identified bottlenecks (with likely cause)
- Metrics that exceeded thresholds
- Prioritised recommendations to improve performance
- Suggested next steps
```

---

## 4. Generate Stress Test Scenarios

```
Generate stress test scenarios for the following system to find its breaking point.

System:
[Describe the application and infrastructure]

Normal expected load:
[e.g. 500 concurrent users, 1000 requests/min]

Create scenarios that:
- Gradually increase load beyond normal capacity
- Test sudden traffic spikes (e.g. 10x normal load instantly)
- Simulate resource exhaustion (memory, DB connections, threads)
- Test recovery behaviour after the system is overloaded

For each scenario include: name, description, load profile, expected failure mode, and what to observe.
```

---

## 5. Define Performance SLAs and Acceptance Criteria

```
Help me define performance SLAs and acceptance criteria for the following application.

Application type: [e.g. e-commerce / SaaS dashboard / mobile API]
Expected concurrent users: [number]
Peak traffic periods: [e.g. Black Friday, end of month]
Infrastructure: [e.g. AWS, 3 app servers, RDS]

Define:
- Response time thresholds (p50, p90, p95, p99)
- Throughput targets (requests per second)
- Error rate thresholds
- Availability / uptime SLA
- Scalability expectations
- Pass/fail criteria for performance test sign-off
```
