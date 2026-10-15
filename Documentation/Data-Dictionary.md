# Global Banking Analytics — Data Dictionary

## Dataset Overview
This dataset is used for Power BI analysis of banking customers, accounts, loans, transactions, credit quality, branches, and customer risk across 2024–2026.

## Core Fields

| Field | Description | Analysis |
|---|---|---|
| Customer_ID | Unique customer identifier | Customer counts |
| Bank_Name | Bank associated with the record | Bank comparison |
| Branch_ID | Branch identifier | Branch analysis |
| State | State associated with the record | Geographic analysis |
| City | City associated with the record | Geographic analysis |
| Customer_Segment | Customer segment | Segment analysis |
| Customer_Status | Customer lifecycle/status | Customer status |
| Account_Type | Bank account type | Account distribution |
| Transaction_Date | Transaction date | Time analysis |
| Transaction_Type | Transaction category | Transaction analysis |
| Transaction_Channel | Transaction channel | Channel analysis |
| Loan_Type | Loan category | Lending analysis |
| Loan_Status | Loan status | Loan analysis |
| Risk_Category | Customer risk category | Risk analysis |

## Numeric Fields

| Field | Description | Main Measure |
|---|---|---|
| Age | Customer age | Average Age |
| Credit_Score | Customer credit score | Average Credit Score |
| Account_Balance | Account balance | Total Balance |
| Loan_Amount | Loan amount | Total Loan Amount |
| Transaction_Amount | Transaction amount | Transaction Value |
| Digital_Usage_Score | Digital banking usage score | Digital engagement |

## Main Categories

**Customer Segment:** Mass Market, Affluent, Small Business, High Net Worth

**Customer Status:** Active, Dormant, At Risk, Closed

**Risk Category:** Low, Medium, High, Critical

**Loan Status:** No Loan, Active, Paid, Delayed, Defaulted

## Data Preparation Notes
- Set `Transaction_Date` to Date.
- Keep `Customer_ID` and `Transaction_ID` as identifiers.
- Keep monetary columns numeric.
- Use `DISTINCTCOUNT(Customer_ID)` for customer KPIs.
- Use `DISTINCTCOUNT(Transaction_ID)` for transaction counts.
- Review blanks and duplicate identifiers before analysis.
- Treat `No Loan` as a valid loan status, not as a missing customer.
