## AtliQ Bank Credit Card Project -  Exploratory Data Analysis

# 🏦 AtliQ Bank Credit Card Analysis

## 📌 Overview
AtliQ Bank planned to launch a **new credit card** and needed to identify the most suitable customer segment while minimizing financial risks.  

---

## ⭐ Situation
### 🔹 Identifying Target Customers
- Understanding **customer demographics & spending behavior**  
- Segmenting customers based on **income, credit history, and transactions**  

### 🔹 Assessing Credit Risk & Fraud Detection
- Analyzing **credit scores, utilization rates, and outstanding debts**  
- Detecting **anomalies** such as extreme credit utilization and suspicious transactions  

### 🔹 Optimizing the Marketing Strategy
- Understanding **preferred spending platforms and product categories**  
- Personalizing **offers and rewards** to increase credit card adoption  

A **data-driven approach** was required to **clean, analyze, and interpret** customer transaction patterns, ensuring the marketing strategy was **targeted and risk-free**.

---

## 🎯 Task
The objectives of the analysis were:

### 1️⃣ Customer Segmentation
- Classify customers based on **age, income, spending behavior, and credit profiles**  
- Identify **high-value customers** with strong transaction history  
- Differentiate between **low-risk and high-risk** customers  

### 2️⃣ Understanding Spending Behavior
- Determine the **top spending categories** and preferred payment methods  
- Analyze **transaction trends** across different platforms and locations  

### 3️⃣ Credit Risk Assessment & Fraud Detection
- Evaluate customers **exceeding their credit limits**  
- Detect **outliers and fraudulent transactions** based on spending trends  

### 4️⃣ Optimizing Marketing Strategies
- Develop **data-driven recommendations** for promotional campaigns  
- Personalize **credit limits and offers** based on customer behavior  

---

## 🚀 Action
To meet these objectives, the following **data analysis and machine learning techniques** were used:

### 🔹 1. Data Cleaning & Preprocessing

#### 📌 Data Sources:
- **Customers Table** (Demographics, Annual Income)  
- **Credit Profiles Table** (Credit Scores, Credit Limits, Outstanding Debts)  
- **Transactions Table** (Purchase Amounts, Platforms, Categories)  

#### 📌 Handling Missing Values:
- **Annual Income** → 50 missing values replaced with **occupation-wise median income**  
- **Credit Limit** → 65 missing values imputed using a **credit score-based regression model**  
- **Transaction Platform** → 4,941 missing values filled with **Amazon** (most frequent platform)  

#### 📌 Duplicate Record Removal:
✔ **4 duplicate customer records** removed  

#### 📌 Outlier Detection & Treatment:

| Column | Issue | Fix |
|--------|-------|-----|
| **Age** | Outliers (Min: 1, Max: 135) | Capped between **18-80** (median-based correction) |
| **Annual Income** | Extreme values detected | Adjusted **low-income outliers** to ₹100K minimum threshold |
| **Transaction Amount** | Extreme purchases (IQR method) | Capped transactions exceeding **99th percentile** |

---

### 🔹 2. Exploratory Data Analysis (EDA)

#### 📌 Customer Demographics & Segmentation
- **Age Distribution:**  
  ✔ Largest segment: **26-48 years (56.7%)**  
  ✔ **Young customers (18-25):** Low credit exposure, high potential  

- **Income Distribution:**  
  ✔ **Highest income segments:** Business Owners & Consultants  
  ✔ **Middle-class consumers:** Moderate spending, consistent credit usage  

#### 📌 Spending Patterns

| Category | Spending Share (%) |
|----------|-------------------|
| **Electronics** | 35.2% |
| **Fashion & Apparel** | 28.7% |
| **Beauty & Personal Care** | 15.4% |

✔ **Preferred Transaction Platforms:**  
- **Amazon (52%)**, **Flipkart (32%)**, **Alibaba (16%)**  
- **City customers spend** 20% **more than rural customers**  

---

### 🔹 3. Credit Risk Assessment & Fraud Detection

#### 📌 Credit Score vs. Credit Limit Correlation
✔ Pearson Correlation: **0.85** (**Strong positive correlation**)  
✔ Customers with **low credit scores (300-499)** had **lower credit limits & higher default risk**  
✔ Customers **with scores above 750** received significantly higher limits  

#### 📌 Outstanding Debt Analysis
✔ Some customers had **debts exceeding their credit limits**  
✔ Identified **high-risk customers** with low repayment history  
✔ Suggested **credit cap enforcement** for customers exceeding **90% utilization**  

#### 📌 Fraud Detection: Anomalous Transactions
✔ **Zero transaction amounts** (Amazon) were flagged and replaced with **category median**  
✔ **Unrealistic transactions** (>95th percentile) were **investigated**  

---

### 🔹 4. Marketing Strategy Optimization

✔ **Primary Target Group:**  
  - **Age 26-48**, high spending power  
  - **Business Owners & Consultants (Income > ₹500K)**  

✔ **Secondary Target Group:**  
  - **Young customers (18-25):** Potential for credit adoption  

✔ **Optimized Promotional Strategies:**  
  - **Cashback & rewards** to **increase credit card usage**  
  - **Higher credit limits** for strong repayment history  
  - **Platform-specific promotions** on **Amazon, Flipkart, Alibaba**  

---

## 📊 Result

### ✅ 1. Customer Segmentation for Credit Card Targeting
✔ Identified **high-value customers** for the credit card  
✔ Segmented customers into **low, medium, and high-risk groups**  

### ✅ 2. Spending Behavior Insights
✔ Most popular categories: **Electronics, Fashion, Beauty**  
✔ Preferred transaction platforms: **Amazon, Flipkart, Alibaba**  
✔ **City-based customers** spend more than rural customers  

### ✅ 3. Risk & Fraud Detection
✔ Flagged **outliers in credit utilization & debt repayment**  
✔ Identified **high-risk customers exceeding credit limits**  
✔ Corrected **anomalies in transaction data**  

### ✅ 4. Optimized Marketing & Credit Strategies
✔ Targeted **promotional campaigns** for high-income users  
✔ **Personalized credit limits** based on customer profiles  
✔ Increased engagement through **cashback & reward programs**  

---

## 📌 Final Recommendations  
🔹 **Increase credit limits** for customers with strong credit history  
🔹 Offer **promotional discounts** on Amazon, Flipkart, and Alibaba  
🔹 Launch **targeted offers** for business owners & high-income segments  
🔹 Encourage **younger customers (18-25)** with cashback rewards  
🔹 Monitor **high-risk customers** with low credit scores and excessive debt  

---

## 🏁 Conclusion  
This project successfully provided **data-driven insights** for AtliQ Bank’s credit card launch. By leveraging **customer segmentation, spending behavior analysis, and credit risk assessment**, AtliQ Bank can:  

✔ **Optimize marketing strategies**  
✔ **Enhance credit risk management**  
✔ **Maximize customer engagement & adoption rates**  

---

## 📂 Technologies Used  
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)  
- **SQL** (MySQL)  
- **Jupyter Notebook**  
- **Power BI & Excel** for visualization  

---

### 📌 **Author**  
👤 **Sree Varshan**  
💼 Aspiring **Data Analyst & Data Scientist**  
📧 **[Your Email]**  
🔗 **[LinkedIn Profile]**  

---

### ⭐ **Like this project? Give it a star!** ⭐  





# Customer Transaction
![Analysis](https://github.com/user-attachments/assets/52152b81-1329-43d7-a812-293c5e68511b)


# Correlation Of Credit Score Profiles
![Correlation](https://github.com/user-attachments/assets/a03e9e48-568e-49a0-bd98-aebefc40e63a)


