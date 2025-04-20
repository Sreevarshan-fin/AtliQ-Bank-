# AtliQ Bank – Credit Card Campaign Analysis

## Objective
The goal of this project was to evaluate the performance of a new credit card campaign targeted at young adults, providing actionable insights into customer segmentation, credit risk, and marketing effectiveness. The analysis was designed to help AtliQ Bank optimize its marketing efforts, improve customer targeting, and manage financial risk—all within a limited budget.

## Problem Statement
AtliQ Bank aimed to launch a new credit card targeting young adults (ages 18–25). Before full-scale implementation, the bank needed to ensure the campaign's effectiveness through data-driven analysis. The challenge was to assess credit risk, identify the best customer segments, and determine the success of the campaign using a statistically valid **A/B test**.

## Role
- Data Analyst: Responsible for performing data cleaning, statistical testing (A/B test), customer segmentation, and providing insights to improve marketing strategy.

## Tools & Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **SQL** (for querying data)
- **Jupyter Notebooks** (for analysis)
- **Scipy** (for statistical analysis)

## Action Taken

### 1. Data Cleaning & Preprocessing:
- **Missing Data**:
  - Imputed missing **income** values using occupation-wise medians.
  - Replaced missing **credit limit** values using regression based on **credit scores**.
  - Filled missing **platform** entries with 'Amazon', the most frequent platform.
  
- **Outliers**:
  - **Age**: Capped between 18–80 using median correction.
  - **Annual Income**: Adjusted extreme low values to a ₹100K minimum threshold.
  - **Transaction Amounts**: Capped using the 99th percentile (IQR method).

### 2. A/B Testing Design & Execution:
- Calculated sample size for the test using:
  - **Effect Size (Cohen’s d)**: 0.4
  - **Power**: 0.8 (80%)
  - **Significance Level (α)**: 0.05
  - **Required Sample Size**: 100 customers for the test group and 40 for the control group.
  
- **Campaign Duration**: 09-Oct to 11-Dec 2023 (2 months)
- **Conversion Rate**: 40% (40 out of 100)
  
- **Statistical Testing**:
  - The **Z-test** was performed to compare daily average transaction amounts.
  - **Z-score** > Critical Z-value and **p-value** < 0.05 → **Reject the null hypothesis**, confirming that the test group performed better than the control group.

### 3. Customer Segmentation & Behavioral Analysis:
- **Segmentation** based on:
  - **Age**, **Income**, **Credit Score**, and **Transaction Behavior**.
  - Identified **high-value users** (e.g., Business Owners) and **low-risk** vs. **high-risk** customers.
  
- **Spending Behavior**:
  - Top spending categories: **Electronics** (35.2%) and **Fashion & Apparel** (28.7%).
  - City-based customers spent 20% more than rural customers.
  - **Top Platforms**: Amazon (52%), Flipkart (32%), Alibaba (16%).

### 4. Credit Risk & Fraud Detection:
- Identified **high-risk customers** with poor credit scores or excessive credit utilization.
- Detected **fraudulent activities** such as zero-value transactions and spending spikes.

## Results
- **40% Conversion Rate** in the test group.
- **Statistically Significant Results**:
  - **Z-score** was higher than the critical Z-value.
  - **p-value** < 0.05 → **Reject the null hypothesis** (campaign had a positive effect).
  
- **Segmentation**: Accurately segmented customers into **low**, **medium**, and **high-risk** tiers.
- **Spending Insights**: Identified top spending categories and preferred platforms (Amazon, Flipkart).
- **Fraud Detection**: Cleaned the data to remove fraudulent behavior.

## Conclusion
This data-driven analysis provided valuable insights to support the bank's decision-making process. The project helped AtliQ Bank:
- Optimize customer targeting strategies.
- Reduce financial exposure by identifying high-risk profiles.
- Increase credit card adoption with targeted offers and personalized campaigns.

## Recommendations
- Increase **credit limits** for reliable, high-score customers.
- Launch targeted **cashback campaigns** on Amazon, Flipkart, and Alibaba.
- Promote credit card adoption among younger users (18–25).
- **Monitor and limit exposure** to high-risk customers.

## Future Work
- Extend analysis to other customer segments.
- Explore additional machine learning models for fraud detection and risk profiling.
- Continuously track campaign performance to refine strategies.

---

## Additional Information
For more details or to explore the project further, check out the repository and data analysis notebooks.



---





# Customer Transaction
![Analysis](https://github.com/user-attachments/assets/52152b81-1329-43d7-a812-293c5e68511b)


# Correlation Of Credit Score Profiles
![Correlation](https://github.com/user-attachments/assets/a03e9e48-568e-49a0-bd98-aebefc40e63a)


