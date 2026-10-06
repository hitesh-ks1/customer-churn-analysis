# Customer Churn & Retention Analysis 📊

An end-to-end customer analytics project analyzing telecom customer churn using **SQL and Power BI**. The objective is to identify high-risk customer segments, understand churn patterns, and derive actionable retention insights.

---

## 📌 Project Overview

The project analyzes **7,043 telecom customer records** containing information about customer tenure, contract type, payment method, internet service, monthly charges, and churn status.

The workflow covers:

**Data Cleaning → SQL Analysis → Power BI Dashboard → Business Insights**

---

## 🛠️ Tools & Technologies

- **SQL (SQLite):** Data cleaning, transformation, and analysis
- **DB Browser for SQLite:** Query execution and data export
- **Power BI:** Dashboard development and visualization
- **DAX:** KPI and analytical measures
- **Excel:** Data validation
- **GitHub:** Project documentation and version control

---

## 🧹 Data Cleaning

The raw dataset was cleaned using SQL.

Key transformations included:

- Removed 11 records with blank `TotalCharges`
- Trimmed whitespace from categorical columns
- Created a binary `Churn_Flag` column
- Created `Tenure_Group` categories for customer segmentation
- Validated the cleaned dataset before visualization

### Before vs After

| Metric | Raw Data | Clean Data |
|---|---:|---:|
| Total Customers | 7,043 | 7,032 |
| Blank TotalCharges | 11 | 0 |
| Churn Flag | Not Available | Added |
| Tenure Group | Not Available | Added |

---

## 📊 SQL Analysis

SQL queries were used to investigate key business questions:

- What is the overall customer churn rate?
- Which contract types have the highest churn?
- How does churn vary with customer tenure?
- Which payment methods are associated with higher churn?
- How do average monthly charges differ between churned and retained customers?
- How does churn vary across internet service types?

All SQL queries are available in:

- `data_cleaning.sql`
- `churn_analysis.sql`

---

## 📈 Power BI Dashboard

An interactive dashboard was developed to monitor customer churn and retention patterns.

### Key Dashboard Components

- Total Customers
- Total Churned Customers
- Overall Churn Rate
- Average Monthly Charges
- Churn by Contract Type
- Churn by Tenure Group
- Churn by Internet Service
- Churned vs Retained Customers
- Internet Service filtering using slicers

---

## 🔍 Key Insights

- **Month-to-month contracts** have substantially higher churn than long-term contracts.
- **Newer customers** show higher churn risk, making the first year an important retention window.
- **Electronic check users** exhibit higher churn compared with other payment methods.
- Customers who churn generally have **higher average monthly charges** than retained customers.
- **Fiber optic customers** show relatively high churn despite being a premium service segment.
- The overall churn rate is approximately **26.5%** in the analyzed dataset.

---

## 💡 Business Recommendations

Based on the analysis:

- Prioritize retention campaigns for month-to-month customers.
- Focus onboarding and engagement efforts on customers in their first year.
- Investigate payment-related friction among electronic check users.
- Review pricing and perceived value for high-charge customers.
- Investigate service-quality and customer-experience issues among fiber optic users.
- Use churn-risk segmentation to prioritize proactive retention efforts.

---

## 📂 Repository Structure

```text
customer-churn-analysis/
│
├── README.md
├── data_cleaning.sql
├── churn_analysis.sql
├── telco_cleaned.csv
└── churn_dashboard.pbix
