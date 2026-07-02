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

+ **Python Merging Pipeline:** Wrote a Python script utilizing pandas to handle left joins across massive datasets, successfully merging company, job posting, and skills data. Replaced null values and aggregated grouped skills into a clean, comma-separated string format for easier downstream processing.

### 2. Feature Engineering & Transformation (Power Query / M Language)
Wrote custom M Language scripts to extract structured insights from messy text fields:
+ **Job Schedule Categorization:** Built conditional logic to parse summary strings and accurately flag roles as Full-Time, Part-Time, Contract, Freelance, or Internship.
+ **Title Standardization:** Mapped hundreds of varied, inconsistent job titles into standardized parent categories (e.g., standardizing "ml engineer", "deep learning engineer", and "ai engineer" into Machine Learning Engineer).
+ **Seniority Extraction:** Parsed titles for keywords like Lead, Principal, Chief, Director, VP, and Senior to classify roles into distinct hierarchy levels (Associate vs. Mid/Senior Level).

# 📊 Key Insights & Deliverables
** 📈 Peak Hiring Periods:** Identified major seasonal spikes in talent acquisition, noting a significant high of 2,926 job openings in January 2023, helping the client optimize their recruitment timing. 
<img width="436" height="182" alt="image" src="https://github.com/user-attachments/assets/170dc2f2-e59b-4ebe-aa4b-76826b3fb162" />

** 🛠️ In-Demand Skills:** Visualized market requirements through a dynamic word cloud, revealing that SQL, Python, Excel, Tableau, and Cloud Engineering (AWS/Azure) dominate employer demands. 
<img width="1095" height="484" alt="image" src="https://github.com/user-attachments/assets/e7c9dae5-c7b7-4f8a-a789-4ffec9ba8831" />

** 🏢 Top Job Domains:** Tracked shifting market demands over three years. Found that while "Data Engineer" and "Data Analyst" remained top roles across 2022-2024, demand for "Senior Data Engineer" surged to the #1 spot in 2024.
<img width="364" height="131" alt="image" src="https://github.com/user-attachments/assets/2421710a-2d8f-4844-b3a3-47c6447fade2" />

 ** 🌍 Evolving Work Structures:** Analyzed the distribution of hybrid, onsite, and remote roles to track post-pandemic employment trends globally.    
<img width="437" height="141" alt="image" src="https://github.com/user-attachments/assets/bda52f0c-f6a1-4ee6-93a2-73ad660a006b" />
