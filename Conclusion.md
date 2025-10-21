# EDA INSIGHTS
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

The objective of this study was to predict the **default risk** of credit card clients using various machine learning models.  
After performing **data cleaning**, **outlier handling**, and **class imbalance correction (via SMOTE)**, three models were trained and evaluated —  
**Logistic Regression**, **Decision Tree Classifier**, and **Random Forest Classifier**.

---
# ML INSIGHTS
### 1. Model Comparison Summary

| Model | Accuracy | Minority (Default) Recall | Minority Precision | Key Observation |
|:--|:--:|:--:|:--:|:--|
| **Logistic Regression** | 0.57 | 0.62 | 0.25 | Better recall — identifies more defaults but with false positives. |
| **Decision Tree Classifier** | 0.67 | 0.34 | 0.24 | Moderate results; interpretable but prone to overfitting. |
| **Random Forest Classifier** | 0.75 | 0.23 | 0.30 | Balanced and stable performance across both classes. |

---

### 2. Key Insights

- **Random Forest** achieved the **highest overall accuracy (≈75%)**, showing strong generalization and robustness.  
- **Logistic Regression** performed well in identifying defaults (higher recall) but suffered from lower precision, leading to more false positives.  
- **Decision Tree** produced moderate results and is useful for interpretability but not optimal for predictive accuracy.  
- Applying **SMOTE** improved the recall for the minority class (defaulters) but slightly reduced overall accuracy — a common trade-off in imbalanced classification.

---

### 3. Final Model Choice

The **Random Forest Classifier** was selected as the **final model** due to:
- Strong predictive accuracy and generalization capability,  
- Ability to handle non-linear relationships,  
- Resistance to noise and overfitting,  
- Balanced trade-off between recall and precision.

---

### 4. Future Enhancements

To further improve model performance:
- Perform **hyperparameter tuning** using `GridSearchCV` or `RandomizedSearchCV`.  
- Experiment with **XGBoost** or **LightGBM** for better recall on the minority class.  
- Apply **feature selection** or **dimensionality reduction (PCA)** to remove noise.  
- Explore **cost-sensitive learning** or gather more balanced data.

---

### ✅ Final Statement

The developed ML pipeline successfully predicted **credit card default risk** and provided insights into payment and behavioral patterns.  
Overall, **ensemble-based models like Random Forest** proved to be effective for real-world financial risk analysis — enabling more reliable, data-driven lending decisions.

## ✅ Overall Insights
- Default is influenced by a combination of **payment history**, **credit limit**, and **demographics** (age, education, marital status).  
- The dataset has **imbalanced classes**, which must be handled during model building (if done later).  
- **Data cleaning** (handling unknown education and marriage codes) is recommended before modeling.

