# Data Migration Validation & Reconciliation

## 📌 Project Overview

This project is a Python-based **Data Migration Validation and Reconciliation framework** designed to compare data between a source/old table and a target/new table stored in MySQL.

The solution uses **Python, Pandas, SQLAlchemy, and PyMySQL** to validate whether migrated data is complete, accurate, and consistent.

The framework performs:

- Schema validation
- Column comparison
- Row-count validation
- Missing record detection
- Extra record detection
- Business-key validation
- Source-to-target record matching
- Column-level data comparison
- Data mismatch identification
- Migration reconciliation

---

## 🎯 Business Problem

During a database migration, data can be:

- Missing from the target system
- Added unexpectedly to the target system
- Modified incorrectly
- Stored with different column structures
- Changed during transformation

Manual validation of large datasets can be time-consuming and error-prone.

This project automates the validation process and provides a reliable way to determine whether the source and target datasets are consistent.

---

## 🎯 Project Objectives

1. Validate source and target table structures.
2. Compare source and target columns.
3. Validate source and target record counts.
4. Identify missing records.
5. Identify extra records.
6. Validate the business key.
7. Match source and target records.
8. Compare common columns.
9. Identify data-level mismatches.
10. Generate a final migration validation status.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data validation and automation |
| Pandas | Data extraction and comparison |
| SQLAlchemy | Database connectivity |
| PyMySQL | MySQL database driver |
| MySQL | Source and target database |
| OpenPyXL | Optional Excel report generation |
| Jupyter Notebook | Development and analysis |

---

## 🏗️ Project Architecture

```text
             MySQL Database
                   |
          -------------------
          |                 |
     Source Table       Target Table
          |                 |
          ------- Python ---
                   |
                Pandas
                   |
        ---------------------
        |        |          |
      Schema   Records    Columns
     Check     Check      Check
        |        |          |
        ---------------------
                   |
          Reconciliation Report
                   |
             PASS / FAIL
