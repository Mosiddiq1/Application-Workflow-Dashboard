# Application Workflow Dashboard (Power BI Portfolio Project)

A realistic Power BI portfolio project analysing application workflows, data quality issues, payment behaviour, and processing performance using a synthetic dataset.

This project demonstrates end-to-end Power BI development, from data cleaning to business insights.

---

## 🔧 Skills Demonstrated

- Power Query data cleaning & transformation  
- Data modelling & date intelligence  
- DAX measures for KPIs and financial analysis  
- Multi-page dashboard design  
- Translating operational data into business insights  

---

## 📥 Data Source 

A synthetic dataset (`https://1drv.ms/x/c/e50c82921dec91fb/IQBY-lVMyiOES7dIu6PkYKWnAV9OqgZ207kk3e-QLDPSgz8?e=HGPX1t `) was created to simulate a real-world application processing workflow, including:

- Multiple application types (e.g. Student, Fully Qualified, Restoration)
- Quarterly fee variations
- Payment statuses (Paid, Pending, Unpaid)
- Intentional duplicates, nulls, and outliers for data quality analysis

The dataset is safe, generic, and suitable for portfolio use.

---

## 🧹 Power Query Data Cleaning

### Removed Duplicates
Removed intentionally injected duplicate rows to simulate real-world data cleaning scenarios.

### Standardised Data Types
Key columns were aligned to appropriate data types:
- **SubmissionDate & PaymentDate** → Date  
- **Age & DaysToProcess** → Whole Number  
- **PaymentAmount** → Decimal Number  
- Categorical fields → Text  

This ensures accurate calculations and stable DAX measures.

### Handled Null Values
Null values were selectively retained in specific fields to support data quality analysis, while essential fields were filtered where required.

### Preserved Outliers
Intentional outliers were kept to demonstrate anomaly detection:
- Ages below 18 or above 75  
- Extreme payment values (e.g. 9,999; 15,000)

### Date Intelligence
Additional columns were created to support trend analysis:
- SubmissionMonth / SubmissionYear  
- PaymentMonth / PaymentYear  
- Month number columns to enable correct chronological sorting  

---

## 📐 Key DAX Measures

Custom DAX measures were created to support KPI reporting and analysis, including:

- **Total Collected Revenue (Paid-only)**  
- **Payment Completion Rate**  
- **Outstanding Count (Pending + Unpaid)**  
- **Average Days to Process**

These measures ensure consistent, reusable logic across report pages.

---

## 📊 Power BI Report Pages

### KPI Overview
High-level operational snapshot including application volume, processing speed, payment completion rate, and revenue.

### Application Breakdown
Analysis of application volume and processing performance by applicant type, application type, and country.

### Payment Insights
Focused analysis of revenue and payment behaviour:
- Paid vs Outstanding applications
- Revenue by applicant and application type
- Year-over-year revenue trends (2024 vs 2025)

### Data Quality Insights
Highlights missing information, failed checks, and outliers to demonstrate data quality monitoring.

---

## 🔍 Insights Summary

Key insights from the dashboard include:
- A measurable gap between application volume and collected revenue, emphasising the importance of payment completion tracking.
- Certain application types contribute disproportionately to total revenue despite lower volumes.
- Outstanding applications represent a clear operational and financial backlog.
- Revenue trends vary by year and month, reflecting realistic payment timing behaviour.

This project demonstrates the ability to convert raw operational data into actionable insights using Power BI.

---

## 📁 Repository Structure

- `/data` – Synthetic dataset (CSV)  
- `/powerbi` – ![image alt](https://github.com/Mosiddiq1/Application-Workflow-Dashboard/blob/54048d525da7e47c2265712a769a3470d2e80358/Application%20Breakdown%20.png)
- ![image alt](
- `README.md` – Project documentation  

---

## 👤 Author

Created by **Omar Siddiq**  
Power BI portfolio project showcasing realistic operational analytics.
