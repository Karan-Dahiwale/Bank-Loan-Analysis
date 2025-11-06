# 🏦 Bank Loan Report Dashboard

A comprehensive analytics solution to evaluate a bank’s lending performance, loan portfolio health, and borrower risk characteristics using key KPIs, domain knowledge, and SQL-driven insights.

---

## 📌 Problem Statement
To monitor and assess bank lending performance, this dashboard provides detailed insights into:

- Total loan applications and funding trends
- Loan repayment efficiency
- Borrower risk assessment through DTI & Loan Status
- Month-to-date (MTD) and Month-over-month (MoM) tracking for all metrics

It helps the bank make informed lending decisions and improve portfolio management strategies. :contentReference[oaicite:0]{index=0}

---

## 🎯 Key KPIs Tracked

| KPI | Description |
|-----|-------------|
| Total Loan Applications | Count of overall loan submissions |
| Total Funded Amount | Total principal disbursed |
| Total Amount Received | Loan payments collected from borrowers |
| Average Interest Rate | Lending pricing metric |
| Average Debt-to-Income Ratio | Borrower financial health evaluation |

All metrics include:  
✅ Overall, ✅ MTD, ✅ MoM comparisons :contentReference[oaicite:1]{index=1}

---

## ✅ Good Loan vs Bad Loan Categorization
| Category | Loan Status Used |
|----------|-----------------|
| **Good Loans** | Fully Paid, Current |
| **Bad Loans** | Charged Off |

KPIs evaluated for each category:
- Number of applications
- Total funded amount
- Total payment received :contentReference[oaicite:2]{index=2}

---

## 📊 Dashboard Views

### 📍 Dashboard 1: Summary
KPI cards + Loan Status Grid View

---

### 🌍 Dashboard 2: Overview
Visual insights:

| Chart Type | Dimensions |
|------------|------------|
| Line Chart | Monthly trends (Applications, Funding, Received Amount) |
| Filled Map | State-wise lending performance |
| Donut Chart | Loan Term distribution |
| Bar Chart | Employee length + Loan Purpose analysis |
| Tree Map | Home ownership segmentation |

Reveals seasonal patterns & geographic disparities. :contentReference[oaicite:3]{index=3}

---

### 📑 Dashboard 3: Details
Comprehensive tabular view of all borrower & loan attributes  
→ Enables deep drill-down and operational monitoring :contentReference[oaicite:4]{index=4}

---

## 🏦 Banking Domain Understanding (Business View)
Why analyzing loan data matters:

- Credit risk assessment
- Customer retention & profiling
- Fraud detection
- Portfolio performance optimization
- Regulatory compliance-driven reporting

Includes major steps in loan lifecycle:  
Application → Verification → Approval → Disbursement → Monitoring → Repayment :contentReference[oaicite:5]{index=5}

---

## 🧠 Data Field Terminology (Short Dictionary)
Examples:

| Field | Meaning |
|-------|--------|
| DTI | Measures repayment capacity |
| Loan Status | Identifies performance health of loan |
| Interest Rate | Cost of borrowing |
| Grade / Subgrade | Borrower risk classification |
| Employment Length | Indicator of income stability |

Used for risk-based pricing & underwriting decisions. :contentReference[oaicite:6]{index=6}

---

## 🗄 SQL Queries Used
All KPIs & dashboard visuals are powered by SQL queries, such as:

```sql
SELECT COUNT(id) AS Total_Applications
FROM bank_loan_data;
