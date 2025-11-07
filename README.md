# 🏦 Bank Loan Report Dashboard

A data-driven analytics dashboard designed to evaluate a bank’s **loan performance, portfolio health, and borrower risk characteristics** through key KPIs, SQL queries, and business insights.

---

## 🧭 1. Project Title / Headline
**Bank Loan Report Dashboard — Banking Analytics with Power BI & SQL**

---

## 📝 2. Short Description / Purpose
The **Bank Loan Report Dashboard** helps financial institutions track lending operations and assess portfolio quality.  
It provides **data-driven insights into loan applications, funding, repayments, and borrower behavior**, enabling better lending decisions, early risk detection, and strategic improvements in credit policy.

### 🔍 Business Purpose:
- Monitor overall **lending performance and risk exposure**  
- Identify patterns in **loan defaults vs repayments**  
- Support **data-driven decisions** in loan approval and collections

---

## ⚙️ 3. Tech Stack

| Category | Tools / Technologies |
|-----------|---------------------|
| **Data Source** | SQL Database (bank_loan_data) |
| **Querying** | SQL (MySQL / SQL Server) |
| **Data Visualization** | Power BI / Tableau |
| **Data Cleaning** | Excel, Power Query |
| **Documentation** | Word, Markdown (README) |

---

## 🗂 4. Data Source
The dataset used in this project contains real-world banking attributes related to **loan applications and borrower profiles**.

**Key Columns:**
- `Loan_ID`, `Loan_Status`, `Loan_Amount`, `Funded_Amount`, `DTI`, `Interest_Rate`
- `Employment_Length`, `Grade`, `Sub_Grade`, `Purpose`, `Home_Ownership`, `State`
- `Issue_Date`, `Term`, `Total_Payment_Received`

📘 *Data sourced from a structured banking database simulating real lending scenarios.*

---

## 💡 5. Features & Highlights

### 🏦 Business Problem
Banks often face challenges understanding how loans perform across multiple segments — customer types, geographies, and risk categories.  
This dashboard consolidates all that information to:
- Identify **good vs bad loans**
- Highlight **funding and repayment patterns**
- Measure **risk concentration and portfolio performance**

---

### 🎯 Goal of the Dashboard
To build an **interactive loan analytics dashboard** that tracks:
- Total loan applications
- Funded and received amounts
- DTI and interest-rate-based risk indicators
- Monthly performance (MTD, MoM)
- Good vs Bad loan categorization

---

### 🔍 Walk-Through of Key Visuals

#### 📍 **Dashboard 1: Summary View**
- KPI cards showing overall metrics (Applications, Funding, Received Amount)
- Loan status grid highlighting portfolio quality
- Quick view of MTD & MoM growth

#### 🌍 **Dashboard 2: Overview**
| Visual Type | Purpose |
|--------------|----------|
| **Line Chart** | Monthly trends (Applications, Funding, Payments) |
| **Filled Map** | State-wise performance & disbursal patterns |
| **Donut Chart** | Loan term distribution |
| **Bar Chart** | Employee length & loan purpose segmentation |
| **Tree Map** | Home ownership contribution to loans |

👉 Reveals seasonal trends, risk concentration, and geographic impact.

#### 📊 **Dashboard 3: Detailed View**
- Tabular report with all borrower data  
- Enables data filtering & in-depth analysis for operations

---

### 📈 Business Impact & Insights
- Identified **Good Loans (Fully Paid, Current)** vs **Bad Loans (Charged-Off)**  
- Detected portfolio leakage in **high-interest-rate loans**  
- Optimized lending focus on **low DTI and stable employment segments**  
- Helped management **reduce NPA (Non-Performing Asset)** risk by early detection  
- Supported data-driven decision making and compliance monitoring

---

## 📸 6. Screenshots

### 🔹 Dashboard Summary
![Bank Loan Summary Dashboard](https://github.com/Karan-Dahiwale/Bank-Loan-Analysis/blob/main/Bank%20Loan%20Report%20(Summery).png)

### 🔹 Business Overview
![Loan Overview Visuals](https://github.com/Karan-Dahiwale/Bank-Loan-Analysis/blob/main/Bank%20Loan%20Report%20(Overview).png)

*(Note: Replace with your Power BI or Tableau dashboard screenshots in your repo folder: `/assets/dashboard_1.png`, `/assets/dashboard_2.png`)*

---

## 🧮 Example SQL Queries

```sql
-- Total loan applications
SELECT COUNT(id) AS Total_Applications
FROM bank_loan_data;

-- Total funded amount
SELECT SUM(loan_amount) AS Total_Funded_Amount
FROM bank_loan_data;

-- Good loan performance
SELECT COUNT(id), SUM(funded_amount), SUM(total_payment)
FROM bank_loan_data
WHERE loan_status IN ('Fully Paid', 'Current');
