# 🗄️ Database Testing Prompts

Use these prompts to generate database test cases, validate data integrity, and test migrations.

---

## 1. Generate Database Test Cases for a Feature

```
You are a QA engineer. Generate database-level test cases for the following feature.

Feature:
[Describe the feature and what data it creates, reads, updates, or deletes]

Database: [PostgreSQL / MySQL / MongoDB / SQL Server / other]
Key tables / collections involved: [list them]

Cover:
- Data is correctly inserted / updated / deleted when the feature is used
- Constraints are enforced (NOT NULL, UNIQUE, FOREIGN KEY, CHECK)
- Cascading deletes and updates work as expected
- Default values are applied correctly
- Data types and field lengths are validated
- Transactions roll back correctly on failure
- Indexes support expected query performance

Format: Test ID | Description | SQL/Query to run | Expected Result
```

---

## 2. Validate Data Integrity After a Migration

```
Generate a data validation checklist and SQL queries to verify data integrity after the following database migration.

Migration details:
[Describe what the migration does — schema changes, data transformation, table moves, etc.]

Database: [type]
Affected tables: [list]

Validate:
- Row counts match between source and target
- No NULL values in required fields
- No orphaned records (referential integrity)
- Data transformations applied correctly
- No duplicate records introduced
- Indexes and constraints recreated correctly
- Sample spot-checks on critical records

Output as a checklist with SQL queries for each check.
```

---

## 3. Write SQL Queries to Test Business Logic

```
Write SQL queries to verify the following business logic is correctly reflected in the database.

Business Rule:
[Describe the rule — e.g. "An order cannot be placed if the user's account is suspended" or "Discount is only applied for orders over £50"]

Tables and schema (if known):
[Describe or paste relevant table structures]

Write queries that:
- Confirm compliant records exist as expected
- Identify any records that violate the business rule
- Can be used as part of a regression test suite

Include comments explaining what each query checks.
```

---

## 4. Generate Test Cases for Stored Procedures or Triggers

```
Generate test cases for the following stored procedure or database trigger.

Procedure / Trigger definition:
[Paste the code or describe what it does]

Database: [type]

Cover:
- Happy path execution with valid inputs
- Boundary and edge case inputs
- Invalid or null inputs
- Error handling (what happens when it fails?)
- Side effects on related tables
- Performance with large data sets
- Concurrent execution behaviour (if applicable)

Format: Test ID | Input | Action | Expected DB State | Pass/Fail Criteria
```

---

## 5. Generate a Database Performance Test Plan

```
Create a database performance test plan for the following system.

System:
[Describe the application and database usage patterns]

Database: [type and version]
Expected data volume: [rows per key table, growth rate]

Include:
- Key queries to benchmark
- Index effectiveness checks
- Query execution plan analysis approach
- Slow query identification strategy
- Test data volume requirements
- Concurrency and locking scenarios
- Suggested tools (e.g. EXPLAIN ANALYZE, pgBench, SysBench)
- Performance thresholds and acceptance criteria
```
