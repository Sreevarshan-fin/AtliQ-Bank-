## AtliQ Bank Credit Card Project - Analysis Report

##📌 Objective

The primary objective of this analysis is to examine customer transactions and credit profiles to identify a target group for the launch of the AtliQ Bank credit card. The study focuses on understanding spending behavior, risk assessment, and optimizing marketing strategies based on data-driven insights.

🛠 Tools Used

Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)

SQL (MySQL for data extraction and transformation)

Jupyter Notebook (for exploratory data analysis and visualization)

Excel (for cross-verification and reporting)

📚 Concepts Discussed & Skills Gained

📌 Data Cleaning & Preprocessing

Handling missing values (mean/median imputation, occupation-based median income replacement)

Removing duplicate records

Outlier detection using standard deviation & IQR method

Capping extreme values based on business constraints

📌 Exploratory Data Analysis (EDA)

Understanding customer demographics

Identifying spending patterns and transaction trends

Analyzing credit profiles (credit score distribution, utilization, outstanding debt)

📌 Statistical Analysis & Visualization

Correlation analysis (credit score vs. credit limit)

Data distribution analysis using histograms and box plots

Identifying trends through bar charts and scatter plots

📌 Segmentation & Targeting

Customer segmentation based on age, income, and spending behavior

Identifying high-value customers for targeted marketing

📌 Risk Assessment & Fraud Detection

Evaluating credit score vs. credit limit correlation

Identifying customers with outstanding debt exceeding their credit limit

Detecting invalid transactions (zero or unrealistic amounts)

📌 Marketing Strategy Optimization

Identifying preferred transaction platforms and product categories

Analyzing payment method preferences

Formulating targeted promotions based on user behavior

📊 Expected Outcomes

🔹 Customer Segmentation for Credit Card Targeting

Identify high-income, high-spending customers.

Define risk categories based on credit score and utilization rates.

🔹 Understanding Spending Behavior

Determine most frequently purchased product categories.

Analyze platform preferences for online transactions.

🔹 Risk & Fraud Detection

Identify outliers in credit utilization and debt repayment.

Flag anomalies in transaction data.

🔹 Optimized Credit Card Marketing Strategy

Determine which customer segments to target with specific offers.

Personalize credit limits based on customer profiles.

🔍 Key Insights & Findings

🔹 Customer Segmentation

Largest Customer Group: Age 26-48 (56.7%)

Highest Income Segments: Business Owners & Consultants

Young Customers (18-25): Lower credit exposure, but potential for growth

🔹 Spending Patterns

Top 3 Spending Categories:

Electronics

Fashion & Apparel

Beauty & Personal Care

Most Used Platforms: Amazon, Flipkart, Alibaba

City Customers Spend More than Rural Customers

🔹 Credit Profile Analysis

Credit Score Correlation:

Credit Score & Credit Limit (0.85 correlation) → Higher scores lead to higher limits.

Low Scores (300-499) → Lower credit limits and higher risk.

Outstanding Debt: Some customers exceeded their credit limit, requiring a cap.

🔹 Outlier Handling & Data Cleaning

Missing annual income values replaced with occupation-wise median.

Extreme age values (below 15 & above 80) replaced with median per occupation.

Zero transaction amounts (Amazon purchases) replaced with category median.

Outliers in credit limits corrected using historical trends.

🔹 Marketing Strategy Optimization

Primary Target: Customers aged 26-48 with high spending power.

Secondary Target: 18-25 age group (credit adoption potential).

Promotion Focus: High-value customers (Business Owners, Consultants).

Best Platforms for Promotion: Amazon, Flipkart, Alibaba.

Encourage Credit Card Use: By offering better rewards & cashback.

🎯 Final Recommendations

Launch targeted offers for high-income segments (e.g., business owners, consultants).

Increase credit limits for users with high credit scores and strong transaction history.

Offer cashback & rewards to attract younger customers (18-25 age group).

Run platform-specific promotions on Amazon, Flipkart, and Alibaba.

Monitor high-risk customers with poor credit scores and high utilization.

📌 Conclusion

This analysis provides data-driven insights to support AtliQ Bank’s credit card launch. By leveraging customer segmentation, spending behavior insights, and risk assessments, the bank can optimize its marketing and risk management strategies effectively.
