# Churn-Analysis-Project
# Bank-Churn-Analysis

**Dashboard Link:** https://app.powerbi.com/groups/me/dashboards/a7cb0511-62d8-46cb-ab50-1cc2df2a6c22?ctid=a1d0d612-1d52-4d5b-a047-01a1056ce8c3&pbi_source=linkShare

---

## Problem Statement

This analysis aims to help the bank understand its customer churn rates and identify factors contributing to customer churn. By analyzing data from France, Spain, and Germany, the bank can make informed decisions to reduce churn rates and improve customer retention.

### Key Insights:
- The overall churn rate stands at **20.4%**, with the target being **15%**.
- Significant factors contributing to churn include:
  - **Age groups:** Customers aged **51-60** have the highest churn rate.
  - **Credit scores:** Low credit scores (<400) are associated with a **100% churn rate**.
  - **Account balances:** Customers with high account balances (>200k) have the highest churn rate (**55.9%**).

By targeting these areas, the bank can work toward reducing churn and improving customer satisfaction.

---

## Steps Followed

### 1. Data Loading
- Imported the dataset (CSV format) into **Power BI Desktop**.

### 2. Data Preview
- Used Power Query Editor to examine the dataset by enabling:
  - **Column Distribution**
  - **Column Quality**
  - **Column Profile**

### 3. Data Cleaning
- Removed unnecessary columns (e.g., **Estimated Salary**).
- Renamed products to "Prod 1," "Prod 2," etc., using the **Add Column by Example** feature.
- Updated binary-coded columns (e.g., Credit Card Status) with descriptive labels (e.g., **Owned**/**Not Owned**).
- Grouped numerical columns (e.g., Age, Credit Score, Account Balance) into ranges.
- Ranked grouped columns using a reference and calculated column for sorting.

### 4. Data Modeling
- Established relationships between tables in the data model.

### 5. Measure Creation
- **Total Customers:**  
  Customers = COUNT('Customer Data'[Customer ID])
  
   ![image](https://github.com/user-attachments/assets/672cdbb5-13f7-4e0e-bbea-3d9216b13700)

- **Churned Customers:**  
  `Customers Lost = CALCULATE(COUNT('Customer Data'[Churn Status]), 'Customer Data'[Churn Status] = "Churned")`

   ![image](https://github.com/user-attachments/assets/a018a10d-5b0f-41d0-b33f-052fb6b50614)

- **Churn Rate:**  
  `Churn Rate = 'Customer Data'[Customers Lost] / 'Customer Data'[Customers]`

   ![image](https://github.com/user-attachments/assets/94299efe-e62b-4ac7-aa47-53397ba307e0)


### 6. Visualization Design
- **Card visuals**: Total customers and churn rate.
  
  ![image](https://github.com/user-attachments/assets/12474c12-f56d-4b13-b6d8-ab32f9e8ed14)

- **Gauge visual**: Compare churn rate against the target.

  ![image](https://github.com/user-attachments/assets/0158b7a1-f2f8-4b25-a1e0-92bba980c71c)

- **Donut charts**: Customer distributions by gender, activity status, credit card ownership, country, and products.

 ![image](https://github.com/user-attachments/assets/d8fb1713-c5a4-4bc5-9b65-6b76a544aad9)

- **Area charts**: Customer and churn rates by age groups, credit scores, and account balances.

 ![image](https://github.com/user-attachments/assets/ab9dee42-169b-4e40-a1f7-de61d0d87af3)


### 7. Publishing
- Uploaded the report to **Power BI Service** for sharing and collaboration.

---

## Insights

### Customers
- **Total Customers:** 10,000  
  - Male Customers: 5,457  
  - Female Customers: 4,543

- **Activity Status:**  
  - Active: 5,151  
  - Inactive: 4,849  

- **Credit Card Ownership:**  
  - Owned: 7,055  
  - Not Owned: 2,945  

- **Country Distribution:**  
  - France: 5,014  
  - Germany: 2,473  
  - Spain: 2,477  

- **Product Usage:**  
  - **Product 1**: Most popular across genders and countries.

### Churn Analysis
- **Overall Churn Rate:** 20.4% (Target: 15%)

#### Churn by Product
- **Product 2:** Lowest churn rate of **7.6%**.

#### Churn by Age Group
- **Highest:** Customers aged 51-60 at **56.2%**.  
- **Lowest:** Customers aged 20 and below at **5.6%**.

#### Churn by Credit Score
- **Credit Score < 400:** 100% churn rate.  
- **Credit Scores 601-700 & 801+:** Lowest churn rates (~19.7%).

#### Churn by Account Balance
- **10k-100k:** 20.5% churn rate.  
- **200k+:** Highest churn rate of **55.9%**.

---

## Snapshots

### Dashboard (Power BI Service)


![Screenshot (501)](https://github.com/user-attachments/assets/4b21adf4-08df-42d3-8d98-7a5e807897af)

### Report (Power BI Desktop)

![Screenshot (500)](https://github.com/user-attachments/assets/9e6e6876-e041-4054-9722-fc712a54a8e5)

## Insights  
  

#### Customer Overview  
- The bank serves **10,000 customers**, with:  
  - **54.57% male** and **45.43% female** customers.  
  - **51.5% active** and **48.5% inactive** customers.  
  - **70.55% own credit cards**, while **29.45% do not**.  

#### Country Distribution  
- **France:** 50.14% of total customers, the largest share.  
- **Spain:** 24.77% of total customers, the smallest share.  

#### Product Preferences  
- **Product 1** is the most popular across all demographics.  

---

### Churn Analysis  

#### Overall Churn Rate  
- The churn rate is **20.4%**, exceeding the target of **15%**.  
- **Female customers** have a higher churn rate (**25.1%**) compared to males (**16.5%**).  

#### Churn by Age Group  
- Customers aged **51-60** have the highest churn rate at **56.2%**, indicating significant dissatisfaction.  
- Customers aged **20 and below** have the lowest churn rate at **5.6%**.  

#### Churn by Credit Score  
- **Credit scores below 400**: **100% churn rate**, suggesting critical retention issues.  
- **Credit scores 601-700 and 801+**: Lowest churn rates (~**19.7%**).  

#### Churn by Account Balance  
- Accounts with balances over **200k** have the highest churn rate at **55.9%**.  
- Accounts between **10k-100k** have a churn rate of **20.5%**.  

#### Product Analysis  
- **Product 2** has the lowest churn rate at **7.6%**, indicating higher satisfaction with this product.  

---

## Recommendations  

### 1. Improve Retention in High-Churn Segments  
- **Age 51-60**: Implement tailored loyalty programs and products to meet the needs of this group.  
- **Low Credit Scores**: Provide education on credit improvement and retention offers for customers with low scores.  

### 2. Focus on High-Balance Customers  
- Investigate why customers with balances over **200k** are churning.  
- Offer premium services, relationship managers, or rewards to retain these high-value customers.  

### 3. Address Gender-Specific Churn  
- **Female Customers**: Design personalized offers, better service channels, and women-focused products to address the higher churn rate among female customers.  

### 4. Leverage Product Insights  
- **Product 2**: Analyze the features of Product 2 that lead to lower churn rates and replicate these qualities in other products.  
- **High-Churn Products**: Reassess the value proposition of products with higher churn rates and adjust accordingly.  

### 5. Competitive Benchmarking  
- Study competitors’ offerings in **France** and **Germany** to stay competitive and meet or exceed their features.  

### 6. Churn Prediction and Proactive Engagement  
- Implement predictive analytics to identify customers at risk of churning and engage them proactively with targeted communications, offers, and retention campaigns.  

### 7. Educational Campaigns for Low-Balance and Low-Credit Customers  
- Offer financial literacy programs for customers with low credit scores or account balances to help improve their financial standing and loyalty.  

By implementing these recommendations, the bank can effectively reduce its churn rate, meet its **15% target**, and enhance overall customer satisfaction and retention.
