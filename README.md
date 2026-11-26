# HR & Payroll Exploratory Data Analysis (SQL)

## 📌 Project Overview
In this project, I created and queried a relational HR and Payroll database (`Parks_and_Recreation`) using MySQL. My goal was to go beyond practicing basic syntax and use foundational SQL queries to answer real-world workforce, demographic, and compensation questions.

## 🗂️ Database Structure
The database consists of three interconnected tables:
* **`employee_demographics`**: Stores employee personal information (`employee_id`, `first_name`, `last_name`, `age`, `gender`, `birth_date`).
* **`employee_salary`**: Tracks job titles, compensation, and department IDs (`employee_id`, `first_name`, `last_name`, `occupation`, `salary`, `dept_id`).
* **`parks_departments`**: Lookup table mapping department IDs (`department_id`) to official department names (`department_name`).

## 🎯 Business Problems I Solved
1. **Workforce & Retirement Planning:** I audited active employee demographics, checked unique gender categories (`DISTINCT`), and calculated 10-year age projections (`age + 10`) to help anticipate future retirements.
2. **Compensation & Salary Band Audits:** I filtered payroll records (`WHERE salary <= 50000` and `< 50000`) to isolate entry-level and support staff earning $50,000 or less for salary and budget reviews.
3. **Succession Planning & Personnel Lookups:** I used logical operators (`AND`, `OR`, `NOT`) to identify senior staff over age 55 and verify specific employee records by birth date and gender.
4. **Generational Cohort & Directory Searches:** I used wildcard pattern matching (`LIKE`, `%`, `_`) to segment employees born in the 1980s (`198%`) and search staff records using partial name prefixes and character lengths.

## 🛠️ SQL Concepts Used
* **Database & Table Setup:** `CREATE DATABASE`, `CREATE TABLE`, `INSERT INTO`
* **Data Retrieval & Calculations:** `SELECT`, `DISTINCT`, arithmetic expressions, column aliases
* **Conditional Filtering:** `WHERE`, comparison operators (`=`, `!=`, `<`, `<=`)
* **Logical Operators:** `AND`, `OR`, `NOT`, parentheses precedence
* **Pattern Matching:** `LIKE` with `%` and `_` wildcards

## 📂 Files in This Repository
* `parks_and_recreation_setup.sql`: Full SQL script to create the database schema and populate all three tables.
* `hr_exploratory_analysis.sql`: Commented SQL queries organized by business questions.

## 🚀 How to Run
1. Open MySQL Workbench (or any MySQL-compatible environment).
2. Execute `parks_and_recreation_setup.sql` to build and populate the database.
3. Run the queries inside `hr_exploratory_analysis.sql` to view the results.

## 🔜 Next Steps
* Expand the analysis using `GROUP BY`, `HAVING`, and `ORDER BY` for departmental salary aggregations.
* Use `JOIN`s to analyze cross-table relationships and spot missing employee/department records.

