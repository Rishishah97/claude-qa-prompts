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

---

## 6. Generate a Locust Load Test Script

```
Write a Locust load test script in Python for the following scenario.

Endpoints to test:
[List the endpoints, methods, and request bodies]

User behaviour flow:
[Describe the sequence of actions a virtual user should take]

Load profile:
- Users: [number]
- Spawn rate: [users per second]
- Duration: [minutes]

Include:
- Realistic think times between requests
- Auth handling (login once per user, reuse token)
- Custom success/failure conditions
- Clean, commented Python code
```

---

## 7. Analyse and Improve Slow Queries

```
Analyse the following slow database query and suggest performance improvements.

Query:
[Paste the SQL query]

Context:
- Database: [PostgreSQL / MySQL / other]
- Table sizes: [approximate row counts]
- Current execution time: [ms or seconds]
- EXPLAIN output (if available): [paste here]

Provide:
- Root cause of slowness
- Index recommendations
- Query rewrite suggestions
- Any schema changes that would help
- Expected improvement after fixes
```

---

## 8. Create a Capacity Planning Test Plan

```
Create a capacity planning test plan to determine the maximum load this system can handle before degrading.

System:
[Describe the application and infrastructure]

Current baseline performance:
[Any known metrics — response times, throughput, user counts]

Plan should include:
- How to establish the performance baseline
- Step-by-step load increments to run
- Metrics to monitor at each step (latency, CPU, memory, DB connections, error rate)
- How to identify the saturation point
- What degradation looks like (thresholds to watch)
- Infrastructure scaling options to test
- Recommendations for headroom and scaling triggers
```

---

## 9. Write a Soak / Endurance Test Plan

```
Design a soak (endurance) test plan for the following application.

Application:
[Describe the app and its normal usage patterns]

Soak test objectives:
[e.g. detect memory leaks, connection pool exhaustion, disk space growth]

Plan should cover:
- Test duration (recommended minimum and maximum)
- Load level to sustain (% of normal traffic)
- Metrics to monitor over time (memory, heap, thread count, GC activity, DB connections)
- Sampling intervals and alerting thresholds
- Expected gradual degradation patterns to watch for
- How to interpret results and identify slow leaks
```

---

## 10. Document Performance Test Results

```
Write a performance test results report based on the following data.

Test data / metrics:
[Paste your raw results, graphs summary, or key numbers]

Application tested:
[Name and version]

Audience for this report: [Engineering team / Stakeholders / Both]

Include:
- Executive summary (pass/fail against SLAs)
- Test environment and configuration
- Test scenarios run
- Key metrics (response time percentiles, throughput, error rate)
- Bottlenecks identified
- Comparison to previous results (if applicable)
- Recommendations
- Sign-off recommendation (go / no-go)
```
