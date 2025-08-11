# ML-Credit-Card-Default
#  Credit Card Default Prediction – EDA & ML

##  Overview  
This project conducts **Exploratory Data Analysis (EDA)** and develops **Machine Learning (ML)** models on the **UCI “Default of Credit Card Clients”** dataset. The goal is to analyze patterns in client data and accurately predict the likelihood of default next month—vital for credit risk management and financial institutions.

---

##  Dataset  
- **Source**: UCI Machine Learning Repository – *Default of Credit Card Clients* dataset :contentReference[oaicite:0]{index=0}  
- **Instances**: 30,000 clients :contentReference[oaicite:1]{index=1}  
- **Features**: 23 explanatory variables + target variable :contentReference[oaicite:2]{index=2}  
- **No missing values** – dataset is clean and complete :contentReference[oaicite:3]{index=3}  

**Key Variables:**

- `LIMIT_BAL`: Credit limit amount (NT dollars) :contentReference[oaicite:4]{index=4}  
- Demographics:
  - `SEX` (1=male, 2=female)
  - `EDUCATION` (1=graduate, 2=university, 3=high school, 4=others, etc.)
  - `MARRIAGE` (1=married, 2=single, 3=others)
  - `AGE` (years) :contentReference[oaicite:5]{index=5}  
- **Payment history** (`PAY_0` to `PAY_6`): Repayment status from September to April 2005 (scale from -2/no consumption to 9 = delay ≥ 9 months) :contentReference[oaicite:6]{index=6}  
- **Bill statements** (`BILL_AMT1` to `BILL_AMT6`): Amounts billed from September to April 2005 :contentReference[oaicite:7]{index=7}  
- **Previous payments** (`PAY_AMT1` to `PAY_AMT6`): Amounts paid during the same period :contentReference[oaicite:8]{index=8}  
- **Target**: `default.payment.next.month` — 1 indicates default next month, 0 otherwise :contentReference[oaicite:9]{index=9}  

---

##  Objectives  

### EDA Goals:
- Understand demographic and credit behavior of clients
- Examine distribution of features and their relationships with default outcome
- Identify key risk indicators such as payment delays, bill amounts, demographics

### Modeling Goals:
- Build classification models to predict default risk (binary: default vs. non-default)
- Compare model performance using Logistic Regression, Random Forest, XGBoost, Neural Networks
- Address class imbalance (~22% defaulters) using techniques like SMOTE, undersampling :contentReference[oaicite:10]{index=10}  
- Use evaluation metrics: accuracy, precision, recall, F1-score, AUC, confusion matrix

---

##  Tools & Libraries  
- **Data & Analysis**: `pandas`, `numpy`  
- **Visualization**: `matplotlib`, `seaborn`, `plotly`  
- **Modeling & Preprocessing**: `scikit-learn`, `imblearn` (e.g., SMOTE)  
- (Optional) Use `xgboost` for boosting algorithms or `tensorflow/keras` for deep learning

---

##  Project Workflow  

### 1. Data Ingestion & Preprocessing
- Load dataset (e.g., CSV or Excel)
- Rename and clean columns for clarity
- Check for missing values (none are expected) :contentReference[oaicite:11]{index=11}  

### 2. EDA
- Analyze distributions (LIMIT_BAL, AGE, bill/payment amounts)
- Visualize default rates across categorical features (EDUCATION, MARRIAGE, SEX)
- Correlation heatmap among numerical variables to detect multicollinearity

### 3. Feature Engineering & Balancing
- Create features like average bill/payment, number of delayed payments, bill-to-payment ratio
- Address class imbalance with SMOTE or undersampling :contentReference[oaicite:12]{index=12}

### 4. Model Training & Evaluation
- Apply different classifiers: Logistic Regression, Random Forest, XGBoost, Neural Net
- Use stratified train-test split and cross-validation
- Evaluate models with classification metrics and ROC curves

### 5. Insights & Interpretation
- Identify strong default predictors (e.g., high delay count, high bills, young age)
- Share model insights and potential business risk use cases  

---

##  Sample Visualizations  
- **Bar charts**: Default rates by education, marital status  
- **Histograms/box plots**: Distribution of credit limit, bill amounts, age  
- **Heatmaps**: Feature correlations showing multicollinearity  
- **ROC curves**: Compare classifiers’ trade-off between sensitivity and specificity

---

##  Expected Outcomes  
- Clear insights into what drives default risk among clients  
- A predictive model capable of identifying high-risk clients  
- Balanced evaluation confirming robustness and reliability of models

---

##  Future Work  
- Incorporate deep learning architectures (e.g., MLP neural networks) :contentReference[oaicite:13]{index=13}  
- Explore explainability (SHAP, LIME) for actionable business insights  
- Build a risk scorecard system for real-time credit risk monitoring  

---

##  How to Run  
```bash
git clone https://github.com/<username>/credit-default-eda-ml.git
cd credit-default-eda-ml
pip install -r requirements.txt
jupyter notebook credit_default_analysis.ipynb
