# PostgreSQL Practice 🐘

A structured repository of SQL scripts, database schemas, and hands-on exercises designed to build and sharpen PostgreSQL skills — from foundational database concepts and CRUD operations to advanced SQL features and database programming.

## 📋 Table of Contents

- [Repository Structure](#-repository-structure)
- [Topics Covered](#-topics-covered)
- [Prerequisites](#-prerequisites)
- [Getting Started](#-getting-started)
- [How to Practice](#-how-to-practice)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📂 Repository Structure

```text
postgresql-practice/
├── 01-database-and-crud/       # Database operations, CREATE, INSERT, SELECT, UPDATE, DELETE
├── 02-datatypes-and-constraints/ # Data types, PRIMARY KEY, NOT NULL, DEFAULT, CHECK
├── 03-data-refining/           # WHERE, ORDER BY, DISTINCT, LIMIT, LIKE
├── 04-operators-and-functions/ # Relational, logical, aggregate and string functions
├── 05-grouping-and-aggregation/ # GROUP BY, HAVING, COUNT, SUM, AVG, MIN, MAX
├── 06-table-alterations/       # ALTER TABLE, modifying table structures
├── 07-conditional-expressions/ # CASE expressions
├── 08-relationships-and-joins/ # Foreign keys, relationships and SQL JOINs
├── 09-views-and-subqueries/    # Views and advanced query composition
├── 10-stored-procedures/       # Stored procedures
├── 11-user-defined-functions/  # Custom SQL functions
├── 12-window-functions/       # ROW_NUMBER, RANK, DENSE_RANK, PARTITION BY
├── 13-ctes/                    # Common Table Expressions (WITH)
├── 14-triggers/                # Database triggers and automated actions
├── projects/                   # Practical database projects (E-Store)
├── datasets/                   # Sample SQL dump files and CSV data
└── README.md
```

---

## 🎯 Topics Covered

### 1. Database Fundamentals
- Database Concepts
- Database vs DBMS
- Relational Database Management Systems (RDBMS)
- Database vs Schema vs Table
- CRUD Operations

### 2. Database Operations (DDL & DML)
- CREATE DATABASE
- DROP DATABASE
- Listing and Switching Databases
- CREATE TABLE
- INSERT INTO
- SELECT
- UPDATE
- DELETE

### 3. Data Types & Constraints
- PostgreSQL Data Types
- PRIMARY KEY
- FOREIGN KEY
- NOT NULL
- DEFAULT
- UNIQUE
- CHECK Constraints

### 4. Data Refining & Filtering
- WHERE Clause
- ORDER BY
- DISTINCT
- LIMIT
- LIKE
- Filtering and Sorting Records

### 5. Operators
- Relational Operators
- Logical Operators
- Comparison Operators
- Combining Multiple Conditions

### 6. Aggregate Functions
- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()
- GROUP BY
- HAVING Clause

### 7. String Functions
- CONCAT()
- REPLACE()
- SUBSTRING()
- Common PostgreSQL String Operations

### 8. Table Modification
- ALTER TABLE
- Adding Columns
- Modifying Column Properties
- Renaming Columns
- Dropping Columns
- CHECK Constraints

### 9. Conditional Expressions
- CASE Expressions
- Conditional Data Transformation
- Categorizing Query Results

### 10. Relationships & Joins
- One-to-One Relationships
- One-to-Many Relationships
- Many-to-Many Relationships
- Foreign Key Relationships
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL OUTER JOIN
- CROSS JOIN

### 11. Views
- Creating Views
- Querying Views
- Updating and Dropping Views
- Reusable SQL Queries

### 12. Stored Procedures
- Creating Stored Procedures
- Executing Procedures
- Procedure Parameters
- Database-side Operations

### 13. User-Defined Functions
- Creating Custom Functions
- Function Parameters
- Return Types
- SQL Functions and PL/pgSQL Basics

### 14. Window Functions
- OVER()
- PARTITION BY
- ORDER BY in Window Functions
- ROW_NUMBER()
- RANK()
- DENSE_RANK()
- Aggregate Window Functions

### 15. Common Table Expressions (CTEs)
- WITH Clause
- Basic CTEs
- Multiple CTEs
- Using CTEs with Joins and Aggregations

### 16. Triggers
- Creating Triggers
- BEFORE and AFTER Triggers
- Trigger Functions
- Automatic Database Actions

### 17. Practical Projects
- Employee Database Management
- E-Commerce Database (E-Store)
- Relational Database Design
- Real-World SQL Query Exercises

---

## 🛠 Prerequisites

Before running the scripts in this repository, ensure you have the following installed:

- **PostgreSQL** (v14 or higher recommended)
- A SQL client or CLI tool such as **psql**, **pgAdmin**, **DBeaver**, or **DataGrip**
- *(Optional)* **Docker** if you prefer running PostgreSQL in a container

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/postgresql-practice.git
cd postgresql-practice
```

### 2. Set Up a Practice Database

**Option A: Using local PostgreSQL (`psql`)**

```bash
psql -U postgres -c "CREATE DATABASE pg_practice;"
```

**Option B: Using Docker**

```bash
docker run --name pg-practice \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=pg_practice \
  -p 5432:5432 \
  -d postgres:16
```

### 3. Load Sample Data

Run the seed scripts inside the `datasets/` folder:

```bash
psql -U postgres -d pg_practice -f datasets/init_schema.sql
psql -U postgres -d pg_practice -f datasets/seed_data.sql
```

---

## 💡 How to Practice

1. Navigate to a topic folder.
2. Review the topic-specific SQL scripts.
3. Try solving the exercises independently before checking the solutions.
4. Experiment with different queries and database structures.
5. Practice combining multiple concepts to solve real-world problems.

---

## 🤝 Contributing

Contributions, additional practice problems, and query optimizations are welcome!

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/add-window-exercises`).
3. Commit your changes (`git commit -m "Add advanced window function exercises"`).
4. Push to the branch (`git push origin feature/add-window-exercises`).
5. Open a Pull Request.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
