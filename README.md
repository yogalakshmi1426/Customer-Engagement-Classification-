# 🧠 Customer Engagement Classification

This project uses logistic regression to analyze and predict customer engagement behavior based on various features such as website visits, email opens, and monthly spend. The analysis was conducted for a portfolio assignment in the context of a retail company aiming to improve digital engagement and retention.

---

## 📊 Problem Statement

A retail company is struggling with low customer engagement despite a strong customer base. Using the provided customer dataset, the goal is to:

1. Predict customer engagement using logistic regression.
2. Identify which factors influence engagement most.
3. Propose three actionable data-driven strategies to boost engagement.
4. Acknowledge potential limitations and implementation challenges.

---

## 🗃️ Dataset Overview

The dataset contains the following features:

- `Customer_ID` – Unique ID for each customer
- `Age` – Age of the customer
- `Tenure_Months` – Duration of the customer's relationship (in months)
- `Monthly_Spend` – Average monthly spend
- `Support_Tickets` – Number of support tickets raised
- `Email_Opens` – Number of marketing emails opened
- `Website_Visits` – Number of visits to the company's website
- `Engaged` – **Target variable (1 = engaged, 0 = not engaged)**

---

## 🧪 Methods

### ✔️ Data Cleaning & Exploration
- Checked for null values, duplicates, and data types.
- No missing data was found.
- Used `.describe()`, `.info()`, and `.value_counts()` for initial profiling.

### ✔️ Feature Selection
Selected:
- `Email_Opens`
- `Website_Visits`
- `Monthly_Spend`
- `Support_Tickets`
- `Tenure_Months`

These features were chosen based on intuition and correlation with engagement.

### ✔️ Model Building
- Used **StatsModels' Logit (Logistic Regression)** from `statsmodels.api`.
- Added a constant term to predictors using `add_constant()`.
- Trained the model on the full dataset.

### ✔️ Evaluation
- Checked model summary for p-values and coefficient significance.
- Identified key engagement drivers (Website_Visits, Email_Opens).
- Interpreted log-odds to explain likelihood of engagement.

---

## 📈 Key Findings

- **Website_Visits** and **Email_Opens** had strong positive coefficients.
- Higher `Monthly_Spend` alone wasn’t enough — interaction was needed.
- Support ticket count negatively affected engagement (possible friction).

---

## 📌 Recommendations

Based on the model’s insights, here are three data-driven strategies:

1. **Enhance Email Campaigns:**  
   Customers opening more emails were significantly more engaged. Personalized and relevant content could further drive this.

2. **Website Personalization:**  
   Frequent website visits are linked with engagement. Improve UX and recommend products based on browsing behavior.

3. **Optimize Support Channels:**  
   High support ticket counts reduced engagement. Streamlining issue resolution may improve the user experience and satisfaction.

---

## ⚠️ Implementation Considerations

- **Model Limitation:** Only a few features were used. More behavioral and demographic data could improve predictions.
- **Binary Outcome Simplification:** Real-world engagement is often multi-level (e.g., partially engaged).
- **Bias in Self-Reported Behavior:** Customers who open emails may also be more tech-savvy, introducing sample bias.

---

## 📁 Repository Contents

