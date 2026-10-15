# Global Banking Analytics — Dashboard Documentation

## Project Objective
Transform banking records into an interactive Power BI report that answers three questions:

1. How is the banking portfolio performing?
2. Who are the customers and what is their risk profile?
3. How are customers borrowing and transacting?

# Dashboard 1 — Executive Overview

## Purpose
Provide a high-level view of customer scale, financial position, lending, transaction activity, and credit quality.

## KPI Cards
- Total Customers
- Total Balance
- Total Loan Amount
- Transaction Value
- Average Credit Score

## Main Visuals
1. **Transaction Trend** — Line chart showing transaction value over time.
2. **Customers by Bank** — Column chart comparing customer counts across banks.
3. **Customer Segment** — Donut chart showing segment composition.
4. **Account Type** — Horizontal bar chart showing customers by account type.
5. **Bank Performance Summary** — Matrix comparing customers, balance, loans, transaction value, and credit score.

## Business Use
This page is designed for executives and managers who need a quick overview of banking performance before moving into detailed analysis.

# Dashboard 2 — Customer & Risk Analysis

## Purpose
Analyze customer demographics, credit quality, customer status, and risk exposure.

## KPI Cards
- Total Customers
- Average Age
- Average Credit Score
- At Risk Customers
- High + Critical Risk

## Main Visuals
1. **Customers by Risk Category** — Column chart.
2. **Customer Status Distribution** — Donut chart.
3. **Risk by Bank** — 100% stacked bar chart.
4. **Segment vs Risk** — 100% stacked bar chart.

## Risk Color Standard

| Risk | Color |
|---|---|
| Low | Teal |
| Medium | Blue |
| High | Orange |
| Critical | Red |

Keep the order **Low → Medium → High → Critical** consistently.

## Business Use
This page helps identify customer risk concentration, compare banks, and understand how risk differs across customer segments.

# Dashboard 3 — Loans & Transaction Analytics

## Purpose
Analyze lending and transaction behavior in greater detail.

## Recommended KPIs
- Total Branches
- Total Customers
- Total Balance
- Total Loan Amount
- Transaction Value

## Main Visuals
- Monthly Transaction Value Trend
- Loan Status Distribution
- Loan Amount by Loan Type
- Transaction Value by Transaction Type
- Transaction Value by Channel
- Top 10 Branches by Transaction Value
- Transaction Heatmap
- Branch Performance Summary

## Slicers
Use compact dropdown slicers for relevant dimensions such as Bank, Customer Segment, Customer Status, Risk Category, Branch, Account Type, Loan Status, and Transaction Date.

## Interaction
Selections should cross-filter relevant KPIs and visuals. Use Power BI Edit Interactions where necessary.

## Formatting
Financial values should use currency and millions where appropriate, e.g. `$203.10M`. Counts should use whole numbers. Average Age and Average Credit Score should use one decimal place.
