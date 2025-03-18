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

Exploratory Data Analysis (EDA)

Exploring the Customer Table

Handling Missing Values in the Annual Income Column

50 null values detected.

Instead of removing, missing values were replaced using the occupation-wise median for accuracy.

Descriptive Statistics for the Customer Table

Age: Min = 1, Max = 135 (Valid range: 18 - 80 as per business manager).

Annual Income: Min = 2, Max = 447K (Valid minimum: 100 as per business rule).

Handling Outliers in the Annual Income Column

Outlier Detection: Standard deviation method (values beyond ±3 standard deviations considered outliers).

Upper Outliers: Verified and found valid (e.g., high-income business owners).

Lower Outliers: Minimum income is 2, but business rule states income should be at least 100.

Treatment: Replaced values below 100 with the occupation-wise median.

Handling Null Values in the Age Column

No missing values found.

Handling Outliers in the Age Column

Min Age: 1, Max Age: 135 (Valid range: 18 - 80 as per business manager).

Outliers Detected: 20 records.

Treatment Options:

Removing them (not ideal, as data loss occurs).

Replacing with mean or median.

Chosen Method: Occupation-wise median age for more accuracy.

Exploring the Credit Score Table

Data Cleaning 1: Removing Duplicates

Total rows: 1004.

Identified 4 duplicate rows based on cust_id.

Last occurrence of each duplicate retained; earlier ones removed.

Data Cleaning 2: Handling Missing Values in the Credit Limit Column

65 null values found.

Business Insight: Credit limits are linked to credit scores.

Treatment: A mathematical relationship between credit score and credit limit was explored for imputation.

Data Cleaning 3: Handling Outliers in Outstanding Debts

Some debts exceed credit limits, which is illogical.

Business Rule: A customer's debt should not exceed their credit limit.

Treatment: Checked and corrected inconsistencies.

Exploring the Transaction Table

Data Cleaning 1: Handling Null Values in the Platform Column

4941 rows have null values.

Business Insight: Amazon is the most frequently used platform for purchases.

Treatment: Replaced null values with "Amazon" (especially for electronic purchases).

Data Cleaning 2: Handling Outliers in Transaction Amount

Outlier Detection: IQR method (values beyond 1.5 times IQR considered outliers).

Treatment Options:

Winsorization (capping at lower and upper bounds).

Removing extreme outliers (if justified by business needs).

Final Notes

The dataset has been thoroughly cleaned by:

Handling missing values.

Removing duplicates.

Treating outliers using statistical and business logic.

![Analysis](https://github.com/user-attachments/assets/52152b81-1329-43d7-a812-293c5e68511b)

