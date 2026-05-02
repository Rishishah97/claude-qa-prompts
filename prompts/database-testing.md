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

---

## 6. Generate Test Cases for Database Constraints

```
Generate test cases to validate database constraints for the following schema.

Schema:
[Paste or describe your table definitions including constraints]

Database: [type]

Cover each constraint type present:
- NOT NULL: attempt to insert NULL into required fields
- UNIQUE: attempt to insert duplicate values
- FOREIGN KEY: attempt to insert orphaned records; attempt to delete parent records
- CHECK: attempt values that violate check conditions
- DEFAULT: verify defaults are applied when fields are omitted
- PRIMARY KEY: attempt duplicate PKs; verify auto-increment behaviour

For each: SQL statement to run, expected error/behaviour, pass/fail criteria.
```

---

## 7. Test Database Transactions and Rollbacks

```
Generate test cases for database transaction handling in the following scenario.

Feature / Operation:
[Describe the multi-step operation that uses a database transaction]

Database: [type]

Cover:
- All steps succeed: verify all changes committed
- Failure at step 2 of N: verify all previous steps rolled back
- Concurrent transactions: verify isolation level prevents dirty reads
- Deadlock scenario: verify deadlock is detected and resolved
- Long-running transaction: verify locks are released appropriately
- Savepoint behaviour (if used)
- Connection failure mid-transaction: verify rollback on reconnect

Include setup SQL, test steps, and verification queries for each scenario.
```

---

## 8. Generate NoSQL / MongoDB Test Cases

```
Generate test cases for the following MongoDB collection and operations.

Collection name: [name]
Document schema: [describe the structure]
Operations to test: [find, insert, update, delete, aggregation, etc.]

Cover:
- CRUD operations with valid documents
- Schema validation rules (if using JSON Schema validation)
- Index usage verification (explain() shows index hit)
- Query performance with large datasets
- Atomic operations on embedded documents
- Array field operations ($push, $pull, $addToSet)
- Aggregation pipeline correctness
- Handling of missing or null fields in queries
- Write concern and read preference behaviour
```

---

## 9. Write Data Seeding Scripts for Test Environments

```
Write a data seeding script for the following test environment.

Database: [type and version]
Schema: [describe the tables or paste DDL]

Seed data requirements:
- [Entity 1]: [how many records, any specific values needed]
- [Entity 2]: [how many records, relationships to Entity 1]
- [etc.]

The script should:
- Be idempotent (safe to run multiple times)
- Respect foreign key constraints and insertion order
- Use realistic but anonymised data
- Support different environments (dev, staging, CI)
- Be easy to extend with new entities

Output clean SQL or [Python / Node.js] seeding code.
```

---

## 10. Validate ETL Pipeline Data Quality

```
Generate data quality test cases for the following ETL pipeline.

Pipeline:
[Describe the source, transformation steps, and destination]

Source system: [type]
Destination system: [type]
Key transformations: [list them]

Test cases should cover:
- Row count reconciliation (source vs destination)
- Column-level data accuracy (spot-check key fields)
- Null handling (nulls in source mapped correctly)
- Data type conversions (no truncation or precision loss)
- Deduplication logic (duplicates correctly handled)
- Filter conditions (only expected records included)
- Incremental load correctness (only new/changed records processed)
- Rejection and error log validation
- Performance (pipeline completes within SLA)

Include SQL queries to validate each check.
```
