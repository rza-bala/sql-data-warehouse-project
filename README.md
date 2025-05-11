# 🏗️ SQL Data Warehouse Project

This project implements a modular **SQL Data Warehouse** using a layered architecture: **Bronze → Silver → Gold**. It consolidates ERP and CRM datasets into a PostgreSQL-based warehouse to support scalable analytics, reporting, and data quality validation.

---

## 🧠 Project Goals

- Load ERP and CRM source data into a PostgreSQL database
- Implement a **three-tier data warehouse architecture**
- Perform data cleansing, transformation, and integration
- Provide business-ready tables for analytics use cases
- Ensure data quality with automated SQL checks

---

## 🛠️ Technologies Used

| Tool/Tech     | Purpose                            |
|---------------|------------------------------------|
| PostgreSQL    | Relational database platform       |
| SQL (DDL/DML) | Schema creation and ETL processing |
| pgAdmin       | Optional GUI for PostgreSQL        |
| CSV Files     | Source datasets                    |
| Bash/psql     | Running SQL scripts                |

---

## 📁 Data Sources

| File Name                     | Description                   |
|------------------------------|-------------------------------|
| `cust_info.csv`              | CRM customer profiles         |
| `prd_info.csv`               | CRM product details           |
| `sales_details.csv`          | CRM sales transactions        |
| `CUST_AZ12.csv`              | ERP customer reference data   |
| `LOC_A101.csv`               | ERP location metadata         |
| `PX_CAT_G1V2.csv`            | ERP product category mappings |

---

## 📊 Data Warehouse Layers

### 🔹 Bronze Layer (Raw)
- Ingests data directly from CSV files
- Maintains raw structure for traceability

### 🔸 Silver Layer (Cleansed)
- Applies cleaning, joining, and transformation logic
- Produces structured and consistent data models

### 🟡 Gold Layer (Business)
- Final tables for reporting and dashboards
- Includes derived fields, KPIs, and dimensional models

---

## 🚀 How to Run

> **Note**: Replace `your_user` and `your_db` with your actual PostgreSQL username and database name.

### 1. Initialize Database

```bash
psql -U your_user -f scripts/init_database.sql

