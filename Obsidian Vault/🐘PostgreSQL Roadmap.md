# [[VANITY]], [[topics to cover]],

## 🟢 Phase 1: Introduction & Setup
- [ ] Understand what PostgreSQL is and its use cases
- [ ] Install PostgreSQL on local machine (Linux, macOS, Windows)
- [ ] Access PostgreSQL using:
  - [ ] `psql` CLI
  - [ ] GUI tools like pgAdmin, DBeaver
- [ ] Understand how PostgreSQL uses roles (users) and databases
- [ ] Create and connect to a database

## 🟡 Phase 2: SQL Basics with PostgreSQL
- [ ] Basic SQL syntax (keywords, case sensitivity, semicolon)
- [ ] Create tables using `CREATE TABLE`
- [ ] Insert data using `INSERT INTO`
- [ ] Select data using `SELECT`
- [ ] Use `WHERE`, `AND`, `OR`, `NOT`
- [ ] Use comparison operators: `=`, `<`, `>`, `BETWEEN`, `LIKE`, `IN`

## 🟠 Phase 3: Core SQL Features
- [ ] Understand data types (numeric, text, boolean, date/time)
- [ ] Update data with `UPDATE`
- [ ] Delete records with `DELETE`
- [ ] Sorting data with `ORDER BY`
- [ ] Limit results using `LIMIT` and `OFFSET`
- [ ] Aliasing with `AS`
- [ ] NULL handling with `IS NULL`, `COALESCE`, `NULLIF`

## 🔵 Phase 4: Schema Design & Relationships
- [ ] Understand normalization and denormalization
- [ ] Use `PRIMARY KEY`, `UNIQUE`, `NOT NULL`, `CHECK` constraints
- [ ] Define foreign key relationships
- [ ] Create `JOIN`s:
  - [ ] `INNER JOIN`
  - [ ] `LEFT JOIN`
  - [ ] `RIGHT JOIN`
  - [ ] `FULL JOIN`
- [ ] Understand indexes and performance

## 🟣 Phase 5: Aggregate Functions & Grouping
- [ ] Use `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- [ ] Use `GROUP BY` and `HAVING`
- [ ] Create subqueries in `WHERE`, `FROM`, and `SELECT`

## 🔶 Phase 6: Advanced PostgreSQL Features
- [ ] Use `DISTINCT`, `CASE`, `FILTER`
- [ ] Use Common Table Expressions (CTEs) with `WITH`
- [ ] Write recursive queries
- [ ] Perform `UPSERT` with `ON CONFLICT`
- [ ] Use `RETURNING` to fetch modified data
- [ ] Generate series with `generate_series()`

## 🟤 Phase 7: Data Modeling & Advanced Types
- [ ] Create and manage schemas
- [ ] Use `ENUM`, `ARRAY`, `UUID`, `JSON`, `JSONB`
- [ ] Use HSTORE (key-value pairs)
- [ ] Store hierarchical data (e.g., adjacency list, ltree)

## 🧩 Phase 8: User Management & Security
- [ ] Create users and roles
- [ ] Grant and revoke permissions
- [ ] Understand schema and table privileges
- [ ] Manage roles, groups, and inheritance
- [ ] Use `pg_hba.conf` and `postgresql.conf`

## 🧪 Phase 9: Performance & Optimization
- [ ] Analyze query plans using `EXPLAIN` and `EXPLAIN ANALYZE`
- [ ] Use `ANALYZE`, `VACUUM`, and `REINDEX`
- [ ] Tune configuration parameters for performance
- [ ] Partition tables and use table inheritance
- [ ] Optimize indexes (B-tree, Hash, GIN, GiST)

## 🔁 Phase 10: Backup, Restore & Replication
- [ ] Backup databases with `pg_dump` and `pg_dumpall`
- [ ] Restore with `psql` or `pg_restore`
- [ ] Enable WAL archiving and point-in-time recovery
- [ ] Set up streaming replication
- [ ] Use logical replication and `pglogical`

## 🧠 Phase 11: PL/pgSQL & Stored Procedures
- [ ] Learn PL/pgSQL syntax
- [ ] Write functions with `CREATE FUNCTION`
- [ ] Use triggers and `AFTER`, `BEFORE` events
- [ ] Write stored procedures using `CALL`
- [ ] Use `RAISE NOTICE`, `EXCEPTION`, and control flow

## ⚙️ Phase 12: Extensions & Ecosystem
- [ ] Install and use popular extensions:
  - [ ] `pg_stat_statements`
  - [ ] `PostGIS` (geospatial support)
  - [ ] `uuid-ossp`
  - [ ] `pg_trgm` (fuzzy string matching)
  - [ ] `citext` (case-insensitive text)
- [ ] Use foreign data wrappers (FDWs)
- [ ] Monitor performance with `pg_stat_activity`

## 🧑‍🔬 Phase 13: Real-world Projects
- [ ] Design a normalized schema for a blog/e-commerce
- [ ] Build a reporting dashboard with CTEs and JSON
- [ ] Write a backup + restore automation script
- [ ] Benchmark indexing impact on large queries
- [ ] Integrate PostgreSQL with Python, Node.js, or Go

## 📚 Bonus: Best Practices and References
- [ ] Always back up before making schema changes
- [ ] Avoid `SELECT *` in production queries
- [ ] Use proper data types and constraints
- [ ] Keep functions small and modular
- [ ] Read the [official PostgreSQL documentation](https://www.postgresql.org/docs/)
- [ ] Follow [PostgreSQL style guide](https://wiki.postgresql.org/wiki/SQL_Coding_Conventions)

