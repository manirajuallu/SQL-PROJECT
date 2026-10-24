# GYM MANAGEMENT SYSTEM – MYSQL PROJECT

## 📌 Project Overview
The **Gym Management System** is a database project developed using **MySQL**. It helps manage gym members, trainers, membership plans, memberships, payments, and attendance records.

The project demonstrates how SQL can be used to create and manage a database, connect related tables, generate reports, and automate tasks using views, stored procedures, and triggers.

## 🎯 Objectives
- Store and manage gym members' details.
- Maintain trainer information and specializations.
- Manage membership plans, durations, and fees.
- Assign plans and trainers to members.
- Record payments and payment methods.
- Maintain member attendance records.
- Generate useful reports using SQL queries.
- Validate payments and automatically maintain a payment log.

## 🛠️ Technologies Used
- **Database:** MySQL
- **Language:** SQL


## 🗂️ Database Tables
The database name is `gym_management_system`.

| Table | Purpose |
|---|---|
| `members` | Stores members' personal details and join dates. |
| `trainers` | Stores trainers' names, specializations, and phone numbers. |
| `membership_plans` | Stores plan names, durations, and fees. |
| `memberships` | Connects members with membership plans and trainers, including start and end dates. |
| `payments` | Stores payment amounts, dates, and payment methods. |
| `attendance` | Stores attendance dates and Present/Absent status for members. |
| `payment_log` | Keeps an audit record of newly inserted payments through a trigger. |

## 🔗 Table Relationships
- `members` → `memberships`: a member can have membership records.
- `membership_plans` → `memberships`: a plan can be assigned to membership records.
- `trainers` → `memberships`: a trainer can be assigned to membership records.
- `members` → `payments`: payments are linked to members.
- `members` → `attendance`: attendance records are linked to members.
- `payments` → `payment_log`: a trigger records new payments in the log.

Foreign keys help maintain relationships between related tables.

## ✨ Features
- Create the database and its tables.
- Insert sample members, trainers, plans, memberships, and payments.
- Use foreign keys to connect related records.
- Create indexes to help searches on selected columns.
- Create views for member details, total revenue, and trainer-wise member counts.
- Create stored procedures to view member details, calculate revenue, and add payments.
- Use triggers to log new payments and reject zero or negative payment amounts.
- Run queries to find member details, trainer assignments, revenue, city-wise counts, highest payment, average plan fee, and memberships nearing expiry.

## 🧠 SQL Concepts Used
- Database and table creation: `CREATE DATABASE`, `CREATE TABLE`
- Data insertion: `INSERT INTO`
- Primary keys and foreign keys
- Data types: `INT`, `VARCHAR`, `DATE`, `DECIMAL`, `ENUM`
- Indexes: `CREATE INDEX`
- Joins: `JOIN`, `LEFT JOIN`
- Aggregate functions: `SUM()`, `COUNT()`, `MAX()`, `AVG()`
- Grouping and sorting: `GROUP BY`, `ORDER BY`
- Views: `CREATE VIEW`
- Stored procedures: `CREATE PROCEDURE`
- Triggers: `CREATE TRIGGER`
- Date functions: `CURDATE()`, `DATE_ADD()`
- Filtering: `WHERE`, `BETWEEN`

## ▶️ How to Run the Project
1. Install and open **MySQL** (for example, MySQL Workbench or the MySQL command-line client).
2. Open the project's `.txt` file.
3. Review the SQL script before running it.
4. Execute the script to create the database, tables, sample records, indexes, views, procedures, triggers, and example queries.
5. Run queries such as `SELECT * FROM members;` to view the data.

## 📊 Example Reports
The project includes SQL queries to:
1. Display all members.
2. Display all trainers.
3. Show members with their assigned trainers.
4. Calculate total payment revenue.
5. Count members in each city.
6. Find the number of members assigned to each trainer.
7. Find memberships ending within the next 30 days.
8. Find the highest payment.
9. Calculate the average membership plan fee.
10. Display members enrolled in the yearly plan.

## 🧪 Sample Data
The SQL script includes sample records for:
- 5 members
- 3 trainers
- 4 membership plans
- 5 memberships
- 5 payments

The attendance table is created, but the provided script does not insert sample attendance records.

```
## 🚀 Future Improvements
- Add more sample attendance records.
- Create additional reports for monthly payments and attendance.
- Add constraints to make required fields mandatory.
- Build a user interface in a future version if needed.

