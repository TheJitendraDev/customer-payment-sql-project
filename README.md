# Customer & Payment Management System

A PostgreSQL-based database project designed to manage customer information and payment transactions. This project demonstrates practical SQL concepts including JOINs, GROUP BY, HAVING, aggregate functions, subqueries, CTEs, and SQL Views.

---

## 📌 Project Overview

The **Customer & Payment Management System** is a relational database project developed using **PostgreSQL** and **SQL**.

The system stores customer details and their payment transactions in separate relational tables. SQL queries are used to combine, filter, group, and analyze payment data to generate meaningful customer-wise reports.

### Main Objectives

- Store customer information
- Store customer payment transactions
- Establish relationships between customers and payments
- Analyze payment transactions
- Generate customer-wise payment reports
- Perform aggregate calculations
- Use advanced SQL queries for data analysis

---

## 🛠️ Technologies Used

- PostgreSQL
- SQL
- pgAdmin 4
- Git
- GitHub

---

## 🗄️ Database Structure

The project contains two main tables:

### 1. Customer Table

The `customer` table stores customer information.

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| customer_id | BIGINT | PRIMARY KEY | Unique customer ID |
| first_name | VARCHAR(50) | | Customer first name |
| last_name | VARCHAR(50) | | Customer last name |
| email | VARCHAR(100) | | Customer email |
| address_id | BIGINT | | Address reference |

### 2. Payment Table

The `payment` table stores payment transaction information.

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| payment_id | BIGINT | PRIMARY KEY | Unique payment ID |
| customer_id | BIGINT | FOREIGN KEY | Related customer |
| amount | NUMERIC(10,2) | | Payment amount |
| mode | VARCHAR(50) | | Payment method |
| payment_date | DATE | | Payment date |

---

## 🔗 Database Relationship

The `customer_id` column connects the `customer` and `payment` tables.

```text
        CUSTOMER
        --------
        customer_id
             |
             |
             | 1 : N
             |
             ↓
        PAYMENT
        -------
        payment_id
        customer_id
        amount
        mode
        payment_date
