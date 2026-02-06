# LoanTap – Credit Underwriting & Default Risk Analysis

## Mindset
This case study focuses on building comfort with **business uncertainty** rather than finding a single “right” answer.  
The objective is to explore the data, apply analytical reasoning, and make **defensible business recommendations** based on statistical and model-driven insights.

---

## About LoanTap
LoanTap is an online lending platform that provides customized loan products to millennials, salaried professionals, and small businesses. The company aims to simplify and modernize the lending experience by offering instant and flexible credit solutions.

LoanTap offers four primary financial products:
- Personal Loan  
- EMI Free Loan  
- Personal Overdraft  
- Advance Salary Loan  

This case study focuses **only on the underwriting process for Personal Loans**.

---

## Business Problem
The data science team at LoanTap is developing an underwriting layer to assess the **creditworthiness of individuals**.

### Objective:
Given a set of attributes for an individual:
- Determine whether a **credit line should be extended**
- Recommend appropriate **repayment terms**
- Minimize default risk while maximizing lending opportunities

The target variable is **loan_status**, indicating whether a loan is performing or defaulted.

---

## Dataset
**File:** `LoanTapData.csv`

The dataset contains borrower-level information related to income, employment, credit history, and loan characteristics.

---

## Data Dictionary (Key Variables)
- **loan_amnt**: Loan amount applied for  
- **term**: Loan term (36 or 60 months)  
- **int_rate**: Interest rate  
- **installment**: Monthly payment  
- **grade / sub_grade**: LoanTap credit grading  
- **emp_title**: Borrower job title  
- **emp_length**: Employment length (0–10 years)  
- **home_ownership**: Home ownership status  
- **annual_inc**: Annual income  
- **verification_status**: Income verification status  
- **issue_d**: Loan issue month  
- **loan_status**: Loan outcome (Target Variable)  
- **purpose**: Loan purpose  
- **dti**: Debt-to-income ratio  
- **open_acc / total_acc**: Credit line information  
- **revol_bal / revol_util**: Revolving credit usage  
- **pub_rec / pub_rec_bankruptcies**: Public record indicators  
- **mort_acc**: Mortgage accounts  
- **application_type**: Individual or joint application  

---

## Analysis Approach

### Exploratory Data Analysis (EDA)
- Dataset structure and summary statistics
- Distribution of loan status
- Relationship between target variable and predictors
- Visual analysis using count plots, box plots, and heatmaps
- Correlation analysis among numerical features

---

### Feature Engineering
- Creation of binary risk flags:
  - `pub_rec_flag`
  - `mort_acc_flag`
  - `pub_rec_bankruptcies_flag`
- Handling missing values
- Outlier detection and treatment
- Feature scaling using StandardScaler / MinMaxScaler

---

## Modeling
- Logistic Regression for default prediction
- Model interpretability and coefficient analysis
- Probability-based risk assessment

---

## Model Evaluation
- Classification Report (Precision, Recall, F1-score)
- ROC-AUC Curve
- Precision-Recall Curve
- Threshold tuning and tradeoff analysis

---

## Precision vs Recall Tradeoff
Special focus is given to:
- Minimizing **false negatives** (missing actual defaulters)
- Balancing business risk (NPA) with lending opportunities
- Choosing thresholds that align with conservative lending strategies

---

## Key Insights
- Certain credit attributes strongly influence default risk
- Income, debt burden, and credit utilization are major predictors
- Binary risk flags help simplify underwriting decisions
- Precision-recall balance is critical in loan approval systems

---

## Business Recommendations
- Apply stricter approval criteria for high-risk segments
- Use probability thresholds instead of fixed rules
- Prioritize recall for defaulter detection to reduce NPAs
- Customize repayment terms based on risk score
- Combine model predictions with business judgment

---

## Tools & Technologies
- Python  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- Logistic Regression  
- Statistical Evaluation Metrics  
