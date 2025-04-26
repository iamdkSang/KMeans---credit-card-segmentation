
---

# **Parallel K-Means Clustering & PCA for Credit Card Data**

This repository contains the implementation of parallelized K-Means clustering and PCA (Principal Component Analysis) using Python and Numba, aimed at speeding up the computation for large datasets. The project focuses on segmenting credit card users based on their transaction patterns and reducing data dimensionality to extract meaningful insights. These insights are then utilized to propose effective marketing strategies.

## **Members**
- 20127214: Nguyễn Trương Minh Khôi
- 20127612: Đỗ Khánh Sang

## **Project Overview**

### **1. Objective**
- **Parallel K-Means Clustering**: To efficiently group credit card users into distinct segments based on their behavior using a parallelized version of the K-Means algorithm.
- **Parallel PCA**: To reduce the dimensionality of the dataset using a parallelized PCA approach, making it easier to visualize and analyze.
- **Data Insights & Marketing Strategies**: To extract insights from the clustered data and propose targeted marketing strategies based on these insights.

### **2. Dataset**
- **Credit Card Dataset**: The dataset used in this project is the "Credit Card Dataset for Clustering," which contains anonymized data of credit card users. The data includes features such as balance, purchases, cash advance, and more.
- **Kaggel link**: [Kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata).

### **3. Methodology**

#### **A. Sequential Implementations**
- **K-Means Clustering**: A basic implementation of the K-Means algorithm to group similar users.
- **PCA**: A traditional PCA implementation to reduce the dimensions of the dataset.

#### **B. Parallel Implementations**
- **Parallel K-Means**: Implemented using Numba with parallel processing capabilities to significantly speed up the clustering process on both CPU and GPU.
- **Parallel PCA**: PCA is optimized using Numba to reduce computation time, allowing faster processing of large datasets.

### **4. Project Structure**
- **/20127214_20127612.ipynb**: Contains Jupyter notebooks that demonstrate the implementation and comparison of sequential vs. parallelized versions of K-Means and PCA.
- **/data**: Includes the pre-processed credit card dataset.
- **/Slides**: Slides to report.
- **README.md**: This document.

### **5. Insights & Marketing Strategies**

#### **I. Cluster Insights**

1. **Cluster 0:**
   - **Profile:** Customers with low overall purchase amounts, low transaction frequency, and low one-off purchases.
   - **Insight:** This cluster represents low-engagement customers. They might be cautious spenders or less active in using their credit cards.

2. **Cluster 1:**
   - **Profile:** Customers with high purchase amounts and transaction frequency, but low one-off purchase amounts.
   - **Insight:** These customers are regular spenders who prefer smaller, frequent transactions. They might be using the card for daily expenses rather than large, occasional purchases.

3. **Cluster 2:**
   - **Profile:** Customers with high purchase amounts, high transaction frequency, and high one-off purchases.
   - **Insight:** This is the premium segment, with customers who make frequent transactions and are also willing to spend large amounts in a single go. They likely have higher credit limits and are more comfortable with larger financial commitments.


#### **II. Marketing Strategies**

1. **Cluster 0 (Low Engagement):**
   - **Objective:** Increase card usage.
   - **Strategy:**
     - **Promotional Offers:** Introduce targeted promotions like cashback or discounts for transactions made within specific categories (e.g., groceries, fuel).
     - **Engagement Campaigns:** Encourage these customers to use their cards more frequently by offering bonuses or rewards for reaching certain spending thresholds.
     - **Educational Content:** Provide content that educates them on the benefits of using credit cards for various types of purchases.

2. **Cluster 1 (Frequent Small Spenders):**
   - **Objective:** Encourage higher-value purchases.
   - **Strategy:**
     - **Upgrade Offers:** Offer incentives to upgrade their credit limits or switch to cards with better benefits, which might encourage them to make larger purchases.
     - **Bundle Offers:** Introduce bundled services or products that require higher spending, such as travel packages or electronics, combined with financing options.
     - **Loyalty Programs:** Enhance loyalty programs that reward frequent use with points that can be redeemed for larger purchases.

3. **Cluster 2 (High Spenders):**
   - **Objective:** Retain and reward premium customers.
   - **Strategy:**
     - **Exclusive Rewards:** Offer exclusive rewards such as luxury travel perks, concierge services, or access to premium events to retain these high-value customers.
     - **Personalized Offers:** Provide personalized offers based on their spending history, such as discounts on categories they frequently spend in or special financing for large purchases.
     - **VIP Programs:** Create a VIP program with higher rewards rates, lower interest rates, or exclusive access to premium products and services.

After performing clustering and dimensionality reduction, the project analyzes the resulting segments to uncover user behavior patterns. Based on these insights, the following marketing strategies are proposed:
- **Targeted Campaigns**: Identify high-value customers and create personalized marketing campaigns.
- **Product Recommendations**: Suggest relevant products or services to different segments based on their usage patterns.
- **Customer Retention**: Implement loyalty programs for segments that show a tendency to churn.

## **Getting Started**

### **Prerequisites**
- Python 3.7 or later
- Google Colab
- Libraries: Numpy, Pandas, Matplotlib, Seaborn, Numba, Scikit-learn

### **Usage**
Open the Google Colab in the `/20127214_20127612.ipynb` directory to explore the implementations and results, execute the K-Means and PCA algorithms on the dataset.

### **Performance Comparison**
- A detailed comparison of the execution times for sequential vs. parallelized versions is provided in the notebooks, highlighting the efficiency gains achieved through parallelization.

### **Contributing**
Contributions are welcome! Please fork this repository and submit a pull request with your improvements or bug fixes.

### **License**
This project is licensed under the MIT License.

### **Acknowledgments**
- The dataset used in this project is provided by [Kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata).
- Special thanks to the developers of Numba for their amazing tool that makes parallel computing in Python accessible.

---
