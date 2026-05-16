# Personal & Household Financial Management System (RDBMS)

## Overview
This repository contains a production-ready, 3NF-normalized relational database system designed to manage personal and household finances. The project focuses on strict **Data Integrity**, automated business logic via database **Triggers**, and advanced **Analytical Queries** for financial auditing.

## Key Technical Features

### 1. 3NF Normalized Schema Architecture
Designed and implemented a robust relational schema consisting of **13 interconnected tables** to handle complex financial entities:
* **Core Entities:** `Users`, `Households`, `Financial_Accounts`, `Transactions`.
* **Budgeting & Goals:** `Budget_Goals`, `Categories`, `Savings`, `Bills`, `Income_Sources`.
* **System Logistics:** `Notifications`, `Location`, `Countries`.

### 2. Automated PL/SQL Logic & Data Integrity
To preserve data quality and prevent negative anomalies, the database relies on automated server-side programming rather than application-layer validation:
* **Dynamic Balance Management (`trg_account_balance_update`):** Automatically recalculates and updates real-time balances in `Financial_Accounts` whenever an `INCOME` or `EXPENSE` transaction occurs.
* **Risk & Fraud Prevention (`trg_savings_check`):** Enforces data constraints by blocking any updates where current savings accidentally exceed the target goal amount.
* **Data Quality Constraints:** Heavy implementation of database-level constraints (`CHECK`, `UNIQUE`, `FOREIGN KEY` cascades) to prevent data corruption.
* **Automated Low-Balance Alerts (`notify_low_balance`):** Trigger pipeline that automatically fires and populates the `Notifications` audit table when an account's balance drops below a critical threshold.

### 3. Advanced Financial Analytics
Developed optimized SQL queries to extract actionable business intelligence from financial records, leveraging:
* Multi-table **JOINs** and deep nested **Subqueries** to track spending speed.
* Sophisticated **GROUP BY** and Window functions for monthly budget execution analysis and tracking discrepancies between expected and actual household limits.

### 4. QA & Data Consistency Validation
* Generated and systematically loaded **2,600+ mock records** (exactly 200 validation rows across all 13 schemas) engineered via Mockaroo.
* Executed integration testing on relational constraints to confirm data consistency under heavy transaction logging simulations.

## Tech Stack
* **Database Engine:** Oracle SQL / PL-SQL (compatible with PostgreSQL)
* **Modeling Tools:** Entity-Relationship Diagramming (ERD)
* **Testing & Mocking:** Mockaroo Data Pipelines
