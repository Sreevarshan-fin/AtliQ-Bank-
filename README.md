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

## Datasets
1. Customers
2. Credit_Profiles
3. Transaction
4. Average Transaction After Campaign

## Import Data Sets Read Through SQL
```sql
-- Example SQL query to import datasets
SELECT * FROM Customers;
SELECT * FROM Credit_Profiles;
SELECT * FROM Transaction;
SELECT * FROM Average_Transaction_After_Campaign;

🔎 Exploratory Data Analysis (EDA)
🧑‍💻 Explore Customer Table
Handling Missing Values in Annual Income Column
50 null values found.
Solution: Replace nulls with occupation-wise median income instead of removing them to retain important data.
Customer Table Summary
Age: min = 1, max = 135 (Valid range: 18 to 80 as per business insights)
Annual Income: min = 2, max = 447K (Valid range: Above 100)
🛠️ Treatment of Outliers (Annual Income)
Standard Deviation Method: Identifies outliers beyond ±3 standard deviations.
Decision:
Higher income outliers are retained (valid data for business owners).
Lower income outliers are corrected (income should be at least 100).
Possible Treatments:
❌ Remove Outliers → Not ideal, as we lose valid customers.
🔄 Replace with Mean/Median → Median is preferred due to sensitivity to extreme values.
📊 Replace with Occupation-Wise Median → Best approach for more accurate representation.
Handling Missing Values in Age Column
No null values detected.
🛠️ Treatment of Outliers (Age Column)
Observed Range: min = 1, max = 135 (Valid range: 15 to 80 as per business manager)
20 outliers found
Treatment Approach:
Replace with occupation-wise median age instead of removing them.
🏦 Explore Credit Score Table
✅ Data Cleaning - Step 1: Removing Duplicates
python
Copy code
df.drop_duplicates(subset=['cust_id'], keep='last', inplace=True)
4 duplicate rows removed (last occurrence retained).
🛠️ Data Cleaning - Step 2: Handling NULL Values in Credit Limit Column
65 missing values found
Solution:
Establish a relationship between credit score and credit limit to predict missing values.
🚨 Data Cleaning - Step 3: Outliers in Outstanding Debts
Identified cases where outstanding debt > credit limit (violates business logic).
Solution: Correct cases where outstanding debt should not exceed credit limits.
💳 Explore Transaction Table
🛠️ Data Cleaning - Step 1: Handling NULL Values in Platform Column
4,941 missing values
Solution: Replace missing values with "Amazon" (most frequently used platform).
📊 Data Cleaning - Step 2: Handling Outliers in Transaction Amount
Used Interquartile Range (IQR) method to identify outliers.
Solution:
Extreme values capped at lower & upper bounds.
Some extreme cases were removed based on business insights.


# Customer Transaction
![Analysis](https://github.com/user-attachments/assets/52152b81-1329-43d7-a812-293c5e68511b)


# Correlation Of Credit Score Profiles
![Correlation](https://github.com/user-attachments/assets/a03e9e48-568e-49a0-bd98-aebefc40e63a)


