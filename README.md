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

### Churn Rate =
DIVIDE(
    CALCULATE(
        COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn]),
        'WA_Fn-UseC_-Telco-Customer-Churn'[Churn] = "Yes"
    ),
    COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn])
)

### Customer Retention Rate =
DIVIDE(
    CALCULATE(
        COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn]),
        'WA_Fn-UseC_-Telco-Customer-Churn'[Churn] = "No"
    ),
    COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[Churn])
)


### Total Subscription Revenue
Total Subscription Revenue =
SUM(
    'WA_Fn-UseC_-Telco-Customer-Churn'[TotalCharges]
)

---

## Report Overview
### 👥 Customer Overview

#### The customer overview provides a high-level understanding of the customer base, including:

- Total subscribers
- Churn rate
- Retention rate
- Total revenue
- Average monthly revenue
- Gender distribution
- Senior citizen status
- Partner and dependent status
- Internet service
- Online security
- Payment methods
### 📉 Churn Analysis

#### The churn analysis examines customer churn across key business dimensions, including:

- Contract type
- Gender
- Customer tenure
- Payment method
- Internet service
- Online security
- Technical support
- Device protection

---


## Key Insight
Customer Base

### 1. ABC Communications has 7,043 subscribers, with a relatively balanced gender distribution:

50.48% male
49.52% female

Only 16.21% of customers are senior citizens.

### 2. Contract Type is a Major Churn Driver

Customers on month-to-month contracts have the highest likelihood of churning.

The analysis indicates that customers on month-to-month contracts are approximately 6.32 times more likely to churn compared with customers on longer-term contracts.

Customers on two-year contracts demonstrate the strongest retention.

### 3. Tenure Influences Retention

-- Customer retention increases as tenure increases.

-- This indicates that newer customers represent an important retention opportunity and should receive additional engagement during the early stages of their relationship with the company.

### 4. Value-Added Services Influence Churn

Customers without services such as:

- Online Security
- Technical Support
- Device Protection

-- show higher levels of churn.

--These services may increase perceived customer value and contribute to stronger customer loyalty.

### 5. Payment Method Influences Churn

Customers using Electronic Check have the highest churn among the payment methods analyzed.

This suggests that payment experience and payment method may be important factors in customer retention.

---

## 💉 Key drivers of churn rate
The analysis highlights factors such as:

- Month-to-month contracts
- Lack of Online Security
- Lack of Technical Support
- Fiber Optic internet service
- Electronic Check payment method
- Customer tenure


## ⚠️ Business Risks
### 1. Revenue Loss

High customer churn can result in the loss of recurring revenue and lower customer lifetime value.

### 2. Increased Customer Acquisition Costs

Replacing customers who leave requires additional marketing and acquisition expenditure.

### 3. Competitive Customer Loss

Customers on flexible month-to-month contracts can switch easily to competitors offering better prices, promotions, or services

---

## Recommendations
### 1. Encourage Customers to Subscribe to Long-Term Contracts
Introduce attractive discounts, loyalty rewards, or exclusive benefits for customers who migrate from month-to-month subscriptions to one-year or two-year contracts. This strategy will improve customer retention and provide more predictable revenue.

### 2. Strengthen Technical Support Services
Invest in responsive, high-quality technical support to resolve customer issues quickly. Providing 24/7 support, faster issue resolution, and proactive customer assistance will improve customer satisfaction and reduce churn.

### 3. Promote Online Security Services
Educate customers on the benefits of Online Security and offer promotional bundles or free trial periods. Customers who use Online Security services are less likely to leave because they perceive greater value from the company's offerings.

### 4. Encourage the Adoption of Device Protection Services
Increase awareness of Device Protection plans through targeted marketing campaigns and bundled service packages. Protecting customer devices enhances the overall customer experience and strengthens loyalty.

### 5. Review Fiber Optic Customer Experience
Although Fiber Optic is the most popular internet service, it is also associated with higher churn. Management should investigate customer complaints, assess service quality, network reliability, pricing, and customer support for Fiber Optic users. Improving the overall experience for this customer segment could significantly reduce churn.

### 6. Improve Payment Experience
Encourage customers using Electronic Check to switch to automatic payment methods such as bank transfers or credit card payments. Offering incentives for automatic payments can improve convenience and reduce churn associated with billing issues.

---
## Project Summary

Customer Churn Analysis transforms telecommunications customer data into actionable insights by identifying the customer segments and factors associated with churn and translating those findings into targeted retention strategies.

