# CreditWise – Loan Approval Prediction System

## 📌 Overview

CreditWise is a Machine Learning project that predicts whether a loan application should be **Approved** or **Rejected** based on an applicant's financial, employment, and personal information. It's built for **SecureTrust Bank**, a mid-sized financial company offering personal and home loans across urban and rural regions of India, to help replace a slow, inconsistent manual verification process with a faster, data-driven one.

---

## 🎯 Problem Statement

SecureTrust Bank currently relies on loan officers manually checking income proofs, employment details, and credit history for every application. This process is time-consuming, biased, and inconsistent, and it leads to two costly mistakes:

1. **Good customers sometimes get rejected** → lost business.
2. **High-risk customers sometimes get approved** → financial losses.

This project builds an intelligent loan approval system that learns patterns from historical applicant data and predicts loan approval automatically, before final human verification.

---

## 🚀 Features

- Data Cleaning & Missing Value Imputation
- Exploratory Data Analysis (EDA)
- Correlation Analysis & Heatmap
- Categorical Encoding (Label Encoding + One-Hot Encoding)
- Feature Scaling (StandardScaler)
- Feature Engineering
- Multiple Machine Learning Models
- Model Performance Comparison

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📊 Dataset

The dataset (`loan_approval_data.csv`) contains **1,000 loan applications** with **20 columns**. Each row represents one applicant.

| Column | Description |
|---|---|
| Applicant_ID | Unique applicant ID |
| Applicant_Income | Monthly income of applicant |
| Coapplicant_Income | Monthly income of co-applicant |
| Employment_Status | Salaried / Self-Employed / Business |
| Age | Applicant age |
| Marital_Status | Married / Single |
| Dependents | Number of dependents |
| Credit_Score | Credit bureau score |
| Existing_Loans | Number of already running loans |
| DTI_Ratio | Debt-to-Income ratio |
| Savings | Savings balance |
| Collateral_Value | Value of collateral provided |
| Loan_Amount | Loan amount requested |
| Loan_Term | Loan duration (months) |
| Loan_Purpose | Home / Education / Personal / Business |
| Property_Area | Urban / Semi-Urban / Rural |
| Education_Level | Graduate / Postgraduate / Undergraduate |
| Gender | Male / Female |
| Employer_Category | Govt / Private / Self |
| **Loan_Approved (Target)** | Yes = Approved, No = Rejected |

The target classes are imbalanced: roughly **65% Rejected** vs **30% Approved** in the raw data.

---

## 🧹 Preprocessing Pipeline

1. **Missing values** — numerical columns imputed with the mean, categorical columns imputed with the most frequent value.
2. **EDA** — class balance, income/credit score distributions, boxplots of key features against loan approval.
3. **Dropped** `Applicant_ID` (not predictive).
4. **Encoding**:
   - `Education_Level` and `Loan_Approved` → Label Encoding
   - `Employment_Status`, `Marital_Status`, `Loan_Purpose`, `Property_Area`, `Gender`, `Employer_Category` → One-Hot Encoding (drop first)
5. **Train/Test Split** — 80/20 split (`random_state=42`).
6. **Feature Scaling** — `StandardScaler` applied to numerical features.

---

## 🤖 Machine Learning Models Used

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes (GaussianNB)

---

## 📈 Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|--------|---------:|----------:|-------:|----------:|
| **Logistic Regression** | **88.0%** | 78.46% | **83.61%** | **80.95%** |
| KNN | 78.5% | 67.31% | 57.38% | 61.95% |
| Naive Bayes | 86.0% | **81.13%** | 70.49% | 75.44% |

- **Best overall model (Accuracy & F1):** Logistic Regression
- **Best model by Precision:** Naive Bayes


---

## ▶️ How to Run

1. Clone the repository
2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. Open the notebook

```bash
jupyter notebook Credit_wise.ipynb
```

---

## 📌 Future Improvements

- Hyperparameter Tuning (GridSearchCV / RandomizedSearchCV)
- Cross Validation
- Handle class imbalance (SMOTE / class weighting)
- Ensemble Learning Models (Random Forest, XGBoost)
- Deployment using Flask or Streamlit

---

## 👨‍💻 Author

Tushar Thorat

LinkedIn: *(Add your LinkedIn URL here)*

GitHub: *(Add your GitHub URL here)*
