# Global Banking Analytics — DAX Measures

## 1. Customer KPIs

### Total Customers
```DAX
Total Customers =
DISTINCTCOUNT(Banking[Customer_ID])
```

### Average Age
```DAX
Average Age =
AVERAGE(Banking[Age])
```

### Average Credit Score
```DAX
Average Credit Score =
AVERAGE(Banking[Credit_Score])
```

## 2. Financial KPIs

### Total Balance
```DAX
Total Balance =
SUM(Banking[Account_Balance])
```

### Total Loan Amount
```DAX
Total Loan Amount =
SUM(Banking[Loan_Amount])
```

### Transaction Value
```DAX
Transaction Value =
SUM(Banking[Transaction_Amount])
```

## 3. Risk KPIs

### At Risk Customers
```DAX
At Risk Customers =
CALCULATE(
    [Total Customers],
    Banking[Customer_Status] = "At Risk"
)
```

### High + Critical Risk
```DAX
High Critical Risk =
CALCULATE(
    [Total Customers],
    Banking[Risk_Category] IN {"High", "Critical"}
)
```

### High Risk Customers
```DAX
High Risk Customers =
CALCULATE(
    [Total Customers],
    Banking[Risk_Category] = "High"
)
```

### Critical Risk Customers
```DAX
Critical Risk Customers =
CALCULATE(
    [Total Customers],
    Banking[Risk_Category] = "Critical"
)
```

### Low Risk Customers
```DAX
Low Risk Customers =
CALCULATE(
    [Total Customers],
    Banking[Risk_Category] = "Low"
)
```

### Medium Risk Customers
```DAX
Medium Risk Customers =
CALCULATE(
    [Total Customers],
    Banking[Risk_Category] = "Medium"
)
```

## 4. Customer Status

### Active Customers
```DAX
Active Customers =
CALCULATE(
    [Total Customers],
    Banking[Customer_Status] = "Active"
)
```

### Dormant Customers
```DAX
Dormant Customers =
CALCULATE(
    [Total Customers],
    Banking[Customer_Status] = "Dormant"
)
```

### Closed Customers
```DAX
Closed Customers =
CALCULATE(
    [Total Customers],
    Banking[Customer_Status] = "Closed"
)
```

## 5. Branch & Transaction Analysis

### Total Branches
```DAX
Total Branches =
DISTINCTCOUNT(Banking[Branch_ID])
```

### Transaction Count
```DAX
Transaction Count =
DISTINCTCOUNT(Banking[Transaction_ID])
```

### Average Transaction Value
```DAX
Average Transaction Value =
AVERAGE(Banking[Transaction_Amount])
```

## 6. Loan Analysis

### Customers with Loans
```DAX
Customers with Loans =
CALCULATE(
    [Total Customers],
    Banking[Loan_Status] <> "No Loan"
)
```

### Active Loans
```DAX
Active Loans =
CALCULATE(
    COUNTROWS(Banking),
    Banking[Loan_Status] = "Active"
)
```

### Defaulted Loans
```DAX
Defaulted Loans =
CALCULATE(
    COUNTROWS(Banking),
    Banking[Loan_Status] = "Defaulted"
)
```

### Delayed Loans
```DAX
Delayed Loans =
CALCULATE(
    COUNTROWS(Banking),
    Banking[Loan_Status] = "Delayed"
)
```

## 7. Risk Percentage Measures

### At Risk %
```DAX
At Risk % =
DIVIDE(
    [At Risk Customers],
    [Total Customers],
    0
)
```

### High + Critical Risk %
```DAX
High Critical Risk % =
DIVIDE(
    [High Critical Risk],
    [Total Customers],
    0
)
```

### Critical Risk %
```DAX
Critical Risk % =
DIVIDE(
    [Critical Risk Customers],
    [Total Customers],
    0
)
```

## 8. Useful Comparison Measures

### Average Balance per Customer
```DAX
Average Balance per Customer =
DIVIDE(
    [Total Balance],
    [Total Customers],
    0
)
```

### Average Loan per Customer
```DAX
Average Loan per Customer =
DIVIDE(
    [Total Loan Amount],
    [Total Customers],
    0
)
```

### Transaction Value per Customer
```DAX
Transaction Value per Customer =
DIVIDE(
    [Transaction Value],
    [Total Customers],
    0
)
```

## 9. Recommended Formatting

| Measure | Format |
|---|---|
| Total Customers | Whole Number |
| Total Branches | Whole Number |
| Transaction Count | Whole Number |
| Average Age | 1 Decimal |
| Average Credit Score | 1 Decimal |
| Total Balance | $#,##0.00M |
| Total Loan Amount | $#,##0.00M |
| Transaction Value | $#,##0.00M |
| Average Transaction Value | Currency |
| At Risk % | Percentage, 1 Decimal |
| High Critical Risk % | Percentage, 1 Decimal |
| Critical Risk % | Percentage, 1 Decimal |

> Replace `Banking` with the exact name of your Power BI table if your table has a different name.

## 10. Measure Organization

For a clean Power BI model, create a dedicated table named:

`_Measures`

Store all measures in this table rather than leaving measures scattered across the source table.

Recommended display folders:

- Customer KPIs
- Financial KPIs
- Risk KPIs
- Customer Status
- Transaction Analysis
- Loan Analysis
- Percentage Measures
- Comparison Measures
