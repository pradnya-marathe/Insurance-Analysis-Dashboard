# Insurance Analysis Dashboard

## Project Summary
The Insurance Analysis Dashboard delivers an end-to-end analytical view of insurance operations using Power BI.  
It focuses on evaluating premium collection, claim performance, policy coverage, and customer demographics to uncover risk patterns and operational trends.  
The dashboard is designed for business analysts, underwriting teams, and claims operations to support data-driven decision-making.

## Project Goals
- Track overall insurance performance through premium, claim, and coverage metrics  
- Analyze claim trends based on age groups, policy categories, and claim outcomes  
- Enable fast record-level lookup using policy, customer, and claim identifiers  
- Assist underwriting and risk assessment through historical claim behavior analysis  

## Author
Pradnya Marathe

## Data Source
Table Name: InsuranceData

### Key Fields
- Policy Information: PolicyNumber, PolicyType, PolicyStartDate, PolicyEndDate  
- Customer Attributes: CustomerID, Age, AgeGroup, Gender  
- Financial Metrics: PremiumAmount, ClaimAmount, CoverageAmount  
- Claim Details: ClaimNumber, ClaimDate, ClaimStatus  
- Policy Status: Active / Inactive  

## Data Preparation and Modeling
- Standardized policy and customer identifiers  
- Converted date columns to appropriate date formats  
- Validated numeric fields for premiums, claims, and coverage amounts  
- Created age group categories for demographic analysis  
- Derived policy activity status using policy end dates  
- Built a date dimension table for time-based analysis  
- Aggregated metrics by policy type, age group, and claim status  

## Key Business Metrics (DAX Measures)
```DAX
Total Premium Amount = SUM(InsuranceData[PremiumAmount])

Total Claim Amount = SUM(InsuranceData[ClaimAmount])

Total Coverage Amount = SUM(InsuranceData[CoverageAmount])

Active Policy Count =
CALCULATE(
    DISTINCTCOUNT(InsuranceData[PolicyNumber]),
    InsuranceData[Active/Inactive] = "Active"
)

Total Claims =
COUNT(InsuranceData[ClaimNumber])

Average Claim Value =
AVERAGE(InsuranceData[ClaimAmount])

Claim to Premium Ratio =
DIVIDE([Total Claim Amount], [Total Premium Amount], 0)
