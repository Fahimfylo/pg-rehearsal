# PostgreSQL Practice 🐘

A structured repository of SQL scripts, database schemas, and hands-on exercises designed to build and sharpen PostgreSQL skills—from foundational queries to advanced database optimization.

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
├── 01-basics/              # SELECT, WHERE, ORDER BY, LIMIT, aliases
├── 02-joins-and-unions/    # INNER, LEFT, RIGHT, FULL OUTER, CROSS JOIN, UNION
├── 03-aggregations/        # GROUP BY, HAVING, COUNT, SUM, AVG, MIN, MAX
├── 04-subqueries-and-ctes/ # Nested queries, Common Table Expressions (WITH), recursive CTEs
├── 05-window-functions/    # ROW_NUMBER, RANK, DENSE_RANK, LAG, LEAD, PARTITION BY
├── 06-ddl-and-dml/         # CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, constraints
├── 07-indexing-and-perf/   # B-Tree, GIN, GiST indexes, EXPLAIN ANALYZE, query tuning
├── 08-advanced-features/   # Views, Materialized Views, Triggers, Stored Procedures, JSONB
├── datasets/               # Sample SQL dump files and CSV data for practice tables
└── README.md
```

---

## 🎯 Topics Covered

- **Core Querying:** Filtering, sorting, pattern matching (`LIKE`, `ILIKE`, regex), and handling `NULL` values.
- **Data Modeling & Constraints:** Primary keys, foreign keys, `UNIQUE`, `CHECK`, `NOT NULL`, and normalization.
- **Joins & Set Operations:** Combining data across multiple relational tables.
- **Analytics & Reporting:** Aggregations, window functions, and grouping sets (`ROLLUP`, `CUBE`).
- **PostgreSQL-Specific Power Features:** Working with `JSONB`, arrays, full-text search, and custom functions (`PL/pgSQL`).
- **Performance Tuning:** Reading query execution plans and creating effective indexes.

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
git clone https://github.com<your-username>/postgresql-practice.git
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
Run the seed script inside the `datasets/` folder to populate your tables:
```bash
psql -U postgres -d pg_practice -f datasets/init_schema.sql
psql -U postgres -d pg_practice -f datasets/seed_data.sql
```

---

## 💡 How to Practice

1. Navigate to a topic folder (e.g., `02-joins-and-unions/`).
2. Open the `problems.sql` file and try writing the queries yourself before checking `solutions.sql`.
3. Use `EXPLAIN ANALYZE` on your queries to inspect execution times and optimize slow scans.

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
