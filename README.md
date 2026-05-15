# Personal Finance Management System (SQL)

## Overview
This project is a relational database system designed to track personal finances, budgets, and savings goals. It focuses on **data integrity**, automation via **triggers**, and complex business logic.

## Key Technical Features
* **Complex Schema:** 8+ normalized tables including Users, Transactions, Households, and Budgets.
* **Automated Logic:** * Triggers for automatic balance updates after transactions.
  * Notification triggers for low balances.
  * Automated budget tracking and validation.
* **Data Integrity:** Heavy use of SQL Constraints (`NOT NULL`, `CHECK`, `FOREIGN KEY`) to ensure high data quality.
* **Analytics:** Includes complex queries with `JOINs`, `GROUP BY`, and Subqueries for financial reporting.

## Tech Stack
* Oracle SQL / PostgreSQL
* Database Design (ERD)
* Data Mocking (Mockaroo)
