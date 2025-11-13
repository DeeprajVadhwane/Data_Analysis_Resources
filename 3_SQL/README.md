# 📘 SQL Mastery: From Beginner to Advanced — Admission Management System

> **Objective:** A complete open-source SQL learning repository designed for self-learners, students, and professionals. This repository explains every SQL concept with clear theory, syntax, and real-world education-based examples (Admission Database).

## Repository Overview

This repo is structured as a complete course + working example. It contains:

* A realistic **Admission Management System** schema and seed data.
* Step-by-step lessons from **Beginner → Intermediate → Advanced**.
* Hands-on **exercises** with solutions and teacher notes.
* SQL scripts grouped by topic (DDL, DML, Queries, Indexing, Window Functions, Performance, Security, Backup).
* Best practices, cheat-sheets, and classroom-ready assignments.

---
SQL-Mastery/
│
├── 📁 01_Basics/
│   ├── 1_Introduction_to_SQL.md
│   ├── 2_Database_Terminology.md
│   ├── 3_Data_Types.md
│   ├── 4_SQL_Commands.md
│
├── 📁 02_Intermediate/
│   ├── 1_Operators.md
│   ├── 2_Constraints.md
│   ├── 3_Clauses.md
│   ├── 4_Functions.md
│
├── 📁 03_Advanced/
│   ├── 1_Joins.md
│   ├── 2_Subqueries.md
│   ├── 3_CTEs.md
│   ├── 4_Windows_Functions.md
│   ├── 5_Views_&_StoredProcedures.md
│
├── 📁 04_Expert/
│   ├── 1_Performance_Optimization.md
│   ├── 2_Transactions.md
│   ├── 3_Dynamic_SQL.md
│   ├── 4_Triggers.md
│
├── 📁 05_Projects/
│   ├── Admission_Analytics_Project.md
│   ├── Student_Performance_Report.md
│   ├── Fee_Payment_Insights.md
│
├── 📁 Assets/
│   ├── ER_Diagram.png
│   ├── Charts/
│   └── Sample_Data/
│
└── README.md

# 🧠 Introduction to SQL

## 📘 What is SQL?

**SQL (Structured Query Language)** is the standard programming language used to interact with **Relational Database Management Systems (RDBMS)** such as MySQL, PostgreSQL, Oracle, and SQL Server.

SQL allows you to:
- Store, manage, and retrieve structured data efficiently.
- Define data relationships using keys.
- Enforce rules and maintain data integrity.
- Perform analytical and transactional operations.

It’s the **language of data** — essential for developers, analysts, and data scientists.

---

## 🎯 Why Learn SQL?

SQL is a *foundational skill* for working with data.  
Whether you're creating dashboards, analyzing trends, or building applications — SQL is the bridge between data and insights.

### 💡 Real-World Example: Admission Management System
Imagine an educational institution managing thousands of student records:
- **Students Table:** Stores basic details (name, age, email, gender)
- **Departments Table:** Lists available departments and their heads
- **Admissions Table:** Tracks which student applied for which course
- **Fees Table:** Records payments and outstanding dues

SQL helps:
- Add new student admissions
- Retrieve students enrolled in a specific course
- Calculate total revenue from fees
- Generate reports by department

---

## 🏗️ What is a Database?

A **database** is an organized collection of data stored in a structured format.  
It allows easy access, management, and updating of data.

| Term | Description | Example |
|------|--------------|----------|
| **Database** | A collection of related tables | `Admission_DB` |
| **Table** | A structured set of data in rows & columns | `Students`, `Departments` |
| **Column (Field)** | A single attribute/variable | `Student_Name`, `Email` |
| **Row (Record)** | A single entry in a table | `('S001', 'Riya', 'CSE')` |
| **Primary Key** | Unique identifier for each record | `Student_ID` |
| **Foreign Key** | Links two related tables | `Department_ID` |
| **Schema** | Blueprint of the database structure | Defines all tables and relationships |

---

## 🧩 What is an RDBMS?

A **Relational Database Management System (RDBMS)** stores data in multiple tables connected by relationships.

Examples:
- **MySQL** — open-source, widely used
- **PostgreSQL** — enterprise-grade and feature-rich
- **SQLite** — lightweight and local
- **MS SQL Server** — Microsoft’s enterprise solution
- **Oracle** — robust and secure for large systems

Key RDBMS Features:
- Data stored in **tables** (rows and columns)
- Relationships maintained via **keys**
- Support for **SQL standard language**
- ACID compliance (ensures data reliability)
- Transaction support for multi-step operations

---

## 🧱 SQL vs NoSQL

| Feature | SQL (Relational) | NoSQL (Non-Relational) |
|----------|------------------|-------------------------|
| Structure | Tables (Rows & Columns) | Documents, Key-Value, Graph |
| Schema | Fixed schema | Dynamic / Flexible schema |
| Relationships | Supported via keys | Usually not supported |
| Use Case | Structured, consistent data | Unstructured or high-speed data |

> 🧭 **Pro Tip:** SQL is best for structured data like admissions, employees, or sales — where relationships and consistency matter.

# 🧩 Database Terminology

## 📘 Introduction

Before diving into SQL queries, it’s important to understand **how databases are structured** and the terms you’ll frequently use while working with them.

Think of a **database** as a digital version of a well-organized filing system.  
Each file, folder, and label has a purpose — similarly, databases have tables, columns, and keys that help manage data efficiently.

We’ll explore all of these below, using our **Admission Management System** as the example.

---

## 🏫 Real-World Example: Admission Management System

Imagine a university managing student data digitally.  
They maintain:
- A **Students Table** for personal details  
- A **Departments Table** for academic branches  
- A **Courses Table** for available subjects  
- An **Admissions Table** to record enrollments  

These tables together form the **Admission_DB** — a single structured database that keeps everything connected.

---

## 🧱 Core Database Terms

| Term | Description | Example in Admission_DB |
|------|--------------|--------------------------|
| **Database** | A collection of related data organized for easy access. | `Admission_DB` |
| **Table** | A structure that stores data in rows and columns. | `Students`, `Departments` |
| **Column (Field)** | Defines the type of data stored (attribute). | `Student_Name`, `Email`, `Course_ID` |
| **Row (Record)** | A single data entry in a table. | `(S101, Riya, CSE, 2024)` |
| **Primary Key (PK)** | A unique identifier for each record. | `Student_ID` |
| **Foreign Key (FK)** | Connects one table to another. | `Department_ID` in Students table links to Departments table |
| **Schema** | The structure or blueprint of the database. | All tables + their relationships |
| **Entity** | A real-world object represented as a table. | Student, Department |
| **Attribute** | Property of an entity. | Student_Name, Age, Gender |
| **Relationship** | Logical connection between two tables. | One Department → Many Students |

---

## 🗂️ Database Hierarchy Overview


> 🧭 Each table is connected using **Primary** and **Foreign Keys**, forming relationships that mimic real-world connections.

---

## 🔗 Understanding Relationships

| Relationship Type | Description | Example |
|--------------------|--------------|----------|
| **One-to-One (1:1)** | Each record in one table relates to exactly one record in another table. | Each department has one head (HOD). |
| **One-to-Many (1:N)** | One record in a table relates to multiple records in another. | One department → many students. |
| **Many-to-Many (M:N)** | Many records in one table relate to many in another (requires a linking table). | Students can enroll in multiple courses. |

---

## 🧾 Example Tables (Simplified)

### 🧍‍♀️ Students Table
| Student_ID | Student_Name | Gender | Department_ID |
|-------------|--------------|---------|----------------|
| S101 | Riya | F | D01 |
| S102 | Aman | M | D02 |

### 🏛️ Departments Table
| Department_ID | Department_Name | HOD |
|----------------|------------------|------|
| D01 | Computer Science | Dr. Meena |
| D02 | Mechanical | Dr. Rajesh |

### 🧮 Admissions Table
| Admission_ID | Student_ID | Course_ID | Admission_Date |
|---------------|-------------|------------|----------------|
| A001 | S101 | C001 | 2024-07-01 |
| A002 | S102 | C003 | 2024-07-02 |

---

## 🧠 Key Points to Remember

- A **database** is like a container for all related tables.  
- **Tables** store the actual data in a structured way.  
- **Primary keys** ensure uniqueness within a table.  
- **Foreign keys** maintain relationships between tables.  
- **Schemas** define how all pieces fit together logically.  
- Understanding these fundamentals helps you write better queries later.

---

## 🧩 In Simple Terms

| Concept | Easy Analogy |
|----------|----------------|
| **Database** | A school |
| **Table** | A classroom |
| **Column** | Attribute like “Subject” or “Teacher” |
| **Row** | A student in that classroom |
| **Primary Key** | Student Roll Number |
| **Foreign Key** | Department Code |


🧩 **Pro Tip for Learners:**  
Start visualizing your Admission_DB as a set of connected tables.  
Draw an **ER Diagram** on paper — it’s the best way to understand relationships between entities.

# 🔢 SQL Data Types

## 📘 Introduction
Data types define the **kind of information** a column can store — like numbers, text, or dates.  
Choosing the right data type is essential for:
- Efficient data storage  
- Accurate calculations  
- Maintaining database integrity  

In our **Admission Management Database**, we use a mix of numeric, text, and date data types to represent real-world data such as student marks, admission dates, fees, and names.

---

## 🧮 1. Numeric Data Types

Numeric data types are used to store **numbers** — whole or decimal — often used for marks, fees, or percentages.

| Data Type | Storage | Description | Example (Admission_DB) |
|------------|----------|--------------|--------------------------|
| **INT** | 4 bytes | Whole numbers | `student_id`, `department_id` |
| **SMALLINT** | 2 bytes | Smaller range of integers | `year_of_passing` |
| **BIGINT** | 8 bytes | Very large numbers | `aadhar_number` |
| **DECIMAL(p,s)** | Variable | Exact decimal values with precision | `percentage DECIMAL(5,2)` → 95.45 |
| **NUMERIC(p,s)** | Variable | Same as DECIMAL | `total_fees NUMERIC(10,2)` |
| **FLOAT** | 4 bytes | Approximate decimal values | `average_score` |
| **DOUBLE** | 8 bytes | High-precision floating-point | `CGPA` |

### 🧠 Example
```sql
CREATE TABLE fee_details (
    student_id INT,
    total_fees DECIMAL(10,2),
    fees_paid DECIMAL(10,2),
    remaining_fees AS (total_fees - fees_paid)
);
```

# 🧱 SQL Data Types — Complete Reference

This section explains the most common **SQL data types** with real-world examples using an **Admission Database** scenario.

---

## 💰 1. Numeric Data Types

💡 **Use `DECIMAL` for money or marks** — it gives accurate results, unlike `FLOAT` which can have rounding errors.

| Data Type | Storage | Description | Example (Admission_DB) |
|------------|----------|--------------|--------------------------|
| INT | 4 bytes | Whole numbers | student_id INT |
| DECIMAL(p, s) | Variable | Precise fixed-point numbers | percentage DECIMAL(5,2) |

---

## 2. Character (String) Data Types

These store **text, names, addresses, and descriptions.**

| Data Type | Storage | Description | Example (Admission_DB) |
|------------|----------|-------------|--------------------------|
| CHAR(n) | Fixed length | Always stores exactly `n` characters | gender CHAR(6) (‘Male’, ‘Female’) |
| VARCHAR(n) | Variable length | Stores only required characters | student_name VARCHAR(100) |
| TEXT | Up to 65,535 chars | Long text like feedback or notes | remarks TEXT |

###  Example
```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    full_name VARCHAR(100) NOT NULL,
    gender CHAR(6),
    email VARCHAR(100) UNIQUE
);
```

## 3. Date and Time Data Types

Used for storing time-based information — like admission date, date of birth, or payment timestamps.

| Data Type | Description | Example (Admission_DB) |
|------------|--------------|------------------------|
| **DATE** | Stores only date (YYYY-MM-DD) | dob, admission_date |
| **TIME** | Stores time (HH:MM:SS) | class_start_time |
| **DATETIME** | Stores both date & time | created_at, updated_at |
| **TIMESTAMP** | Auto-updated time value | record_modified |
| **YEAR** | Stores 4-digit year | year_of_passing |

###  Example
```sql
CREATE TABLE admissions (
    admission_id INT PRIMARY KEY AUTO_INCREMENT,
    student_id INT,
    admission_date DATE NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
## 4. Boolean Data Type

Used for storing **true/false** or **yes/no** values.

| Data Type | Description | Example |
|------------|--------------|----------|
| **BOOLEAN / BOOL** | Stores TRUE or FALSE (internally 0 or 1) | is_active, is_eligible |

### Example
```sql
CREATE TABLE course_registration (
    student_id INT,
    course_id INT,
    is_approved BOOLEAN DEFAULT FALSE
);
```
## 5. Binary Data Types (Advanced)

Used for storing **non-text data** like images, PDFs, or certificates.

| Data Type | Description | Example |
|------------|--------------|----------|
| **BLOB** | Binary Large Object | Store scanned documents |
| **VARBINARY(n)** | Variable-length binary data | Digital signature |

### Example
```sql
CREATE TABLE documents (
    doc_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    certificate BLOB
);
```
```
# 🔐 SQL Constraints and Keys — Complete Guide

Constraints are rules applied to columns to **maintain data integrity** and ensure valid, consistent data is stored in the database.


##  1. What Are Constraints?

Constraints restrict the type of data that can go into a table column.  
They help prevent invalid data entry (like negative age or duplicate emails).

💡 **Example:**  
You can prevent duplicate student emails using a `UNIQUE` constraint,  
or stop empty name fields using a `NOT NULL` constraint.

##  2. Common Types of Constraints

| Constraint | Description | Example Use |
|-------------|--------------|--------------|
| **NOT NULL** | Ensures a column cannot have NULL values | `student_name` must always have a value |
| **UNIQUE** | Ensures all values in a column are unique | Email IDs or Roll Numbers |
| **PRIMARY KEY** | Uniquely identifies each record | `student_id` |
| **FOREIGN KEY** | Links two tables together | `student_id` in admissions references students |
| **CHECK** | Validates values based on a condition | Age must be >= 18 |
| **DEFAULT** | Sets a default value when none is provided | Default `status = 'Pending'` |
| **AUTO_INCREMENT** | Automatically generates unique IDs | Student ID auto-increments |


## 3. NOT NULL Constraint

Ensures a column cannot have empty (NULL) values.

```sql
CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100),
    gender CHAR(6)
);
```

## 4. UNIQUE Constraint

Ensures all values in a column are unique (no duplicates).

CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(100) UNIQUE,
    phone_number VARCHAR(15) UNIQUE
);

💡 Use UNIQUE for attributes like email, roll number, or Aadhar number.

## 5. PRIMARY KEY Constraint

The PRIMARY KEY uniquely identifies each record in a table.
Every table should have one primary key.
```sql
CREATE TABLE departments (
    dept_id INT PRIMARY KEY AUTO_INCREMENT,
    dept_name VARCHAR(50) NOT NULL
);

```
💡**Rules:**

Each table can have only one PRIMARY KEY.

Primary keys cannot be NULL.

They are often combined with AUTO_INCREMENT.

## 6. FOREIGN KEY Constraint

A FOREIGN KEY links two tables together and enforces referential integrity.
```sql
CREATE TABLE admissions (
    admission_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    admission_date DATE,
    FOREIGN KEY (student_id) REFERENCES students(student_id)
);
```

💡 Example:
If a student record is deleted, you can control what happens to related admissions:

CASCADE: Delete related admissions automatically.

SET NULL: Set student_id to NULL.

NO ACTION: Prevent deletion if referenced.

 Example with CASCADE

FOREIGN KEY (student_id) REFERENCES students(student_id)
ON DELETE CASCADE;

## 7. CHECK Constraint

Validates data based on a condition before inserting.
```sql
CREATE TABLE marks (
    mark_id INT AUTO_INCREMENT PRIMARY KEY,
    marks_obtained INT CHECK (marks_obtained BETWEEN 0 AND 100)
);
```
💡 Prevents invalid marks (like -10 or 120) from being inserted.

## 8. DEFAULT Constraint

Sets a default value for a column if no value is provided.

CREATE TABLE course_registration (
    reg_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    status VARCHAR(20) DEFAULT 'Pending'
);


💡 Common defaults:

Boolean flags → DEFAULT TRUE

Status fields → DEFAULT 'Active'

Timestamps → DEFAULT CURRENT_TIMESTAMP

🧩 9. AUTO_INCREMENT

Automatically generates sequential numbers for primary keys.

CREATE TABLE departments (
    dept_id INT AUTO_INCREMENT PRIMARY KEY,
    dept_name VARCHAR(50)
);


💡 No need to manually insert IDs — they’re generated automatically.

🔗 10. Combining Constraints

You can apply multiple constraints on a single column.
```sql
CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    age INT CHECK (age >= 18)
);
```

## 🧭 11. Quick Summary

| Constraint | Purpose | Example |
|-------------|----------|----------|
| **NOT NULL** | Prevent empty values | full_name NOT NULL |
| **UNIQUE** | Prevent duplicates | email UNIQUE |
| **PRIMARY KEY** | Unique identifier | student_id |
| **FOREIGN KEY** | Table relationships | student_id → students |
| **CHECK** | Validate conditions | age >= 18 |
| **DEFAULT** | Assign default value | status DEFAULT 'Active' |
| **AUTO_INCREMENT** | Auto-generate IDs | student_id AUTO_INCREMENT |


```sql
CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    age INT CHECK (age >= 18),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE admissions (
    admission_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    admission_date DATE NOT NULL,
    FOREIGN KEY (student_id) REFERENCES students(student_id)
);

```

# 🤝 SQL Relationships and Joins — Complete Guide

Understanding **relationships** between tables and mastering **SQL JOINs** is at the heart of database design and querying.  
These concepts allow you to connect and analyze data spread across multiple tables.

---

## 🧭 1. What Are Relationships in Databases?

A **relationship** defines how data in one table relates to data in another table.  
Relational databases store data in multiple tables connected by **keys**.

### 🔑 Key Terms
| Term | Description |
|------|--------------|
| **Primary Key (PK)** | Uniquely identifies each record in a table |
| **Foreign Key (FK)** | A field in one table that refers to the Primary Key in another table |
| **Referential Integrity** | Ensures consistency between related tables (e.g., you cannot have an admission for a non-existent student) |

---
--- ---
##  2. Types of Relationships

There are **three main types** of relationships in SQL:

###  1. One-to-One (1:1)

Each record in **Table A** is linked to **only one record** in **Table B**.

####  Example:
- One **student** has one **student_profile**.

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100)
);

CREATE TABLE student_profiles (
    profile_id INT PRIMARY KEY,
    student_id INT UNIQUE,
    address VARCHAR(255),
    phone_number VARCHAR(15),
    FOREIGN KEY (student_id) REFERENCES students(student_id)
);
```
## 2. One-to-Many (1:N)

A single record in **Table A** can relate to multiple records in **Table B**.  
This is the most common relationship in databases.

📘 **Example:**  
One student can have many admissions.

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100)
);

CREATE TABLE admissions (
    admission_id INT PRIMARY KEY,
    student_id INT,
    course_name VARCHAR(50),
    admission_date DATE,
    FOREIGN KEY (student_id) REFERENCES students(student_id)
);
```

## 3. Many-to-Many (M:N)

Each record in **Table A** can relate to multiple records in **Table B**,  
and vice versa.

To implement this, we use a **junction (bridge) table**.

📘 **Example:**  
Many students can enroll in many courses.

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100)
);

CREATE TABLE courses (
    course_id INT PRIMARY KEY,
    course_name VARCHAR(100)
);

CREATE TABLE student_courses (
    student_id INT,
    course_id INT,
    PRIMARY KEY (student_id, course_id),
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id)
);
```
## 3. SQL JOINS — Connecting Data

When querying data from multiple related tables, we use **JOINS** to combine them based on related columns.

| Type | Description |
|------|--------------|
| **INNER JOIN** | Returns records with matching values in both tables |
| **LEFT JOIN** | Returns all records from the left table, and matched records from the right |
| **RIGHT JOIN** | Returns all records from the right table, and matched records from the left |
| **FULL JOIN** | Returns all records when there is a match in either left or right table |
| **CROSS JOIN** | Returns all possible combinations (Cartesian product) |

## 4. INNER JOIN

Returns only rows with **matching values** in both tables.

```sql
SELECT students.full_name, admissions.course_name
FROM students
INNER JOIN admissions
ON students.student_id = admissions.student_id;
```

📊 **Result:**

| full_name   | course_name   |
|--------------|---------------|
| Riya Sharma  | Data Science  |
| Riya Sharma  | SQL Basics    |

🧠 **Concept:**  
If a student doesn’t have an admission, they **won’t appear** in the result.

## 5. LEFT JOIN (LEFT OUTER JOIN)

Returns **all records from the left table**,  
and the **matching records** from the right table (if any).

```sql
SELECT students.full_name, admissions.course_name
FROM students
LEFT JOIN admissions
ON students.student_id = admissions.student_id;
```
## 6. RIGHT JOIN (RIGHT OUTER JOIN)

Returns **all records from the right table**,  
and the **matching records** from the left table.

```sql
SELECT students.full_name, admissions.course_name
FROM students
RIGHT JOIN admissions
ON students.student_id = admissions.student_id;
```

# 7. FULL JOIN (FULL OUTER JOIN)

Returns **all records** when there is a match in either the **left** or **right** table.

```sql
SELECT students.full_name, admissions.course_name
FROM students
FULL JOIN admissions
ON students.student_id = admissions.student_id;

Concept:
Shows every record — matched and unmatched from both tables.

💡 Note: Some SQL databases (like MySQL) don’t support FULL JOIN directly.
You can simulate it using the UNION of LEFT and RIGHT JOINs:

```sql
SELECT * FROM students
LEFT JOIN admissions ON students.student_id = admissions.student_id
UNION
SELECT * FROM students
RIGHT JOIN admissions ON students.student_id = admissions.student_id;
```

## 8. CROSS JOIN

Returns every possible combination of both tables (Cartesian product).

```sql
SELECT students.full_name, courses.course_name
FROM students
CROSS JOIN courses;
```

 Concept:
If there are 5 students and 3 courses, the result will have 15 combinations.

## 9. SELF JOIN

A SELF JOIN is when a table is joined with itself.

 Example:
Find employees and their managers.
```sql
SELECT e.emp_name AS Employee,
       m.emp_name AS Manager
FROM employees e
INNER JOIN employees m
ON e.manager_id = m.emp_id;
```

Concept:
Useful for hierarchical data like organizational structures.

## 10. Combining Multiple Joins

You can join three or more tables together in a single query.
```sql
SELECT s.full_name, c.course_name, a.admission_date
FROM students s
INNER JOIN admissions a ON s.student_id = a.student_id
INNER JOIN courses c ON a.course_id = c.course_id;
```

🧠 Concept:
Combines data from all three — students, admissions, and courses — in one query.

## 11. Practical Use Case: Admission Management System

🎯 Tables:

students → student details

courses → course list

admissions → student-course enrollment

🔍 Query:
Get all student names, courses, and admission dates.

```sql
SELECT s.full_name, c.course_name, a.admission_date
FROM admissions a
JOIN students s ON a.student_id = s.student_id
JOIN courses c ON a.course_id = c.course_id;
```

---
# 🧮 SQL Clauses — WHERE, ORDER BY, GROUP BY, HAVING

SQL Clauses help you **filter, sort, and group** data to get meaningful insights from large datasets.  
They are the building blocks of every query you’ll write as a data analyst or data scientist.

---

## 🧩 1. WHERE Clause — Filtering Data

The **WHERE** clause filters rows based on specified conditions.  
It acts like a **data gatekeeper**, showing only records that match the condition.

### 🧠 Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
### 🎓 Example (Admission_DB)

```sql
SELECT full_name, department, percentage
FROM students
WHERE percentage >= 80;
```

📊 **Result:**

| full_name   | department | percentage |
|--------------|-------------|-------------|
| Riya Sharma  | Science     | 88.5        |
| Aman Verma   | Commerce    | 81.0        |
|

### 🧠 Logical Operators in WHERE

| Operator | Description           | Example                              |
|-----------|----------------------|--------------------------------------|
| =         | Equal to             | `WHERE gender = 'Male'`              |
| != or <>  | Not equal to         | `WHERE department <> 'Arts'`         |
| >         | Greater than         | `WHERE percentage > 90`              |
| <         | Less than            | `WHERE age < 20`                     |
| BETWEEN   | Within a range       | `WHERE percentage BETWEEN 70 AND 90` |
| IN        | Matches any from list| `WHERE department IN ('Science', 'Commerce')` |
| LIKE      | Pattern matching     | `WHERE full_name LIKE 'R%'`          |
| IS NULL   | Checks for null values | `WHERE email IS NULL`              |


### 🧩 Multiple Conditions Example

```sql
SELECT full_name, percentage, department
FROM students
WHERE department = 'Science' AND percentage > 85;
```
📊 **Result:**

| full_name   | percentage | department |
|--------------|-------------|-------------|
| Riya Sharma  | 88.5        | Science     |

## 2. ORDER BY Clause — Sorting Data

The **ORDER BY** clause sorts results in **ascending (ASC)** or **descending (DESC)** order.  
By default, SQL sorts in ascending order.

---

### 🧠 Syntax
```sql
SELECT column1, column2
FROM table_name
ORDER BY column_name [ASC|DESC];

**Example**
```sql
SELECT full_name, percentage
FROM students
ORDER BY percentage DESC;
```
📊 **Result:**

| full_name   | percentage |
|-------------|------------|
| Riya Sharma | 88.5       |
| Aman Verma  | 81.0       |
| Meena Patel | 74.2       |

## Multi-Column Sorting Example

```sql
SELECT full_name, department, percentage
FROM students
ORDER BY department ASC, percentage DESC;
```
📊 **Result:**

| full_name   | percentage |
|-------------|------------|
| Riya Sharma | 88.5       |
| Aman Verma  | 81.0       |
| Meena Patel | 74.2       |

## 3. GROUP BY Clause — Aggregating Data

The **GROUP BY** clause groups rows with the same values in specified columns.  
It is often used with **aggregate functions** such as:

- `COUNT()` — Count the number of rows
- `SUM()` — Sum of values
- `AVG()` — Average of values
- `MIN()` — Minimum value
- `MAX()` — Maximum value

**Syntax**

```sql
SELECT column_name, aggregate_function(column_name)
FROM table_name
GROUP BY column_name;
```
## Example (Admission_DB)
```sql
SELECT department, AVG(percentage) AS avg_percentage
FROM students
GROUP BY department;
```
📊 **Result:**

| department | avg_percentage |
|------------|----------------|
| Science    | 86.2           |
| Commerce   | 79.8           |
| Arts       | 73.4           |


## Multiple Grouping Example
```sql
SELECT department, gender, COUNT(*) AS total_students
FROM students
GROUP BY department, gender;
```

📊 **Result:**

| department | gender | total_students |
|------------|--------|----------------|
| Science    | Female | 20             |
| Science    | Male   | 15             |
| Commerce   | Female | 18             |



## 4. HAVING Clause — Filtering Aggregated Data

The HAVING clause filters data after aggregation.
It’s like a WHERE clause for grouped results.

**Syntax**
```sql
SELECT column_name, aggregate_function(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```
**Example**

```sql
SELECT department, AVG(percentage) AS avg_percentage
FROM students
GROUP BY department
HAVING AVG(percentage) > 80;
```
📊 **Result:**

| department | avg_percentage |
|------------|----------------|
| Science    | 86.2           |
| Commerce   | 81.3           |


## WHERE vs HAVING — Key Difference

| Clause  | Used For                   | Works On                  | Example                           |
|---------|----------------------------|---------------------------|-----------------------------------|
| **WHERE** | Filtering individual rows  | Raw data                  | `WHERE percentage > 80`          |
| **HAVING** | Filtering aggregated groups | Results after `GROUP BY`  | `HAVING AVG(percentage) > 80`   |
### Combined Example — All Clauses Together

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT department, COUNT(*) AS total_students, AVG(percentage) AS avg_score  FROM students  WHERE admission_year = 2025  GROUP BY department  HAVING AVG(percentage) > 75  ORDER BY avg_score DESC;   `

📊 **Result:**

departmenttotal\_studentsavg\_scoreScience3586.2Commerce2880.4

🧠 **Step-by-Step Execution Order:**

1.  **FROM** → Identify the table
    
2.  **WHERE** → Filter raw rows
    
3.  **GROUP BY** → Group remaining rows
    
4.  **HAVING** → Filter grouped data
    
5.  **SELECT** → Display columns or calculations
    
6.  **ORDER BY** → Sort the final output
    

🧠 Real-World Use Cases
-----------------------

ScenarioClause UsedExampleGet all students scoring above 80%WHEREWHERE percentage > 80Sort departments by average marksORDER BYORDER BY AVG(percentage) DESCCount students per departmentGROUP BYGROUP BY departmentShow departments with avg > 75%HAVINGHAVING AVG(percentage) > 75

📚 5. Common Mistakes to Avoid
------------------------------

🚫 Using WHERE with aggregate functions✅ Use HAVING instead.

🚫 Forgetting to include non-aggregated columns in GROUP BY✅ Every column in SELECT that’s not aggregated must appear in GROUP BY.

🚫 Wrong order of clauses✅ Correct order is:SELECT → FROM → WHERE → GROUP BY → HAVING → ORDER BY

---

# 📊 SQL Aggregate Functions — COUNT, SUM, AVG, MIN, MAX

Aggregate functions perform **calculations on multiple rows** of a table and return a **single summarized value**.  
They are most often used with `GROUP BY` to generate summaries such as totals, averages, and counts.

## 🧠 1. Overview of Aggregate Functions

| Function | Description | Example Use |
|-----------|--------------|--------------|
| **COUNT()** | Returns number of rows | Count students |
| **SUM()** | Adds up all values | Total marks or fees |
| **AVG()** | Calculates average value | Average percentage |
| **MIN()** | Finds smallest value | Lowest marks |
| **MAX()** | Finds largest value | Highest marks |

---

## 🎯 2. COUNT() — Count Number of Records

Returns the **number of rows** in a result set that match a condition.

### 🧠 Syntax
```sql
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```
### Example (Admission\_DB)

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT COUNT(*) AS total_students  FROM students;   `

📊 **Result:**

total\_students120

💡 **Tip:**

*   COUNT(\*) counts **all rows**, including NULLs.
    
*   COUNT(column\_name) ignores NULL values.
    

### 🧩 Example — Conditional Count

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT COUNT(*) AS science_students  FROM students  WHERE department = 'Science';   `

📊 **Result:**

science\_students45

➕ 3. SUM() — Add Up Values
--------------------------

Calculates the **total sum** of a numeric column.

### 🧠 Syntax

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT SUM(column_name)  FROM table_name  WHERE condition;   `

### 📘 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT SUM(fees_paid) AS total_revenue  FROM admissions;   `

📊 **Result:**

total\_revenue854000.00

💡 **Use Case:**To find total revenue, total marks, or total expenses.

⚖️ 4. AVG() — Find the Average
------------------------------

Calculates the **average value** of a numeric column.

### 🧠 Syntax

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT AVG(column_name)  FROM table_name;   `

### 📘 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT AVG(percentage) AS avg_score  FROM students  WHERE department = 'Science';   `

📊 **Result:**

avg\_score86.25

💡 **Note:**

*   Ignores NULL values automatically.
    
*   Often combined with GROUP BY.
    

🔽 5. MIN() — Find the Smallest Value
-------------------------------------

Returns the **minimum** value in a column.

### 🧠 Syntax

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT MIN(column_name)  FROM table_name;   `

### 📘 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT MIN(percentage) AS lowest_score  FROM students  WHERE department = 'Commerce';   `

📊 **Result:**

lowest\_score62.4

💡 **Use Case:**Find the lowest salary, smallest order value, or earliest date.

🔼 6. MAX() — Find the Largest Value
------------------------------------

Returns the **maximum** value in a column.

### 🧠 Syntax

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT MAX(column_name)  FROM table_name;   `

### 📘 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT MAX(percentage) AS highest_score  FROM students;   `

📊 **Result:**

highest\_score95.8

💡 **Use Case:**Get top marks, highest salary, or latest date of admission.

🧮 7. Using Aggregate Functions Together
----------------------------------------

You can apply multiple aggregates in one query.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT       COUNT(*) AS total_students,      AVG(percentage) AS avg_marks,      MIN(percentage) AS min_marks,      MAX(percentage) AS max_marks  FROM students  WHERE department = 'Science';   `

📊 **Result:**

total\_studentsavg\_marksmin\_marksmax\_marks4586.2572.495.8

🧩 8. Aggregate Functions with GROUP BY
---------------------------------------

Aggregates combined with GROUP BY summarize data for each group.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT department, COUNT(*) AS total_students, AVG(percentage) AS avg_score  FROM students  GROUP BY department;   `

📊 **Result:**

departmenttotal\_studentsavg\_scoreScience4586.2Commerce3881.4Arts3774.9

💡 **Concept:**Each department is treated as a **group**, and aggregates are calculated per group.

🧮 9. Conditional Aggregates Using CASE
---------------------------------------

Sometimes you need aggregates based on a condition (like conditional COUNT or SUM).

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT       SUM(CASE WHEN gender = 'Male' THEN 1 ELSE 0 END) AS male_students,      SUM(CASE WHEN gender = 'Female' THEN 1 ELSE 0 END) AS female_students  FROM students;   `

📊 **Result:**

male\_studentsfemale\_students5565

💡 **Use Case:**Count specific categories (e.g., number of male vs female students).

🧩 10. Aggregate with DISTINCT
------------------------------

DISTINCT removes duplicates before applying aggregation.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT COUNT(DISTINCT department) AS unique_departments  FROM students;   `

📊 **Result:**

unique\_departments3

💡 **Concept:**Counts only unique values in a column.

⚙️ 11. Aggregate Functions on Dates
-----------------------------------

You can also use aggregates on date columns.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT       MIN(admission_date) AS first_admission,      MAX(admission_date) AS latest_admission  FROM admissions;   `

📊 **Result:**

first\_admissionlatest\_admission2024-01-102025-10-25

💡 **Use Case:**Track time periods — earliest and latest records.

🔍 12. Combining Aggregates and HAVING
--------------------------------------

Use HAVING to filter aggregated results.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   SELECT department, AVG(percentage) AS avg_score  FROM students  GROUP BY department  HAVING AVG(percentage) > 80;   `

📊 **Result:**

departmentavg\_scoreScience86.2Commerce81.3

💡 **Tip:**

*   WHERE filters **before** aggregation
    
*   HAVING filters **after** aggregation
    

🧠 13. Common Mistakes to Avoid
-------------------------------

MistakeProblemFixUsing aggregate in WHERESQL errorUse HAVING insteadMixing aggregated and non-aggregated columnsIncorrect groupingInclude non-aggregated columns in GROUP BYForgetting aliasConfusing resultsUse AS to name output columns

🧭 14. Real-World Use Cases
---------------------------

ScenarioFunctionExampleCount total studentsCOUNT()SELECT COUNT(\*) FROM students;Find total revenueSUM()SELECT SUM(fees\_paid) FROM admissions;Get average marks per departmentAVG()SELECT department, AVG(percentage) FROM students GROUP BY department;Find top and bottom performersMAX() / MIN()SELECT MAX(percentage), MIN(percentage) FROM students;Identify departments with avg > 80HAVINGHAVING AVG(percentage) > 80;

🧮 15. Execution Flow (with Aggregates)
---------------------------------------

1.  **FROM** — Choose the table
    
2.  **WHERE** — Filter rows
    
3.  **GROUP BY** — Group rows
    
4.  **AGGREGATE** — Apply COUNT, SUM, etc.
    
5.  **HAVING** — Filter groups
    
6.  **ORDER BY** — Sort output
    

🧩 Summary — Aggregate Functions Overview
-----------------------------------------

FunctionMeaningCommon UseCOUNT()Number of rowsTotal students, ordersSUM()Total sumTotal fees, salesAVG()Average valueMean marks or priceMIN()MinimumLowest marks or earliest dateMAX()MaximumTop marks or latest date

```
# 🧱 SQL Constraints — PRIMARY KEY, FOREIGN KEY, UNIQUE, CHECK, DEFAULT

SQL **constraints** are rules applied to table columns to maintain **data accuracy, consistency, and integrity**.  
They prevent invalid data from entering the database.

---

## 🎯 What are Constraints?

Constraints are conditions or rules applied to data columns when creating or altering a table.  
They help maintain **reliable and consistent data**.

| Constraint | Description | Example Use |
|-------------|-------------|-------------|
| **PRIMARY KEY** | Uniquely identifies each record | `student_id` in `students` table |
| **FOREIGN KEY** | Links data between tables | `student_id` in `admissions` refers to `students` |
| **UNIQUE** | Ensures all values in a column are unique | `email` column in `students` |
| **CHECK** | Ensures values meet a specific condition | `age >= 18` |
| **DEFAULT** | Provides a default value if none is given | `status = 'Active'` |

---

## 🧩 1. PRIMARY KEY Constraint

- Uniquely identifies each record in a table.
- Automatically enforces **NOT NULL** and **UNIQUE**.
- Each table can have **only one PRIMARY KEY** (single or composite).

### 🧠 Example

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    full_name VARCHAR(100) NOT NULL,
    dob DATE
);
```
### Explanation

*   student\_id uniquely identifies every student.
    
*   Auto-increment ensures each ID is automatically generated.
    

🔗 2. FOREIGN KEY Constraint
----------------------------

*   Establishes a **relationship** between two tables.
    
*   Enforces **referential integrity** — prevents orphan records.
    
*   The foreign key column must match the primary key in the referenced table.
    

### 🧠 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   CREATE TABLE admissions (      admission_id INT PRIMARY KEY AUTO_INCREMENT,      student_id INT,      admission_date DATE,      FOREIGN KEY (student_id) REFERENCES students(student_id)  );   `

### 📘 Explanation

*   student\_id in admissions must exist in students.
    
*   If a student is deleted, their admission record may be restricted (or cascaded).
    

💎 3. UNIQUE Constraint
-----------------------

*   Ensures all values in a column are different.
    
*   Unlike **PRIMARY KEY**, a table can have **multiple UNIQUE** columns.
    

### 🧠 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   CREATE TABLE users (      user_id INT PRIMARY KEY AUTO_INCREMENT,      email VARCHAR(100) UNIQUE,      phone_number VARCHAR(15) UNIQUE  );   `

### 📘 Explanation

*   Prevents duplicate emails or phone numbers.
    
*   Multiple users cannot share the same contact details.
    

⚖️ 4. CHECK Constraint
----------------------

*   Ensures column values satisfy a specific condition.
    
*   Helps enforce **business logic** rules directly in the database.
    

### 🧠 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   CREATE TABLE courses (      course_id INT PRIMARY KEY AUTO_INCREMENT,      course_name VARCHAR(100),      duration_in_months INT CHECK (duration_in_months > 0),      fees DECIMAL(8,2) CHECK (fees >= 1000)  );   `

### 📘 Explanation

*   duration\_in\_months must be greater than 0.
    
*   fees must be at least 1000.
    

⚙️ 5. DEFAULT Constraint
------------------------

*   Assigns a default value when none is specified in INSERT.
    
*   Helps avoid NULL values for common defaults.
    

### 🧠 Example

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   CREATE TABLE employees (      emp_id INT PRIMARY KEY AUTO_INCREMENT,      full_name VARCHAR(100),      department VARCHAR(50) DEFAULT 'General',      is_active BOOLEAN DEFAULT TRUE,      joining_date DATE DEFAULT (CURRENT_DATE)  );   `

### 📘 Explanation

*   If department or is\_active is not provided, default values are inserted.
    
*   Useful for maintaining consistent defaults in large datasets.
    

🧮 Combined Example: Real-World Admission System
------------------------------------------------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   CREATE TABLE students (      student_id INT PRIMARY KEY AUTO_INCREMENT,      full_name VARCHAR(100) NOT NULL,      email VARCHAR(100) UNIQUE,      age INT CHECK (age >= 18)  );  CREATE TABLE admissions (      admission_id INT PRIMARY KEY AUTO_INCREMENT,      student_id INT,      course_name VARCHAR(100),      admission_date DATE DEFAULT (CURRENT_DATE),      FOREIGN KEY (student_id) REFERENCES students(student_id)  );   `

### 🔍 Key Highlights

ConceptExplanation**PRIMARY KEY**student\_id uniquely identifies each student**UNIQUE**email ensures no duplicates**CHECK**age >= 18 enforces admission eligibility**DEFAULT**admission\_date defaults to the current date**FOREIGN KEY**student\_id in admissions links to students

🧭 Key Takeaways
----------------

✅ **PRIMARY KEY** → Uniquely identifies rows✅ **FOREIGN KEY** → Maintains relationships between tables✅ **UNIQUE** → Prevents duplicate values✅ **CHECK** → Validates data conditions✅ **DEFAULT** → Provides fallback values

💡 Best Practices
-----------------

1.  Always define **PRIMARY KEY** in every table.
    
2.  Use **FOREIGN KEYS** to ensure relational consistency.
    
3.  Apply **CHECK** constraints for validation at the database level.
    
4.  Define **DEFAULTS** for optional fields to reduce NULLs.
    
5.  Avoid using too many constraints that could slow down large inserts.
