# Financial-Performance-Analysis-Dashboard
# 📊 Finance Analytics Dashboard | Power BI

## 📌 Project Overview

The Finance Analytics Dashboard is an interactive Power BI solution designed to help financial teams monitor transaction performance, analyze revenue trends, track taxes and fees, and compare business performance across different time periods.

This dashboard transforms raw financial transaction data into meaningful insights through data modeling, DAX calculations, and interactive visualizations.

---

## 🎯 Business Problem

Organizations process thousands of financial transactions every day, making it difficult to:

- Monitor overall transaction volume
- Track total transaction value
- Analyze tax and fee collections
- Compare current performance with previous years
- Identify growth and decline trends
- Measure average transaction value
- Make data-driven financial decisions

Without a centralized reporting solution, stakeholders spend significant time gathering and analyzing data manually.

---

## ✅ Solution

Developed a Power BI dashboard that:

- Consolidates financial transaction data into a single reporting platform
- Provides real-time visibility into financial performance
- Tracks key financial KPIs
- Enables Year-over-Year (YoY) analysis
- Visualizes transaction trends across time periods
- Supports strategic decision-making through interactive reports

---

## 📊 Key Metrics Tracked

### Financial KPIs
- Total Transaction Amount
- Total Transactions
- Average Transaction Value
- Total Fees Collected
- Total Tax Collected

### Growth Analysis
- Previous Year Amount
- Year-over-Year Amount Growth
- Previous Year Transactions
- Year-over-Year Transaction Growth
- Previous Year Fees
- Year-over-Year Fee Growth
- Previous Year Tax
- Year-over-Year Tax Growth

---

## 🛠️ Tools & Technologies

- Power BI
- Power Query
- DAX
- Data Modeling
- ETL
- Microsoft Excel
- Business Intelligence

---

## 🗄️ Data Model

The dashboard follows a relational data model consisting of:

### Fact Table
**finance_transactions**

Key fields:

- Transaction ID
- Transaction Date
- Customer ID
- Account ID
- Transaction Type
- Channel
- Merchant Category
- Amount
- Fee Amount
- Tax Amount
- Transaction Status
- Risk Score
- Fraud Indicator

### Dimension Tables

#### Customers
- Customer Information
- Join Date
- Date of Birth

#### Calendar Table
Used for:

- Time Intelligence
- Year-over-Year Analysis
- Trend Analysis

---

## 📉 DAX Measures Used

### Total Amount

```DAX
Total Amount =
SUM(finance_transactions[amount])
```

Calculates total transaction value.

---

### Previous Year Amount

```DAX
PY Amount =
CALCULATE(
    [Total Amount],
    SAMEPERIODLASTYEAR('Calendar table'[Date])
)
```

Returns previous year's amount.

---

### YoY Amount

```DAX
YOY Amount =
[Total Amount] - [PY Amount]
```

Calculates year-over-year growth.

---

### YoY Amount %

```DAX
YOY % =
DIVIDE([YOY Amount],[PY Amount],0)
```

Calculates percentage growth.

---

### Total Transactions

```DAX
Total Transactions =
DISTINCTCOUNT(finance_transactions[transaction_id])
```

Counts unique transactions.

---

### Previous Year Transactions

```DAX
PY Transactions =
CALCULATE(
    [Total Transactions],
    SAMEPERIODLASTYEAR('Calendar table'[Date])
)
```

Returns transaction count from previous year.

---

### YoY Transactions

```DAX
YOY Transactions =
[Total Transactions] - [PY Transactions]
```

Measures transaction growth.

---

### Average Transaction Value

```DAX
Avg Transaction Value =
AVERAGE(finance_transactions[amount])
```

Calculates average value per transaction.

---

### Total Fees

```DAX
Total Fees =
SUM(finance_transactions[fee_amount])
```

Calculates total fees collected.

---

### Previous Year Fees

```DAX
PY Fees =
CALCULATE(
    [Total Fees],
    SAMEPERIODLASTYEAR('Calendar table'[Date])
)
```

Compares fees with previous year.

---

### Total Tax

```DAX
Total Tax =
SUM(finance_transactions[tax_amount])
```

Calculates total taxes collected.

---

### Previous Year Tax

```DAX
PY Tax =
CALCULATE(
    [Total Tax],
    SAMEPERIODLASTYEAR('Calendar table'[Date])
)
```

Returns previous year's tax amount.

---

### YoY Tax

```DAX
YOY Tax =
[Total Tax] - [PY Tax]
```

Measures tax growth.

---

## 📈 Insights Generated

This dashboard helps stakeholders:

- Monitor transaction performance
- Analyze revenue trends
- Track tax and fee collections
- Measure customer transaction activity
- Identify growth opportunities
- Compare financial performance across years
- Support financial planning and forecasting

---

## 🚀 Project Highlights

✔ Interactive Dashboard Design

✔ Financial KPI Monitoring

✔ Time Intelligence Analysis

✔ Year-over-Year Comparisons

✔ Data Modeling

✔ DAX Calculations

✔ Business Intelligence Reporting

✔ Power Query Data Transformation

Screenshot of Dashboard-- https://github.com/ANALYSTRAJANKUMAR/Financial-Performance-Analysis-Dashboard/blob/main/Finance%20report.png
---

## 📧 Contact

Rajan Kumar

Power BI Data Analyst

Email: rajan8991kumar@gmail.com
