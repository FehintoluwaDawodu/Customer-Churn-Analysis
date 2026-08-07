# 📊 Customer Churn Analysis

This project analyzes **customer churn and retention** for a telecommunications company, **ABC Communications**, using Microsoft Power BI, Power Query, DAX, and Excel.

The analysis explores customer demographics, contract types, payment methods, tenure, service adoption, and the key factors influencing customer churn and retention.

The objective is to transform customer data into **actionable business insights** that can support customer retention, revenue protection, and data-driven decision-making.

---

## 🎯 Project Objectives

The analysis seeks to answer the following business questions:

1. What does the customer base look like?
2. Which customer segments have the highest churn?
3. Does contract type influence customer retention?
4. Does customer tenure affect loyalty?
5. Which services influence customer churn?
6. Which payment methods have higher churn?
7. What actions should management take to reduce churn?

---

## 🛠️ Tools & Technologies

- **Microsoft Power BI** – Dashboard development and data visualization
- **Power Query** – Data cleaning and transformation
- **DAX** – KPI and measure development
- **Microsoft Excel** – Data inspection and preparation
- **CSV** – Source dataset format

---

## 📂 Dataset

### Telco Customer Churn Dataset

The project uses the Telco Customer Churn dataset obtained from Kaggle.

**Dataset Source:**

https://www.kaggle.com/datasets/blastchar/telco-customer-churn

The dataset contains customer-level information including:

- Customer demographics
- Contract type
- Tenure
- Internet service
- Payment method
- Online security
- Technical support
- Device protection
- Monthly charges
- Total charges
- Churn status

---

# 🔄 Data Analytics Process

The project followed a structured data analytics workflow.

## 1. Data Import

The telecommunications customer dataset was imported into Power BI from a CSV file.

## 2. Data Cleaning & Transformation

Power Query was used to prepare the dataset for analysis by:

- Removing inconsistencies
- Checking data quality
- Standardizing data types
- Transforming variables where necessary
- Preparing the dataset for visualization and analysis

## 3. Data Analysis

The cleaned dataset was analyzed to understand the relationship between customer characteristics and churn.

The analysis focused on:

- Customer demographics
- Contract type
- Customer tenure
- Internet service
- Online security
- Technical support
- Device protection
- Payment methods
- Customer churn
- Customer retention

## 4. DAX Measures

DAX was used to create key performance indicators and analytical measures.

### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    CALCULATE(
        COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn]),
        'WA_Fn-UseC_-Telco-Customer-Churn'[Churn] = "Yes"
    ),
    COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn])
)
-- Customer Retention Rate =
DIVIDE(
    CALCULATE(
        COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn]),
        'WA_Fn-UseC_-Telco-Customer-Churn'[Churn] = "No"
    ),
    COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn])
)
-- Total Subscription Revenue =
SUM('WA_Fn-UseC_-Telco-Customer-Churn'[TotalCharges])
