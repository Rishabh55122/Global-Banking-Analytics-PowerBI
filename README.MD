# 🏦 Global Banking Analytics

### Power BI Dashboard | Customer, Financial & Risk Analysis

> **Transforming banking data into interactive insights for better business understanding and decision-making.**

---

## 📊 Project Overview

**Global Banking Analytics** is an interactive **Power BI business intelligence project** built to analyze customer profiles, financial performance, banking activity, and customer risk across **Commonwealth Bank of Australia, JPMorgan Chase, and State Bank of India**.

The project uses banking data covering **2024–2026** and transforms raw records into two focused analytical dashboards. The first dashboard provides an **Executive Overview** of the overall banking portfolio, while the second focuses on **Customer & Risk Analysis** to identify customer distribution, risk exposure, and differences across banks and customer segments.

The goal of this project is not only to visualize data, but to make complex banking information easier to **explore, compare, and interpret** through interactive KPIs, charts, tables, and slicers.

---

## 🎯 Project Objectives

- Analyze overall banking performance
- Understand customer distribution across banks
- Analyze customer segments and account types
- Track transaction activity over time
- Monitor customer credit quality
- Identify At-Risk customers
- Analyze High and Critical risk customers
- Compare risk exposure across banks
- Understand risk distribution across customer segments
- Build an interactive and presentation-ready Power BI report

---

## 🗂️ Dataset Overview

The dataset contains information related to:

| Category | Information |
|---|---|
| 👥 Customers | Customer identifiers and demographics |
| 🏦 Banks | Bank-level customer information |
| 🏢 Branches | Branch-level information |
| 💳 Accounts | Account types and balances |
| 💰 Loans | Loan amounts, types and statuses |
| 💸 Transactions | Transaction dates, amounts and types |
| 📈 Credit | Customer credit scores |
| 🎯 Segments | Customer segment classifications |
| ⚠️ Risk | Customer risk categories |
| 🔄 Status | Customer lifecycle/status |

### Key Dataset Characteristics

- **700 customers**
- **3 banks**
- **193 branches**
- **8 account types**
- **7 loan types**
- Data period: **2024–2026**

---

# 📌 Dashboard 1 — Executive Overview

### Purpose

The **Executive Overview** provides a high-level snapshot of the banking portfolio and allows users to quickly understand customer scale, financial position, lending activity, transaction value, and credit quality.

### Key KPIs

| KPI | Value |
|---|---:|
| Total Customers | **700** |
| Total Balance | **$203.1M** |
| Total Loan Amount | **$147.8M** |
| Transaction Value | **$21.1M** |
| Average Credit Score | **694.9** |

### Visualizations

**📈 Transaction Trend**  
Shows transaction activity across the available years and helps identify changes in transaction value over time.

**🏦 Customers by Bank**  
Compares the number of customers associated with each bank.

**👥 Customer Segment**  
Shows the composition of the customer base across Mass Market, Affluent, Small Business, and High Net Worth segments.

**💳 Account Type**  
Highlights the most common account types based on customer distribution.

**📋 Bank Performance Summary**  
Provides a detailed comparison of customers, balances, loan amounts, and average credit scores across the three banks.

### Business Questions Answered

- How large is the customer base?
- What is the total banking balance?
- How much has been loaned?
- What is the overall transaction value?
- Which bank has the most customers?
- Which customer segment is largest?
- Which account types are most common?
- How does financial performance differ across banks?

---

# 🔎 Dashboard 2 — Customer & Risk Analysis

### Purpose

The **Customer & Risk Analysis** dashboard focuses on customer demographics, customer status, credit quality, and risk exposure.

### Key KPIs

| KPI | Value |
|---|---:|
| Total Customers | **700** |
| Average Age | **41.6** |
| Average Credit Score | **694.9** |
| At Risk Customers | **68** |
| High + Critical Risk | **116** |

### Visualizations

**⚠️ Customers by Risk Category**  
Displays the number of customers classified as Low, Medium, High, and Critical risk.

**👤 Customer Status Distribution**  
Shows the distribution of customers across Active, At Risk, Closed, and Dormant statuses.

**🏦 Risk by Bank**  
Uses a 100% stacked bar chart to compare the risk composition of customers across the three banks.

**🎯 Segment vs Risk**  
Shows how risk is distributed across different customer segments and helps identify segments with higher concentrations of risk.

### Business Questions Answered

- How many customers are at risk?
- How many customers fall into High or Critical risk?
- What is the overall customer risk distribution?
- Which banks have different risk profiles?
- How does risk vary across customer segments?
- What percentage of customers are active, dormant, closed, or at risk?

---

# 🎛️ Interactive Features

The dashboards include interactive **Power BI slicers** that allow users to dynamically filter the analysis.

### Available Filters

- 🏦 Bank
- 👥 Customer Segment
- 🔄 Customer Status
- ⚠️ Risk Category
- 📅 Transaction Date

When a filter is selected, the relevant **KPIs and visualizations update dynamically**, allowing users to explore the data from different perspectives.

---

# 🧮 DAX & Data Analysis

The project uses **DAX measures** to calculate important business metrics.

### Examples

```DAX
Total Customers =
DISTINCTCOUNT(Banking[Customer_ID])
```

```DAX
Total Balance =
SUM(Banking[Account_Balance])
```

```DAX
Total Loan Amount =
SUM(Banking[Loan_Amount])
```

```DAX
Transaction Value =
SUM(Banking[Transaction_Amount])
```

```DAX
Average Credit Score =
AVERAGE(Banking[Credit_Score])
```

```DAX
At Risk Customers =
CALCULATE(
    [Total Customers],
    Banking[Customer_Status] = "At Risk"
)
```

```DAX
High Critical Risk =
CALCULATE(
    [Total Customers],
    Banking[Risk_Category] IN {"High", "Critical"}
)
```

More measures are available in the **DAX** folder.

---

# 🎨 Dashboard Design

The report follows a **modern banking-inspired visual design**.

### Design Principles

- Clean dashboard structure
- Strong KPI hierarchy
- Compact slicers
- Consistent spacing
- Blue-based banking theme
- Risk-focused accent colors
- Minimal visual clutter
- Interactive filtering
- Business-oriented storytelling

The dashboards were designed to balance **aesthetics with analytical usability**, making them suitable for both presentation and exploratory analysis.

---

# 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Power BI** | Dashboard development & visualization |
| **Power Query** | Data cleaning & transformation |
| **DAX** | Measures & analytical calculations |
| **Excel / CSV** | Dataset preparation |
| **GitHub** | Project documentation & version control |

---

# 📁 Repository Structure

```text
Global-Banking-Analytics-PowerBI/
│
├── Dataset/
│   └── Global_Banking_Analytics.csv
│
├── PowerBI/
│   └── Global_Banking_Analytics.pbix
│
├── Dashboard/
│   ├── Dashboard-1-Executive-Overview.png
│   └── Dashboard-2-Customer-Risk.png
│
├── DAX/
│   ├── Banking-DAX-Measures.md
│   └── Banking-DAX-Measures.txt
│
├── Documentation/
│   ├── Data-Dictionary.md
│   ├── Dashboard-Documentation.md
│   └── Project-Presentation.md
│
└── README.md
```

---

# 💡 Key Insights

The dashboards provide several useful observations from the dataset:

- The banking portfolio contains **700 customers**.
- Total customer balances amount to approximately **$203.1M**.
- Total loan exposure is approximately **$147.8M**.
- Transaction value is approximately **$21.1M**.
- The average credit score is approximately **694.9**.
- **68 customers** are classified as At Risk.
- **116 customers** fall into the combined High + Critical risk categories.
- Customer distribution can be compared across the three banks.
- Risk concentration can be analyzed by both bank and customer segment.

These insights demonstrate how Power BI can convert raw banking records into a more accessible **business intelligence layer**.

---

# 📚 What I Learned

This project helped me develop practical experience in:

- Data cleaning and preparation
- Power Query
- Data modeling
- DAX
- KPI development
- Interactive slicers
- Cross-filtering
- Data visualization
- Customer analytics
- Risk analysis
- Dashboard UI/UX
- Business storytelling

One of the biggest lessons from this project was that **a good dashboard is not simply a collection of charts**. The visualizations need to answer specific business questions and guide the user from high-level performance to deeper analysis.

---

# 🚀 Future Improvements

Potential future enhancements include:

- More detailed loan analysis
- Branch-level performance analysis
- Transaction channel analysis
- Monthly transaction trends
- Advanced customer segmentation
- Additional financial KPIs
- Predictive risk analysis
- Automated data refresh

---

## 👨‍💻 Project

**Global Banking Analytics — Power BI**

Built as a practical **Data Analytics & Business Intelligence project** to demonstrate the ability to transform raw banking data into interactive, business-focused dashboards.

---

### ⭐ If you find this project useful

Feel free to explore the dashboards, DAX measures, and documentation to understand how the analysis was structured.

**Power BI • Data Analytics • Business Intelligence • DAX • Banking Analytics • Customer Analytics • Risk Analytics**