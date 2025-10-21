# EDA INSIGHTS
---
### 1. Dataset Overview
- The dataset contains information about **30,000 credit card clients** in Taiwan.  
- The target variable **"default"** indicates whether a client defaulted (1 = Yes, 0 = No).  
- There are **23 features**, including demographic details, credit history, bill amounts, and payment records.

---

### 2. Target Variable Distribution
- Around **77.9%** of clients did **not default**.  
- About **22.1%** of clients **defaulted**, showing a **class imbalance** (important for modeling).


### 3. Gender (SEX)
- **Females** form the majority of the dataset.  
- **Default rates** are slightly **higher among males** compared to females.



### 4. Education (EDUCATION)
- Most clients fall under **Education level 2 (University)** followed by **level 1 (Graduate school)**.  
- A few values like **0, 4, 5, 6** indicate inconsistent or unrecognized categories — they should ideally be grouped under “Others.”  
- **Default rates** are slightly higher for those with **lower education levels.**


### 5. Marital Status (MARRIAGE)
- Majority are **Single (2)** or **Married (1)**.  
- A few entries are **Others (3 or 0)**.  
- **Single clients** show a **slightly higher default tendency** compared to married ones.


### 6. Age (AGE)
- Most clients are aged between **25-40 years.**  
- Younger individuals (<30) tend to have **higher default rates**.


### 7. Limit Balance (CREDIT_LIMIT)
- The credit limit ranges widely from **10,000 to 1,000,000 TWD.**  
- Clients with **lower credit limits** show **higher default rates**.


### 8. Payment History & Bill Amounts
- Clients with a **history of delayed payments (`PAY_1` to `PAY_6`)** show **significantly higher default rates.**  
- **Bill amounts** and **previous payments** vary widely, indicating diverse spending and repayment behaviors.


### 9. Correlation Insights
- Strong correlations observed among **bill amounts** and among **payment amounts** across months.  
- The **target variable** shows moderate correlation with **past payment delays.**



## ✅ Overall Insights
- Default is influenced by a combination of **payment history**, **credit limit**, and **demographics** (age, education, marital status).  
- The dataset has **imbalanced classes**, which must be handled during model building (if done later).  
- **Data cleaning** (handling unknown education and marriage codes) is recommended before modeling.

