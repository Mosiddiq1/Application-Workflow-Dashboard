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
## Application Breakdown Page

This page explores application behaviour across different categories and reveals operational patterns that are not visible in the KPI view.
- Key Visuals Included
        Applications by ApplicationType:
        Shows distribution across Student, Fully Qualified, Body Corporate, and Restoration applications.
        Highlights which workflows contribute most to overall volume.
Average DaysToProcess by ApplicationType:
  Identifies which application categories take longer to process, helping reveal operational bottlenecks.
    
ApplicationType by ApplicantType (UK vs International):
Compares the profile of applications across regions.
Useful for understanding differences in behaviour between UK and international applicants.

ApplicationType Slicer:
    - Allows users to filter the entire page by application category for deeper, interactive exploration.
    
## Key DAX Measures

Several DAX measures were created to support KPI reporting and financial analysis, including:

- **Total Collected Revenue (Paid-only):** Ensures revenue reflects completed payments only.
- **Payment Completion Rate:** Measures the proportion of applications with successful payments.
- **Outstanding Count:** Identifies applications requiring follow-up due to Pending or Unpaid status.
- **Average Days to Process:** Highlights processing efficiency across applicant types.

These measures enable reusable, consistent logic across all report pages.

## Payment Insights

This page focuses on understanding payment behaviour, revenue collection, and outstanding applications.

Key elements include:
- **Collected Revenue (Paid-only):** Revenue calculations explicitly exclude Pending and Unpaid records to reflect actual cash received.
- **Outstanding Count:** Counts applications with Pending or Unpaid statuses to highlight financial backlog.
- **Payment Status Breakdown:** Visualises the proportion of Paid vs Outstanding applications.
- **Revenue by Application Type:** Identifies which application categories contribute most to total revenue.
- **Year-over-Year Revenue Trend (2024 vs 2025):**  
  A multi-line time series compares monthly collected revenue across years, highlighting seasonal patterns and periods of delayed payment activity.

This analysis supports operational decision-making by distinguishing between application volume and realised revenue.

---

## Insights Summary

Key insights from the dashboard include:
- A clear gap between application volume and collected revenue, emphasising the importance of payment completion tracking.
- Certain application types contribute disproportionately to total revenue despite lower volumes.
- Outstanding applications remain a measurable operational risk, particularly during specific periods.
- Revenue trends show seasonal variation and differences in payment timing between 2024 and 2025.

This project demonstrates the ability to translate raw operational data into actionable business insights using Power BI.

---
## Repository Structure
---
## Author
Created by Mosiddiq (Omar Siddiq)  
Demonstrating Power BI skills through realistic analytics.




