# Churn-Analysis-Project
# Bank-Churn-Analysis

**Dashboard Link:** [Add Power BI dashboard link here]

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
  `Customers = COUNT('Customer Data'[Customer ID])`
- **Churned Customers:**  
  `Customers Lost = CALCULATE(COUNT('Customer Data'[Churn Status]), 'Customer Data'[Churn Status] = "Churned")`
- **Churn Rate:**  
  `Churn Rate = 'Customer Data'[Customers Lost] / 'Customer Data'[Customers]`

### 6. Visualization Design
- **Card visuals**: Total customers and churn rate.
- **Gauge visual**: Compare churn rate against the target.
- **Donut charts**: Customer distributions by gender, activity status, credit card ownership, country, and products.
- **Area charts**: Customer and churn rates by age groups, credit scores, and account balances.

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
![Dashboard Snapshot](# "Insert dashboard snapshot link here")

### Report (Power BI Desktop)
![Report Snapshot](# "Insert report snapshot link here")
