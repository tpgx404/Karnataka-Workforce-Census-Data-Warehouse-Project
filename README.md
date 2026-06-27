# Karnataka Workforce Census Data Warehouse

A Data Engineering project that implements the **Medallion Architecture (Bronze → Silver → Gold)** using publicly available Karnataka workforce census datasets from **kar.data.gov.in**. The project transforms raw census data related to **main workers**, **marginal workers**, occupations, industries, and communities into an analytics-ready data warehouse.

<img width="1681" height="677" alt="Screenshot 2026-06-27 105400" src="https://github.com/user-attachments/assets/11f4999f-f319-4e15-ad51-1942db6f4b82" />
---

## Project Overview

This project builds an **end-to-end Data Warehouse** using Karnataka Workforce Census data by implementing the **Medallion Architecture**.

The primary objective is to transform raw census datasets into clean, standardized, and analytics-ready dimensional models that support workforce analysis across:

- Occupations
- Industries
- Geography
- Communities
- Worker categories

The final Gold layer follows a **Star Schema** design suitable for Business Intelligence and reporting.

---

# Architecture

## 🥉 Bronze Layer

- Raw data ingestion
- Delta Lake storage
- Schema preservation
- Source-level data storage

---

## 🥈 Silver Layer

- Data cleaning
- Null handling
- Duplicate removal
- Data validation
- Hierarchical metadata enrichment
- Occupational aggregation labeling
- Industrial data standardization

---

## 🥇 Gold Layer

- Star Schema implementation
- Dimension table creation
- Fact table creation
- Surrogate key generation
- Analytics-ready data model

---

# Technologies Used

- PySpark
- Databricks Community Edition
- Delta Lake
- SQL
- Dimensional Modeling
- Star Schema Design

---

# Data Model

## Dimension Tables

- `dim_geography`
- `dim_occupation`
- `dim_industrial_occupation`
- `dim_community`
- `dim_worker_type`
- `dim_industry`

## Fact Tables

- `fact_occupation_workforce`
- `fact_industrial_workforce`

---

# Data Quality Checks

The following quality validations are performed during the Silver Layer transformation:

- Duplicate detection
- Null validation
- Gender consistency checks
- Rural vs Urban consistency validation
- Industrial category validation
- Referential integrity validation

---

# Example Business Questions

This warehouse can answer questions such as:

- Which occupations employ the largest workforce?
- Which industries contribute the most employment in Karnataka?
- How does workforce participation vary across districts?
- What is the rural versus urban workforce distribution?
- How do workforce patterns differ across communities?
- Which worker categories dominate different industries?

---

# Project Workflow

```text
Raw Census Data
        │
        ▼
 Bronze Layer
 (Raw Delta Tables)
        │
        ▼
 Silver Layer
(Data Cleaning & Validation)
        │
        ▼
 Gold Layer
(Star Schema)
        │
        ▼
Analytics / BI Dashboards
```

---

# Future Enhancements

- Interactive Tableau dashboards
- Power BI integration
- Automated ETL orchestration
- Incremental loading strategy
- CI/CD pipeline for deployment
- Data quality monitoring framework

---

# Dataset Source

The project uses publicly available Karnataka Government datasets from:

**https://karnataka.data.gov.in/**

---

# Author

**Karnataka Workforce Census Data Warehouse**

A Data Engineering project demonstrating:

- Medallion Architecture
- Delta Lake
- PySpark ETL
- Data Warehousing
- Star Schema Modeling
- Data Quality Framework
