## AtliQ Bank Credit Card Project -  Exploratory Data Analysis

## 📌 Objective

The primary objective of this analysis is to examine customer transactions and credit profiles to identify a target group for the launch of the AtliQ Bank credit card. The study focuses on understanding spending behavior, risk assessment, and optimizing marketing strategies based on data-driven insights.

## 🛠 Tools Used

Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)

SQL (MySQL for data extraction and transformation)

Jupyter Notebook (for exploratory data analysis and visualization)

Excel (for cross-verification and reporting)

## 📚 Concepts Discussed & Skills Gained

## 📌 Data Cleaning & Preprocessing

Handling missing values (mean/median imputation, occupation-based median income replacement)

Removing duplicate records

Outlier detection using standard deviation & IQR method

Capping extreme values based on business constraints

## 📌 Exploratory Data Analysis (EDA)

Understanding customer demographics

Identifying spending patterns and transaction trends

Analyzing credit profiles (credit score distribution, utilization, outstanding debt)

## 📌 Statistical Analysis & Visualization

Correlation analysis (credit score vs. credit limit)

Data distribution analysis using histograms and box plots

Identifying trends through bar charts and scatter plots

## 📌 Segmentation & Targeting

Customer segmentation based on age, income, and spending behavior

Identifying high-value customers for targeted marketing

## 📌 Risk Assessment & Fraud Detection

Evaluating credit score vs. credit limit correlation

Identifying customers with outstanding debt exceeding their credit limit

Detecting invalid transactions (zero or unrealistic amounts)

## 📌 Marketing Strategy Optimization

Identifying preferred transaction platforms and product categories

Analyzing payment method preferences

Formulating targeted promotions based on user behavior

## 📊 Expected Outcomes

## 🔹 Customer Segmentation for Credit Card Targeting

Identify high-income, high-spending customers.

Define risk categories based on credit score and utilization rates.

## 🔹 Understanding Spending Behavior

Determine most frequently purchased product categories.

Analyze platform preferences for online transactions.

## 🔹 Risk & Fraud Detection

Identify outliers in credit utilization and debt repayment.

Flag anomalies in transaction data.

## 🔹 Optimized Credit Card Marketing Strategy

Determine which customer segments to target with specific offers.

Personalize credit limits based on customer profiles.

## 🔍 Key Insights & Findings

## 🔹 Customer Segmentation

Largest Customer Group: Age 26-48 (56.7%)

Highest Income Segments: Business Owners & Consultants

Young Customers (18-25): Lower credit exposure, but potential for growth

## 🔹 Spending Patterns

## Top 3 Spending Categories:

Electronics

Fashion & Apparel

Beauty & Personal Care

Most Used Platforms: Amazon, Flipkart, Alibaba

City Customers Spend More than Rural Customers

## 🔹 Credit Profile Analysis

## Credit Score Correlation:

Credit Score & Credit Limit (0.85 correlation) → Higher scores lead to higher limits.

Low Scores (300-499) → Lower credit limits and higher risk.

Outstanding Debt: Some customers exceeded their credit limit, requiring a cap.

## 🔹 Outlier Handling & Data Cleaning

Missing annual income values replaced with occupation-wise median.

Extreme age values (below 15 & above 80) replaced with median per occupation.

Zero transaction amounts (Amazon purchases) replaced with category median.

Outliers in credit limits corrected using historical trends.

## 🔹 Marketing Strategy Optimization

Primary Target: Customers aged 26-48 with high spending power.

Secondary Target: 18-25 age group (credit adoption potential).

Promotion Focus: High-value customers (Business Owners, Consultants).

Best Platforms for Promotion: Amazon, Flipkart, Alibaba.

Encourage Credit Card Use: By offering better rewards & cashback.

## 🎯 Final Recommendations

Launch targeted offers for high-income segments (e.g., business owners, consultants).

Increase credit limits for users with high credit scores and strong transaction history.

Offer cashback & rewards to attract younger customers (18-25 age group).

Run platform-specific promotions on Amazon, Flipkart, and Alibaba.

Monitor high-risk customers with poor credit scores and high utilization.

## 📌 Conclusion

This analysis provides data-driven insights to support AtliQ Bank’s credit card launch. By leveraging customer segmentation, spending behavior insights, and risk assessments, the bank can optimize its marketing and risk management strategies effectively.

# Project Details

## Datasets
1. **Customers**
2. **Credit Profiles**
3. **Transactions**
4. **Average Transactions After Campaign**

## Importing Data Sets via SQL
```sql
-- Example SQL command
SELECT * FROM Customers;
```

## Exploring the Data
```python
df.shape
df.describe()
df.nunique()
df.isnull()
df.isna()
```

# Exploratory Data Analysis

## Exploring the Customer Table

### Handling Missing Values in the `Annual Income` Column
- There are **50 null values** in the `Annual Income` column.
- Instead of removing them (to prevent data loss), we replace them using the **occupation-wise median**.

### Customer Table Summary
- **Age:** Minimum = 1, Maximum = 135 (Business manager stated the valid age range should be **18 to 80**).
- **Annual Income:** Minimum = 2, Maximum = 447k (Annual income should **not be below 100**).

### Treating Outliers in `Annual Income`
- A common practice is to treat values that deviate **±3 standard deviations** as outliers.
- **High-end outliers:** Business owners often have high incomes, so these values are retained.
- **Low-end outliers:** Business rules dictate that income should be at least **100**.
  - These values could be data errors.
  - Possible actions:
    1. **Remove them** (but we decided to keep them).
    2. **Replace with the median** (preferred over the mean).
    3. **Replace with the occupation-wise median** (best approach).

### Handling Null Values in the `Age` Column
- **No null values found.**

### Treating Outliers in the `Age` Column
- **Minimum:** 1
- **Maximum:** 135
- Business rules specify that **age should be between 15 and 80**.
- **20 outliers identified.**
- Possible actions:
  1. Remove them (not ideal as it would lead to data loss).
  2. Replace with the mean/median.
  3. Use the **median age per occupation** (best approach).

## Exploring the Credit Score Table

### Data Cleaning Step 1: Removing Duplicates
```python
df.drop_duplicates(subset=['cust_id'], keep='last', inplace=True)
```
- **Total rows:** 1004
- **Duplicate rows:** 4
- The last occurrence of each duplicate is retained, and earlier occurrences are removed.

### Data Cleaning Step 2: Handling Null Values in the `Credit Limit` Column
- **65 null values** found in the `credit_limit` column.
- Based on business knowledge, credit limits depend on **credit scores**.
- Approach:
  - Identify the mathematical relationship between **credit score** and **credit limit**.
  - Use the credit score to fill in missing values in the `credit_limit` column.

### Data Cleaning Step 3: Identifying Outliers in `Outstanding Debts`
- **Maximum outstanding debt exceeds the maximum credit limit.**
- Business rules dictate that a customer’s debt should not exceed their credit limit.
- Identify such cases and correct them accordingly.

## Exploring the Transaction Table

### Data Cleaning Step 1: Handling Null Values in the `Platform` Column
- **4,941 rows** contain null values in the `platform` column.
- **Amazon** is the most frequently used platform.
- Missing values are replaced with **"Amazon"**.

### Data Cleaning Step 2: Handling Outliers in `Transaction Amount`
- Outliers in the `Trans_Amount` column were identified using the **IQR method**.
- Values beyond **1.5× the interquartile range** were considered outliers.
- Approach:
  - Extreme values were capped at the lower and upper bounds.
  - In some cases, extreme outliers were removed based on business requirements.




# Customer Transaction
![Analysis](https://github.com/user-attachments/assets/52152b81-1329-43d7-a812-293c5e68511b)


# Correlation Of Credit Score Profiles
![Correlation](https://github.com/user-attachments/assets/a03e9e48-568e-49a0-bd98-aebefc40e63a)


