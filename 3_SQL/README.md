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

---

## 🚀 Coming Next

➡️ **Data Types in SQL** — Learn about the different types of data (numbers, text, dates) and how to choose the right one for your tables.

---

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

## 🧑‍💻 2. Character (String) Data Types

These store **text, names, addresses, and descriptions.**

| Data Type | Storage | Description | Example (Admission_DB) |
|------------|----------|-------------|--------------------------|
| CHAR(n) | Fixed length | Always stores exactly `n` characters | gender CHAR(6) (‘Male’, ‘Female’) |
| VARCHAR(n) | Variable length | Stores only required characters | student_name VARCHAR(100) |
| TEXT | Up to 65,535 chars | Long text like feedback or notes | remarks TEXT |

### 🧠 Example
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

### 🧠 Example
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

### 🧠 Example
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

### 🧠 Example
```sql
CREATE TABLE documents (
    doc_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    certificate BLOB
);
```

# 🔐 SQL Constraints and Keys — Complete Guide

Constraints are rules applied to columns to **maintain data integrity** and ensure valid, consistent data is stored in the database.

---

##  1. What Are Constraints?

Constraints restrict the type of data that can go into a table column.  
They help prevent invalid data entry (like negative age or duplicate emails).

💡 **Example:**  
You can prevent duplicate student emails using a `UNIQUE` constraint,  
or stop empty name fields using a `NOT NULL` constraint.

---

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

---

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
🧭 11. Quick Summary
Constraint	Purpose	Example
NOT NULL	Prevent empt

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
