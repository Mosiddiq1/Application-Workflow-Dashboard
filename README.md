# Application Workflow Dashboard

A realistic, simulated operational dataset analysing application workflows, data quality issues, payment trends, and processing performance.

This project was built to demonstrate Power BI skills in:
- Data cleaning
- Data modelling
- DAX calculations
- Visual analytics
- Business insights
---
## 📥 Data Source
A synthetic dataset (`application_processing_dataset_v4.csv`) was created to simulate real-world application workflows with:
- Quarterly fee rules
- Multiple application types
- Payment behaviours (Paid, Pending, Unpaid)
- Outliers and nulls for data quality analysis
- Duplicates for realistic cleaning

Loaded the dataset (CSV format) directly into Power BI and began transformation using Power Query.
---
##  Power Query Data Cleaning

###  Removed Duplicates  
Removed intentionally injected duplicate rows to simulate real-world data cleaning.

###  Standardised Data Types  
Ensured all key columns use appropriate types:
- **SubmissionDate** & **PaymentDate** → Date  
- **Age** & **DaysToProcess** → Whole Number  
- **PaymentAmount** → Decimal Number  
- All categorical fields → Text  

This prevents calculation errors and supports accurate measures in Power BI/DAX.

###  Handled Null Values  
Filtered rows where necessary (e.g., Age, PaymentAmount) while intentionally **keeping nulls** in certain fields for the Data Quality Insights page.

### Preserved Outliers  
Kept intentionally injected outliers to showcase anomaly detection:
- Ages below 18 or above 75  
- Extreme PaymentAmount values (e.g., 9999, 15000)

### Added Date Intelligence Fields  
Created additional columns to support monthly and yearly trend analysis:
- `SubmissionMonth`
- `PaymentMonth`
- `SubmissionYear`
- `PaymentYear`
---
## Power BI Pages (To Be Added)
This dashboard contains multiple report pages:

1. **KPI Overview**
2. **Application Breakdown**
3. **Payment Insights**
4. **Data Quality Insights**
5. **Trend Analysis**
(Screenshots will be added after dashboard completion.)
---
## Key DAX Measures (To Be Added)
- Payment Completion Rate  
- Total Revenue  
- Average DaysToProcess  
- Applications Count  
---
## Insights Summary (To Be Added)
A brief summary of findings will be added after dashboard construction.
---
## Repository Structure
---
## Author
Created by Mosiddiq (Omar Siddiq)  
Demonstrating Power BI skills through realistic analytics.




