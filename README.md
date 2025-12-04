# 📊 Credit Score & Loan Default Analysis

This project involves an exploratory data analysis (EDA) of a financial dataset containing details about loan applicants. The goal is to analyze various factors—such as income, age, loan amount, and credit history—to understand their relationship with loan status and credit risk.

## 📂 Project Overview

The notebook processes a dataset of **32,581 records** and performs data cleaning, univariate analysis, and bivariate analysis to derive actionable insights regarding creditworthiness.

### Key Objectives
* Clean and preprocess raw financial data.
* Analyze the distribution of individual features (Univariate Analysis).
* Investigate the relationship between applicant features and loan defaults (Bivariate Analysis).
* Visualize correlations between numerical variables.

## 🛠️ Technologies Used
* **Python**
* **Pandas** (Data manipulation and cleaning)
* **Matplotlib & Seaborn** (Data visualization: Boxplots, Histograms, Heatmaps)

## 📄 Dataset Details

The dataset contains **12 columns** representing applicant demographics and loan details:

| Column | Description |
| :--- | :--- |
| `person_age` | Age of the applicant |
| `person_income` | Annual income of the applicant |
| `person_home_ownership` | Home ownership status (Rent, Mortgage, Own, Other) |
| `person_emp_length` | Employment length in years |
| `loan_intent` | Purpose of the loan (Education, Medical, Venture, etc.) |
| `loan_grade` | Loan grade classification (A, B, C, D, etc.) |
| `loan_amnt` | Loan amount requested |
| `loan_int_rate` | Interest rate on the loan |
| `loan_status` | Loan status (0 = Non-default, 1 = Default) |
| `loan_percent_income` | Percentage of income dedicated to the loan |
| `cb_person_default_on_file`| Historical default status (Y/N) |
| `cb_person_cred_hist_length`| Length of credit history in years |

## ⚙️ Analysis Workflow

1.  **Data Loading & Inspection:**
    * Loaded data from CSV.
    * Inspected data types and shape (32,581 rows, 12 columns).
2.  **Data Cleaning:**
    * Identified missing values in `person_emp_length` and `loan_int_rate`.
    * **Imputation:** Filled missing `person_emp_length` with the **median** and `loan_int_rate` with the **mean**.
3.  **Univariate Analysis:**
    * Analyzed distributions of age, income, and loan amounts using histograms and boxplots.
    * Examined categorical counts for home ownership, loan intent, and loan grades.
4.  **Bivariate Analysis:**
    * Compared features against `loan_status` to identify risk factors.
    * Generated correlation heatmaps.

## 💡 Key Insights from Analysis

* **Home Ownership:** Applicants who **RENT** their homes show a higher frequency of loan defaults compared to those who own or have a mortgage.
* **Loan Intent:** "Debt Consolidation" and "Medical" loans tend to have higher default rates.
* **Interest Rates:** Higher interest rates are strongly associated with higher default rates.
* **Loan-to-Income Ratio:** A higher `loan_percent_income` is a significant indicator of default risk.
* **Age:** Most applicants are between 20-35 years old.
* **Income:** Higher income generally correlates with lower default risk.

## 🚀 How to Run

1.  Clone the repository.
2.  Ensure the dataset is located at the specified path (or update the `PATH` variable in the notebook).
3.  Install dependencies:
    ```bash
    pip install pandas matplotlib seaborn
    ```
4.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook credit_score.ipynb
    ```
