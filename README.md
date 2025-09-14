# LoanTap Creditworthiness Analysis

## Project Overview
This project builds an **underwriting layer** for LoanTap, an online platform offering customized loan products.  
The goal is to determine whether a **personal loan** should be extended to an individual and recommend suitable repayment terms.  

We use **Logistic Regression** for classification, focusing on identifying real defaulters while minimizing false positives, ensuring loans are disbursed only to creditworthy individuals.

---

## 📂 Dataset
The dataset `LoanTapData.csv` contains attributes related to loan applicants’ financial and credit history.  
The **target variable** is `loan_status`, which indicates the current status of the loan.  

🔗 [Dataset Link](https://drive.google.com/file/d/1eAtX-82fumeQq-M0CdORJCowjLykNQDO/view?usp=drive_link)

### Key Features
- `loan_amnt`: Loan amount applied for  
- `term`: Duration of loan (36 or 60 months)  
- `int_rate`: Interest rate on the loan  
- `installment`: Monthly payment owed if loan is approved  
- `grade` & `sub_grade`: LoanTap-assigned risk grades  
- `emp_title`, `emp_length`: Job title & employment length  
- `home_ownership`: Borrower’s housing status  
- `annual_inc`: Annual income  
- `verification_status`: Whether income was verified  
- `dti`: Debt-to-income ratio  
- `earliest_cr_line`: Date of earliest credit line  
- `open_acc`, `total_acc`: Number of open & total accounts  
- `revol_bal`, `revol_util`: Revolving balance & utilization  
- `mort_acc`: Mortgage accounts  
- `pub_rec`, `pub_rec_bankruptcies`: Public derogatory records  
- `application_type`: Individual or joint application  
- `loan_status`: Target variable – loan outcome  

---

## 🛠 Conceptual Approach

### 1. Exploratory Data Analysis (EDA)
- Checked dataset structure, missing values, and outliers  
- Visualized relationships using **count plots, box plots, and heatmaps**  
- Analyzed correlations among independent variables  

### 2. Feature Engineering
- Created binary flag features (`pub_rec`, `mort_acc`, `pub_rec_bankruptcies`)  
- Encoded categorical variables for modeling  

### 3. Missing Value & Outlier Treatment
- Imputed missing values with appropriate strategies  
- Handled extreme outliers  

### 4. Scaling
- Normalized numerical features using **MinMaxScaler / StandardScaler**  

### 5. Modeling
- Logistic Regression as baseline predictive model  
- Evaluated with:  
  - **Classification Report** (Precision, Recall, F1-Score, Accuracy)  
  - **ROC-AUC Curve**  
  - **Precision-Recall Curve**  

---

## ⚖️ Tradeoff Challenges
- **Minimizing False Positives** → Prevents disbursing loans to risky applicants, reducing NPAs  
- **Precision vs Recall** → Balanced to identify true defaulters while maintaining approval rates  

---

## ✨ Business Impact
This project provides a **data-driven underwriting system** that helps LoanTap:  
✔ Reduce defaults and non-performing assets (NPAs)  
✔ Improve lending efficiency  
✔ Support better risk-based decision-making  

---
