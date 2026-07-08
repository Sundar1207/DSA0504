# Lab: Query Processing for Data Science

## Overview
This lab focuses on understanding how queries are processed, optimized, and executed in data science workflows. It covers relational algebra operations, query execution plans, and performance optimization techniques like indexing.

---

## Objectives
* Understand the core phases of query processing (Parsing, Optimization, Execution).
* Analyze and compare query execution plans (`EXPLAIN`).
* Implement indexing to optimize data retrieval speeds.
* Evaluate the performance of different join algorithms (Nested Loop, Hash Join, Merge Join).

---

## Tools & Technologies
* **Language:** SQL / Python (Pandas)
* **Database Management System:** PostgreSQL / SQLite
* **Environment:** Jupyter Notebook / Terminal

---

## Key Concepts Covered

### 1. Query Execution Plans
Using the `EXPLAIN` or `EXPLAIN ANALYZE` commands to visualize how the database engine executes a query (e.g., Sequential Scan vs. Index Scan).

### 2. Query Optimization
Rewriting inefficient queries (e.g., replacing subqueries with joins or avoiding `SELECT *`) to reduce computational cost.

### 3. Performance Tuning (Indexing)
Creating B-Tree or Hash indexes on frequently queried columns to shift search complexity from $O(N)$ to $O(\log N)$.

---

## Lab Tasks & Implementations

### Task 1: Analyzing an Unoptimized Query
Below is the initial query used to retrieve data before optimization:

```sql
-- Unoptimized Query Example
SELECT customer_id, COUNT(order_id) 
FROM orders 
WHERE status = 'Completed' 
GROUP BY customer_id;
