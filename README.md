# Application Workflow Dashboard (CURRENTLY IN PROGRESS)

A realistic, simulated operational dataset analysing application workflows, data quality issues, payment trends, and processing performance.

This project was built to demonstrate Power BI skills in:
- Data cleaning
- Data modelling
- DAX calculations
- Visual analytics
- Business insights
---
## 📥 Data Source
A synthetic dataset (`to be added`) was created to simulate real-world application workflows with:
- Quarterly fee rules
- Multiple application types
- Payment behaviours (Paid, Pending, Unpaid)
- Outliers and nulls for data quality analysis
- Duplicates for realistic cleaning

Loaded the dataset (CSV format) directly into Power BI and began transformation using Power Query.
---
##  Power Query Data Cleaning

###  Removed Duplicates  
Removed intentionally added duplicate rows to simulate realistic data cleaning.

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
### Fixed Month Sorting Issue  
Power BI raised an error when sorting month names due to multiple SubmissionDate values per month.
Created numerical month columns:
- `SubmissionMonthNumber`
- `PaymentMonthNumber`
Used Sort by Column to sort month names chronologically.
This ensures accurate and professional month-over-month trend visuals.

### DAX Measures Used 
Total Revenue 
- Dax ' Total Rev := SUM('GOC Draft 1'[PaymentAmount])'
Payment Completion Rate
- Dax ' Payment Completion Rate :=
DIVIDE(
    COUNTROWS(FILTER('GOC Draft 1', 'GOC Draft 1'[PaymentStatus] = "Paid")),
    COUNTROWS('GOC Draft 1') ) '

Additional measures such as Average Processing Time and Application Count will be added as the dashboard develops.

These DAX measures allow for dynamic KPI calculations and highlight the ability to convert raw data into meaningful insights.



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




