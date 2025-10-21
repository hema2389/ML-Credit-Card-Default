# 🧾 Exploratory Data Analysis (EDA) — Default of Credit Card Clients Dataset

## 📘 Project Overview
This project performs **Exploratory Data Analysis (EDA)** on the **Default of Credit Card Clients Dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/).  
The goal is to analyze the demographic, financial, and behavioral patterns that influence **credit card default** among clients.

---

## 📊 Dataset Information
- **Source:** UCI Machine Learning Repository  
- **Dataset ID:** 350  
- **Records:** 30,000  
- **Features:** 23 independent variables + 1 target variable  
- **Target Variable:** `default.payment.next.month`  
  - `1` → Defaulted  
  - `0` → Non-default  

### Key Columns
| Feature | Description |
|----------|--------------|
| `LIMIT_BAL` | Credit limit (in NT dollars) |
| `SEX` | Gender (1 = Male, 2 = Female) |
| `EDUCATION` | Education level (1 = Graduate, 2 = University, 3 = High School, others = Unknown) |
| `MARRIAGE` | Marital status (1 = Married, 2 = Single, others = Others) |
| `AGE` | Age of the client |
| `PAY_1` to `PAY_6` | Payment status (last 6 months) |
| `BILL_AMT1` to `BILL_AMT6` | Bill statement amounts (last 6 months) |
| `PAY_AMT1` to `PAY_AMT6` | Amounts paid (last 6 months) |

---

## 🧠 Objective
Perform EDA to:
- Understand the **distribution** of clients and defaults  
- Analyze **demographic trends** (Gender, Education, Marriage, Age)  
- Examine **credit and payment behavior**  
- Identify **patterns or correlations** that may influence defaults  

---

## ⚙️ Tools & Libraries Used
- **Python 3.12+**
- **Google Colab / Jupyter Notebook**
- **Libraries:**
  ```python
  pandas
  numpy
  matplotlib
  seaborn
  ucimlrepo
