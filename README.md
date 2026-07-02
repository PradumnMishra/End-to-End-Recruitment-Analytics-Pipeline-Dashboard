# 🚀 End-to-End Recruitment Analytics Pipeline & Dashboard

Tech Stack: SQL Server | Python (Pandas, PyODBC) | Power Query (M Language) | Power BI

## 📋 Executive Summary
Developed a centralized analytics solution for a recruitment firm to process and analyze over 700,000 unorganized job postings. Designed a hybrid ETL pipeline integrating MS SQL Server, Python, and Power Query to consolidate fragmented data sources into a highly optimized Power BI dashboard. The final product empowers stakeholders to track global hiring trends, optimize workforce planning, and identify shifting demands in the data industry.
<img width="900" height="508" alt="RecruimentAnalytics" src="https://github.com/user-attachments/assets/b3166386-a9e5-4379-b641-026ecbfd568e" />

## 🛑 The Business Problem
* **Massive & Fragmented Data:** Over 700,000 rows spread across multiple disconnected tables (both normalized and centralized structures).
* **Unstructured Text:** Critical details regarding job types and seniority levels were embedded within lengthy, unstructured text paragraphs.
* **Performance Bottlenecks:** The sheer volume of data threatened to compromise Power BI report speed and responsiveness.
* **Lack of Visibility:** The disorganization made it impossible to identify peak hiring periods, remote vs. on-site trends, and localized        skill demands

## 🏗️ Architecture & ETL Workflow
To solve the data silos and performance issues, I engineered a robust data pipeline:

### 1. Data Extraction & Consolidation
+ **Database Integration:** Connected directly to a local MS SQL Server using Python (pyodbc) and Power BI to extract 4 primary dimension/fact tables (company_dim2, job_postings_fact2, skills_dim2, skills_job_dim2).

Python Merging Pipeline: Wrote a Python script utilizing pandas to handle left joins across massive datasets, successfully merging company, job posting, and skills data. Replaced null values and aggregated grouped skills into a clean, comma-separated string format for easier downstream processing.
