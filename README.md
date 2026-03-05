# MySQL Simulator Pro

![MySQL Simulator Pro](https://img.shields.io/badge/MySQL_Simulator-Pro-f97316?style=for-the-badge&logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Database](https://img.shields.io/badge/Database-Simulation-38bdf8?style=for-the-badge&logo=database&logoColor=white)

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-LIVE-f97316?style=for-the-badge&labelColor=1a1f2e" />
  <img src="https://img.shields.io/badge/TABLES-15%2B-38bdf8?style=for-the-badge&labelColor=1a1f2e" />
  <img src="https://img.shields.io/badge/COMMANDS-50%2B-4ade80?style=for-the-badge&labelColor=1a1f2e" />
  <img src="https://img.shields.io/badge/INDEXES-CREATE-f87171?style=for-the-badge&labelColor=1a1f2e" />
</p>

---

## Overview

This project is a **fully functional MySQL simulator** built with **HTML, CSS, and JavaScript**. It replicates core MySQL features, including **DDL, DML, transactions, indexes, and security**, while maintaining a **realistic database structure**. The simulator supports **multi-query execution**, **syntax highlighting**, and **interactive schema browsing**, making it ideal for learning and practicing SQL without a live database.

## ✨ Key Features

### 🗄️ **Complete SQL Execution Engine**

| Command Type           | Supported | Examples                                                        |
| ---------------------- | --------- | --------------------------------------------------------------- |
| **DDL**          | ✅ Full   | `CREATE TABLE`, `ALTER TABLE`, `DROP TABLE`, `TRUNCATE` |
| **DML**          | ✅ Full   | `SELECT`, `INSERT`, `UPDATE`, `DELETE`                  |
| **Indexes**      | ✅ Full   | `CREATE INDEX`, `DROP INDEX`, `SHOW INDEXES`              |
| **Transactions** | ✅ Full   | `BEGIN`, `COMMIT`, `ROLLBACK`, `SAVEPOINT`              |
| **Security**     | ✅ Full   | `CREATE USER`, `GRANT`, `REVOKE`, `SHOW GRANTS`         |
| **Explains**     | ✅ Full   | `EXPLAIN`, `ANALYZE TABLE`                                  |

### 📊 **6 Core Modules**

| Module                         | Focus             | Description                                                                          |
| ------------------------------ | ----------------- | ------------------------------------------------------------------------------------ |
| **01 — Editor**         | SQL Execution     | Professional code editor with line numbers, syntax highlighting, multi-query support |
| **02 — Schema Browser** | Database Explorer | Interactive table viewer with columns, indexes, foreign keys, and preview queries    |
| **03 — Index Manager**  | Performance       | Visual index management with unique indexes and estimated cardinality                |
| **04 — Security Panel** | RBAC              | User/role management with granular table privileges                                  |
| **05 — Lessons**        | Learning          | Categorized SQL tutorials with runnable examples                                     |
| **06 — Results**        | Output            | Multiple tabs: Results, Explain Plan, Performance, Messages, History                 |

---

## 🖥️ **Module 01: SQL Editor**

### **Professional Editor Features** ✍️

- **Line numbers** synchronized with scroll
- **Multi-query execution** with semicolon splitting
- **Keyboard shortcuts**: `Ctrl+Enter` to run, `Tab` for indentation
- **Format SQL** button for basic keyword capitalization
- **Clear** button to reset editor
- **Explain mode** toggle for execution plan visualization

### **Supported SQL Syntax** 🔤

```sql
-- All standard SQL commands
SELECT * FROM customers WHERE country = 'US';
INSERT INTO products (product_id, name, price) VALUES (101, 'Laptop', 999.99);
UPDATE employees SET salary = salary * 1.05 WHERE department = 'Engineering';
DELETE FROM orders WHERE order_date < '2020-01-01';

-- Transactions
BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE id = 1;
UPDATE accounts SET balance = balance + 100 WHERE id = 2;
COMMIT;

-- Indexes
CREATE INDEX idx_lastname ON employees(last_name);
DROP INDEX idx_lastname ON employees;
SHOW INDEXES FROM customers;

-- Security
CREATE USER 'analyst' IDENTIFIED BY 'password';
GRANT SELECT, INSERT ON customers TO analyst;
GRANT analyst TO 'jane_doe';
```

---

## 📂 **Module 02: Schema Browser**

### **Built-in Tables** 📋

| Table                           | Columns | Rows | Description                                 |
| ------------------------------- | ------- | ---- | ------------------------------------------- |
| **CUSTOMERS**             | 5       | 8    | Customer master data with email and country |
| **ORDERS**                | 5       | 8    | Order header with dates and totals          |
| **PRODUCTS**              | 5       | 7    | Product catalog with pricing and stock      |
| **ORDER_ITEMS**           | 5       | 8    | Order line items with quantities            |
| **COUNTRY**               | 3       | 7    | Country codes and names                     |
| **CHICAGO_SCHOOLS**       | 5       | 8    | School performance metrics                  |
| **CHICAGO_SOCIOECONOMIC** | 4       | 8    | Socioeconomic indicators                    |
| **EMPLOYEES**             | 8       | 10   | Employee data with departments              |
| **DEPARTMENTS**           | 4       | 5    | Department details                          |
| **BOOKS**                 | 6       | 6    | Library catalog                             |
| **MEMBERS**               | 5       | 4    | Library members                             |
| **LOANS**                 | 6       | 4    | Book loans                                  |
| **STOCKS**                | 4       | 5    | Stock tickers                               |
| **STOCK_PRICES**          | 6       | 35   | Daily OHLCV data                            |
| **AIRLINES**              | 4       | 4    | Airline codes                               |
| **AIRPORTS**              | 4       | 5    | Airport codes                               |
| **FLIGHTS**               | 9       | 5    | Flight schedules                            |

### **Schema Features** 🔍

- **Search tables** with live filtering
- **Expand/collapse** to show columns
- **Visual indicators** for PK/FK/Indexes
- **Column types** displayed inline
- **One-click preview** button runs `SELECT * FROM table LIMIT 5`

---

## ⚡ **Module 03: Index Manager**

### **Index Operations** 🔧

- **Create indexes** with `CREATE INDEX ... ON table(column)`
- **Unique indexes** with `CREATE UNIQUE INDEX ...`
- **Drop indexes** with clickable "drop" links
- **View all indexes** per table with metadata

### **Index Display** 📊

- Index name
- Column(s) included
- Unique flag
- Cardinality estimate
- One-click drop with confirmation

### **Performance Impact** ⚙️

- Indexes affect `EXPLAIN` plan visualization
- Index scans shown in green, full table scans in orange
- Query optimizer simulation with cost estimates

---

## 🔐 **Module 04: Security Panel (RBAC)**

### **User Management** 👤

- **Built-in users**: `root` (admin), `analyst`, `viewer`
- **Create users**: `CREATE USER 'name' IDENTIFIED BY 'password'`
- **Drop users**: `DROP USER 'name'`

### **Role Management** 🏷️

- **Built-in roles**: `admin` (ALL), `analyst` (SELECT, INSERT, UPDATE), `readonly` (SELECT)
- **Create roles**: `CREATE ROLE role_name`
- **Grant roles**: `GRANT role_name TO 'user'`

### **Privilege Management** 🔑

- **Grant privileges**: `GRANT SELECT, INSERT ON table TO user/role`
- **Revoke privileges**: `REVOKE INSERT ON table FROM user/role`
- **Show grants**: `SHOW GRANTS FOR 'user'`

### **Current Session** 👁️

- Active user displayed in header
- Current roles and effective permissions
- Permission checking on every query

---

## 📚 **Module 05: Lessons Library**

### **4 Main Categories** 📖

| Category               | Lessons | Topics                                                        |
| ---------------------- | ------- | ------------------------------------------------------------- |
| **CREATE & DDL** | 3       | CREATE TABLE, DESCRIBE, DROP, Indexes                         |
| **ALTER TABLE**  | 2       | ADD COLUMN, DROP COLUMN, MODIFY, TRUNCATE                     |
| **SELECT & DML** | 5       | Basics, WHERE, Aggregates, INSERT/UPDATE/DELETE, Transactions |
| **JOINS**        | 3       | INNER JOIN, LEFT JOIN, Chicago JOIN Lab                       |

### **Lesson Features** 🎓

- **Expandable cards** with description
- **Multiple examples** per lesson
- **One-click load** to editor
- **Run automatically** after loading
- **Categorized by SQL operation**

---

## 📊 **Module 06: Results & Analytics**

### **5 Result Tabs** 📑

| Tab                    | Content         | Features                                                |
| ---------------------- | --------------- | ------------------------------------------------------- |
| **Results**      | Query output    | Formatted table, NULL handling, numeric highlighting    |
| **Explain Plan** | Execution plan  | Visual node tree, cost estimates, index recommendations |
| **Performance**  | Query profiling | Min/avg/max times, distribution chart, query comparison |
| **Messages**     | Execution log   | Success/error messages, timestamps, hints               |
| **History**      | Query history   | Last 40 queries with status, time, click to reload      |

### **Explain Plan Visualization** 🔍

- **Node types**: FULL SCAN, INDEX SCAN, JOIN, FILTER, SORT, LIMIT, PROJECTION
- **Color coding** by operation type
- **Step numbers** and execution order
- **Cost estimates** per node
- **Total cost** at top
- **Optimization tips** when full scans detected

### **Performance Profiler** ⏱️

- **Run iterations**: 10–500 runs
- **Metrics**: Min, Avg, Median, P95
- **Distribution chart** with histogram bars
- **Query comparison** A/B testing
- **Percentage difference** calculation

---

## 🎨 **Design & Aesthetics**

### **Professional Database IDE** 🖥️

- **Dark background** (`#1a1f2e`) — easy on the eyes for long coding sessions
- **Orange accent** (`#f97316`) for primary actions and run button
- **Cyan** (`#38bdf8`) for information and data types
- **Green** (`#4ade80`) for success and indexes
- **Red** (`#f87171`) for errors and destructive actions
- **Purple** (`#c084fc`) for security and schema builder
- **Pink** (`#f472b6`) for special features

### **Typography** ✍️

- **Bebas Neue** — Bold headers, logo
- **JetBrains Mono** — Code editor, SQL syntax, table data
- **Nunito** — UI elements, buttons, labels

### **UI Components** 🖼️

- **Tabbed interfaces** throughout (editor/results, sidebar panels)
- **Expandable schema** with animated arrows
- **Status bar** with current section, table/index counts, user
- **Modal dialogs** for import, schema builder, security
- **Toast notifications** for user feedback

### **Color Coding** 🎨

| Element               | Color  | Hex         | Usage             |
| --------------------- | ------ | ----------- | ----------------- |
| **CREATE/DDL**  | Cyan   | `#38bdf8` | CREATE operations |
| **ALTER**       | Purple | `#c084fc` | ALTER operations  |
| **SELECT**      | Orange | `#f97316` | SELECT queries    |
| **JOINS**       | Green  | `#4ade80` | JOIN operations   |
| **Indexes**     | Green  | `#4ade80` | Index indicators  |
| **Primary Key** | Orange | `#f97316` | PK badge          |
| **Foreign Key** | Cyan   | `#38bdf8` | FK badge          |
| **Unique Key**  | Green  | `#4ade80` | UQ badge          |
| **CSV Import**  | Purple | `#c084fc` | CSV badge         |

---

## 🛠️ **Technical Implementation**

### **Architecture**

```
┌─────────────────────────────────────┐
│      MySQL Simulator Pro            │
├─────────────────────────────────────┤
│                                     │
│  ┌─────────────────────────────┐   │
│  │   Core Database Engine      │   │
│  │   • In-memory DB object     │   │
│  │   • 15+ built-in tables    │   │
│  │   • Full DDL/DML/DQL       │   │
│  │   • Transaction state      │   │
│  │   • Index management       │   │
│  │   • RBAC permissions       │   │
│  └─────────────────────────────┘   │
│                                     │
│  ┌─────────────────────────────┐   │
│  │   SQL Parser & Executor     │   │
│  │   • Multi-statement split  │   │
│  │   • WHERE evaluator        │   │
│  │   • JOIN engine            │   │
│  │   • Aggregation functions  │   │
│  │   • Subquery support       │   │
│  └─────────────────────────────┘   │
│                                     │
│  ┌─────────────────────────────┐   │
│  │   Query Optimizer           │   │
│  │   • EXPLAIN plan builder   │   │
│  │   • Index detection        │   │
│  │   • Cost estimation        │   │
│  │   • Performance profiling  │   │
│  └─────────────────────────────┘   │
│                                     │
│  ┌─────────────────────────────┐   │
│  │   UI Components             │   │
│  │   • Editor with line nums  │   │
│  │   • Schema browser         │   │
│  │   • Results tabs           │   │
│  │   • Lesson library         │   │
│  │   • Modals & toast         │   │
│  └─────────────────────────────┘   │
└─────────────────────────────────────┘
```

### **Key Functions**

```javascript
// Core execution
executeStatement(sql)           // Parse and execute any SQL statement
execSelect(sql)                 // SELECT with WHERE, JOINs, GROUP BY
execInsert(sql)                  // INSERT INTO ... VALUES
execUpdate(sql)                  // UPDATE with WHERE
execDelete(sql)                  // DELETE with WHERE

// DDL
execCreate(sql)                   // CREATE TABLE
execDrop(sql)                      // DROP TABLE
execAlter(sql)                     // ALTER TABLE
execTruncate(sql)                  // TRUNCATE TABLE

// Indexes
execCreateIndex(sql)               // CREATE INDEX
execDropIndex(sql)                  // DROP INDEX
execShowIndexes(sql)                // SHOW INDEXES

// Transactions
execBegin()                         // BEGIN TRANSACTION
execCommit()                        // COMMIT
execRollback()                       // ROLLBACK
execSavepoint()                      // SAVEPOINT
execRollbackTo()                     // ROLLBACK TO SAVEPOINT

// Security
execCreateUser(sql)                  // CREATE USER
execCreateRole(sql)                  // CREATE ROLE
execGrant(sql)                       // GRANT privileges/role
execRevoke(sql)                      // REVOKE
execShowUsers()                       // SHOW USERS
execShowRoles()                       // SHOW ROLES
execShowGrants()                      // SHOW GRANTS

// Analysis
buildExplainPlan(sql)                 // Generate execution plan
profileQuery(sql, iterations)         // Performance profiling
runComparison()                        // A/B query comparison

// UI
renderSchema()                         // Render schema browser
renderIndexPanel()                     // Render index manager
renderSecPanel()                       // Render security panel
showResult(res)                        // Display query results
```

---

## 📊 **Sample Queries**

### **Basic Queries**

```sql
-- All customers
SELECT * FROM CUSTOMERS;

-- Filtered customers
SELECT first_name, last_name, country FROM CUSTOMERS WHERE country = 'US';

-- Aggregation
SELECT country, COUNT(*) FROM CUSTOMERS GROUP BY country ORDER BY COUNT(*) DESC;

-- Join customers with orders
SELECT c.first_name, c.last_name, o.order_id, o.total_amount
FROM CUSTOMERS c
INNER JOIN ORDERS o ON c.customer_id = o.customer_id;
```

### **Advanced Queries**

```sql
-- Multi-table join with aggregation
SELECT c.country, COUNT(DISTINCT c.customer_id) AS customers,
       SUM(o.total_amount) AS total_revenue
FROM CUSTOMERS c
LEFT JOIN ORDERS o ON c.customer_id = o.customer_id
GROUP BY c.country
ORDER BY total_revenue DESC NULLS LAST;

-- Subquery
SELECT * FROM PRODUCTS 
WHERE price > (SELECT AVG(price) FROM PRODUCTS);

-- Window function (simulated via subquery)
SELECT product_name, price, 
       (SELECT COUNT(*) FROM PRODUCTS p2 WHERE p2.price > p1.price) + 1 AS rank
FROM PRODUCTS p1
ORDER BY price DESC;
```

### **Transactions**

```sql
BEGIN;
UPDATE PRODUCTS SET price = price * 1.10 WHERE category = 'Electronics';
SAVEPOINT after_update;
DELETE FROM PRODUCTS WHERE stock_qty = 0;
ROLLBACK TO after_update;  -- Keep price update, undo deletion
COMMIT;
```

### **Index & Performance**

```sql
-- Create index
CREATE INDEX idx_country ON CUSTOMERS(country);

-- Explain plan
EXPLAIN SELECT * FROM CUSTOMERS WHERE country = 'US';

-- Analyze table
ANALYZE TABLE CUSTOMERS;
```

### **Security Examples**

```sql
-- Create user with password
CREATE USER 'analyst1' IDENTIFIED BY 'secure123';

-- Grant table privileges
GRANT SELECT, INSERT ON ORDERS TO analyst1;

-- Create role
CREATE ROLE finance_reader;

-- Grant role to user
GRANT finance_reader TO analyst1;

-- See effective grants
SHOW GRANTS FOR analyst1;
```

---

## 🎥 **Video Demo Script** (60-75 seconds)

| Time | Module      | Scene   | Action                                                                             |
| ---- | ----------- | ------- | ---------------------------------------------------------------------------------- |
| 0:00 | Header      | Logo    | Show "MySQL Simulator Pro" with orange accent                                      |
| 0:05 | Editor      | Run     | Run query:`SELECT * FROM CUSTOMERS` → 8 rows returned                           |
| 0:10 | Editor      | Explain | Toggle Explain mode, run join query → visual plan appears                         |
| 0:15 | Schema      | Browse  | Click CUSTOMERS table → columns shown, click preview → query loads               |
| 0:20 | Indexes     | Create  | Run `CREATE INDEX idx_country ON CUSTOMERS(country)` → index appears in manager |
| 0:25 | Security    | Show    | Show current user `root`, roles admin, permissions ALL                           |
| 0:30 | Lessons     | Select  | Click "WHERE Filters" lesson → loads example, runs automatically                  |
| 0:35 | Performance | Profile | Run performance profile on 2 queries → distribution chart                         |
| 0:40 | Results     | History | Show query history with timestamps, click to reload                                |
| 0:45 | Import      | CSV     | Open import modal, show sample datasets                                            |
| 0:50 | Export      | JSON    | Export current database schema                                                     |
| 0:55 | Status      | Bar     | Show 15 tables, 3 indexes, user root                                               |

---

## 🚦 **Performance**

- **Load Time**: < 2 seconds (no external dependencies beyond Google Fonts)
- **Memory Usage**: < 60 MB
- **Query Speed**: Sub-millisecond for simple queries
- **Transaction Handling**: Full ACID simulation with savepoints

---

## 🛡️ **Security Notes**

MySQL Simulator Pro is a **completely safe** educational tool:

- ✅ No actual database connections
- ✅ All data stored in browser memory
- ✅ No data collection or tracking
- ✅ No external dependencies
- ✅ Pure HTML/CSS/JavaScript
- ✅ Educational purposes only — learn SQL concepts safely

---

## 📝 **License**

MIT License — see LICENSE file for details.

---

## 🙏 **Acknowledgments**

- **MySQL** — Original SQL syntax and features
- **PostgreSQL** — Window functions inspiration
- **SQLite** — In-memory database concept
- **IBM Data Science Curriculum** — SQL learning objectives
- **JetBrains** — Mono font for coding

---

## 📧 **Contact**

- **GitHub Issues**: [Create an issue](https://github.com/Willie-Conway/MySQL-Simulator-Pro/issues)
- **Website**: https://willie-conway.github.io/MySQL-Simulator-Pro/

---

## 🏁 **Future Enhancements**

- [ ] Add window functions (RANK, LAG, LEAD)
- [ ] Implement stored procedures
- [ ] Add triggers simulation
- [ ] Include views with materialization
- [ ] Add user-defined functions
- [ ] Implement query cache simulation
- [ ] Add more sample datasets
- [ ] Include SQL injection demo (safe)
- [ ] Add normalization exercises
- [ ] Include database design patterns

---

<p align="center">
  <strong>🗄️ MySQL Simulator Pro — The Ultimate SQL Learning Environment 🗄️</strong>
</p>

*Last updated: March 2025*
