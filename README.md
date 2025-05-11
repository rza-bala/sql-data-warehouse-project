# 🏗️ SQL Data Warehouse Project

This project implements a modular **SQL Data Warehouse** using a layered architecture: **Bronze → Silver → Gold**. It consolidates ERP and CRM datasets into a PostgreSQL-based warehouse to support scalable analytics, reporting, and data quality validation.

---

## 📦 Project Structure
data-warehouse-project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── etl.drawio                      # Draw.io file shows all different techniquies and methods of ETL
│   ├── data_architecture.drawio        # Draw.io file shows the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow.drawio                # Draw.io file for the data flow diagram
│   ├── data_models.drawio              # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
├── .gitignore                          # Files and directories to be ignored by Git
└── requirements.txt                    # Dependencies and requirements for the project
```

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

