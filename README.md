# Karnataka-Workforce-Census-Data-Warehouse
A data engineering project focusing on medallion architecture using the free datasets available on kar.data.gov.in , using the datsets related to marginal workers and main workers in different categories and occupation

<img width="1681" height="677" alt="Screenshot 2026-06-27 105400" src="https://github.com/user-attachments/assets/11f4999f-f319-4e15-ad51-1942db6f4b82" />

# Project Overview
## This project builds an end-to-end Data Warehouse using Karnataka workforce census data following the Medallion Architecture approach (Bronze, Silver, Gold).
## The objective is to transform raw census data into analytics-ready fact and dimension tables capable of supporting workforce, occupation, and industrial analysis.

# Architecture
## 1.Bronze Layer
Raw data ingestion into Delta tables.
## 2.Silver Layer
Data cleaning and validation.
Hierarchical metadata enrichment.
Occupational aggregation labeling.
Industrial data standardization.
## 3.Gold Layer
Star schema implementation.
Dimension and fact table creation.
Surrogate key generation.
Workforce analytical modeling.

# Technologies Used
PySpark
Databricks Community Edition
Delta Lake
SQL
Dimensional Modeling
Star Schema Design
# Data Model
Dimensions:
dim_geography
dim_occupation
dim_industrial_occupation
dim_community
dim_worker_type
dim_industry
Facts:
fact_occupation_workforce
fact_industrial_workforce
# Data Quality Checks
Duplicate detection
Null validation
Gender consistency checks
Rural and urban consistency checks
Industrial category validation
Referential integrity validation
# Example Business Questions
Which occupations employ the largest workforce?
Which industries dominate employment in Karnataka?
How does workforce participation vary across districts?
What is the rural versus urban workforce distribution?
How do workforce patterns differ across communities?
# Future Enhancements
Interactive Tableau dashboards
Additional state datasets
Automated ETL orchestration
Incremental loading strategy
