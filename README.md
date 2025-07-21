# 📊 Customer Churn Analysis using EDA

## 🚀 Overview

This project focuses on an in-depth **Exploratory Data Analysis (EDA)** of a customer churn dataset to uncover patterns that lead to customer attrition and to make a ** Machine Learning Model**. Customer churn is a key concern for subscription-based services, and understanding what drives users to leave helps improve retention strategies.

Through this notebook, I explored and analyzed structured customer data, clean it, visualize trends, examine statistical patterns, and draw business-focused conclusions.

---

## 🎯 Problem Statement

Churn refers to when customers stop using a company's service. Reducing churn is more cost-effective than acquiring new customers. The goal of this project is to analyze a rich customer dataset and uncover hidden signals that may be influencing churn behavior and also to make a model to predict churn for future scenarios

---

## 📁 Dataset Information

The dataset includes records for numerous customers, with attributes such as:

| Feature              | Description                                        |
|----------------------|----------------------------------------------------|
| `age`                | Age of the customer                                |
| `gender`             | Gender of the customer                             |
| `tenure`             | Duration of time (in months) the customer is active|
| `usage_frequency`    | How often the customer uses the service            |
| `support_calls`      | Number of support interactions                     |
| `payment_delay`      | Number of delayed payment days                     |
| `total_spend`        | Total amount spent by the customer                 |
| `last_interaction`   | Number of days since the last interaction          |
| `subscription_type`  | Type of subscription                               |
| `contract_length`    | Duration of the contract                           |
| `churn`              | Target variable (1 = Churned, 0 = Retained)        |

---

## 🛠 Tools & Technologies Used

- **Language**: Python
- **Notebook**: Jupyter
- **Libraries**:
  - `pandas` – Data manipulation
  - `numpy` – Numerical operations
  - `matplotlib` & `seaborn` – Visualization
  - `scipy.stats` – Statistical testing
  - `sklearn` - For machine learning

---

## 🧹 Data Cleaning & Preparation

- Removed non-essential column: `CustomerID`
- Converted column names to lowercase for consistency
- Checked for:
  - Duplicates (none found)
  - Null values (one column had nulls and was dropped)
  - Unique values (ensured no column had a single constant value)

---

## 🔍 Exploratory Data Analysis (EDA)

### 📌 Univariate Analysis

#### ➤ Age
- Distribution mostly between 20–50
- Very few customers above 60 — likely lower adoption among older individuals

#### ➤ Gender
- Slight male skew in dataset
- No significant imbalance

#### ➤ Tenure
- Uniformly distributed from 1 to 60 months
- Represents a healthy spread of customer ages

#### ➤ Usage Frequency
- Ranges from 1 to 30
- Includes both occasional and regular users

#### ➤ Support Calls
- 70% of customers made less than 5 support calls
- Suggests overall satisfaction, but higher calls may link to churn

#### ➤ Payment Delay
- Most delays are within 20 days
- Long delays may signal dissatisfaction or inability to pay

#### ➤ Total Spend
- Mostly between 100–1000 units
- Higher spenders might be retained longer (hypothesis to test)

#### ➤ Subscription Type & Contract Length
- Long-term contracts are more common
- Indicates user preference or business strategy to lock-in customers

---

### 📌 Bivariate & Statistical Analysis

- Conducted **Levene’s Test** to compare variance across churned vs non-churned users
- Visualizations included:
  - KDE plots to inspect numeric distributions
  - Boxplots for detecting skewness and outliers
  - Cumulative percentage plots for understanding support call patterns

#### 🧠 Key Bivariate Observations

- **Churned customers** had:
  - Higher average support calls
  - More delayed payments
  - Lower tenure on average
- **Contract length** and **subscription type** had limited impact on churn — possibly due to business policy or feature uniformity

---

## 📊 Key Business Insights

1. **Support Calls**: Strong correlation with churn. Customers making many support calls are likely dissatisfied.
2. **Tenure**: Low-tenure customers are at higher churn risk — suggesting need for improved onboarding.
3. **Payment Delay**: Longer delays are common among churned users — consider financial incentives or reminders.
4. **Age**: Middle-aged customers are most active, older groups are least active — potential demographic targeting.

---

## 📌 Visual Summary

All visuals (KDE plots, boxplots, bar charts) are present in the notebook, showing clear distinctions between churned and non-churned groups for:
- Support calls
- Tenure
- Payment delays
- Total spend

---
