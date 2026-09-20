# 💳 Customer & Payment Management System

<p align="center">
  <strong>A PostgreSQL-based relational database project for managing customers, payments, and transaction analysis.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/SQL-Queries-orange?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/pgAdmin-4-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="pgAdmin">
  <img src="https://img.shields.io/badge/Git-GitHub-black?style=for-the-badge&logo=git&logoColor=white" alt="Git">
</p>

---

## 📌 About the Project

**Customer & Payment Management System** is a practical **PostgreSQL and SQL project** developed to manage customer information and payment transactions using a relational database.

The project demonstrates how customer and payment data can be stored, connected, filtered, grouped, and analyzed using SQL.

It includes practical implementation of:

- 🔗 JOINs
- 📊 GROUP BY
- 🔍 HAVING
- ➕ Aggregate Functions
- 🧩 Subqueries
- 🔄 Common Table Expressions (CTEs)
- 👁️ SQL Views
- 🔑 Primary & Foreign Keys

---

## 🎯 Project Objectives

The main objectives of this project are:

- Store customer information in a structured relational table.
- Store multiple payment transactions for each customer.
- Establish relationships using Primary Key and Foreign Key.
- Analyze customer payment transactions.
- Generate customer-wise payment reports.
- Calculate total, average, minimum, and maximum payments.
- Analyze payment methods.
- Practice advanced SQL queries using subqueries and CTEs.
- Create reusable SQL reports using Views.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| 🐘 PostgreSQL | Relational Database |
| 🧮 SQL | Data Management & Analysis |
| 🖥️ pgAdmin 4 | Database Management Tool |
| 🌿 Git | Version Control |
| 🐙 GitHub | Project Hosting |

---

# 🗄️ Database Architecture

The project contains two primary tables:

```text
┌──────────────────────────────┐
│          CUSTOMER            │
├──────────────────────────────┤
│ PK  customer_id             │
│     first_name              │
│     last_name               │
│     email                   │
│     address_id              │
└──────────────┬───────────────┘
               │
               │ 1
               │
               │
               │ N
┌──────────────▼───────────────┐
│           PAYMENT            │
├──────────────────────────────┤
│ PK  payment_id              │
│ FK  customer_id             │
│     amount                  │
│     mode                    │
│     payment_date            │
└──────────────────────────────┘
