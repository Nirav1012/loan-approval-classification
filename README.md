# Loan Approval Model Classification
### project setup : 
1) create virtual environment : 
```
python -m venv myenv
```

2) activate virtual environment
```
myvenv\scripts\activate
```

3) insatll dependencies:
```
pip install -r requirements.txt
'''

### About Dataset

1. Data Source
This dataset is a synthetic version inspired by the original Credit Risk dataset on Kaggle and enriched with additional variables based on Financial Risk for Loan Approval data. SMOTENC was used to simulate new data points to enlarge the instances. The dataset is structured for both categorical and continuous features.

2. Metadata
The dataset contains 45,000 records and 14 variables, each described below:


# 🏦 Loan Approval Classification

A machine learning web app that predicts whether a loan application will be **approved** or **rejected** based on the applicant's personal, financial, and credit details. The trained model is served through an interactive [Streamlit](https://streamlit.io/) interface.

---

## 📌 Features

- Interactive UI to enter applicant and loan details
- Instant prediction: **Loan Approved** ✅ or **Loan Rejected** ❌
- Pre-trained scikit-learn pipeline (preprocessing + model in a single pickle file)
- Input options (gender, education, etc.) loaded dynamically from the dataset

---

## 🗂️ Project Structure

```
├── app.py                          # Streamlit application
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation
├── assets/
│   └── AI-Powered Loan Approval.png   # App icon / sidebar image
├── best_model/
│   └── best_model_pipeline.pkl     # Trained model pipeline
└── datasets/
    └── cleaned_data.csv            # Cleaned dataset
```

---

## ⚙️ Project Setup

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <project-folder>
```

### 2. Create a virtual environment

```bash
python -m venv myenv
```

### 3. Activate the virtual environment

**Windows**
```bash
myenv\Scripts\activate
```

```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the app

```bash
streamlit run app.py
```

The app will open in your browser at `http://localhost:8501`.

---

## 📊 About the Dataset

### 1. Data Source

This dataset is a synthetic version inspired by the original [Credit Risk dataset on Kaggle](https://www.kaggle.com/) and enriched with additional variables based on *Financial Risk for Loan Approval* data. **SMOTENC** was used to simulate new data points and enlarge the number of instances. The dataset contains both categorical and continuous features.

### 2. Metadata

The dataset contains **45,000 records** and **14 variables**:

| Column | Type | Description |
|---|---|---|
| `person_age` | Numeric | Age of the applicant |
| `person_gender` | Categorical | Gender of the applicant |
| `person_education` | Categorical | Highest education level |
| `person_income` | Numeric | Annual income |
| `person_emp_exp` | Numeric | Years of employment experience |
| `person_home_ownership` | Categorical | Home ownership status (e.g. rent, own, mortgage) |
| `loan_amnt` | Numeric | Loan amount requested |
| `loan_intent` | Categorical | Purpose of the loan |
| `loan_int_rate` | Numeric | Loan interest rate |
| `loan_percent_income` | Numeric | Loan amount as a fraction of annual income |
| `cb_person_cred_hist_length` | Numeric | Length of credit history (years) |
| `credit_score` | Numeric | Credit score of the applicant |
| `previous_loan_defaults_on_file` | Categorical | Whether the applicant has previously defaulted |
| `loan_status` | Target | Loan outcome: `1` = approved, `0` = rejected |

---

## 🤖 Model

- **Task:** Binary classification (loan approved / rejected)
- **Model:** _<add model name, e.g. Random Forest / XGBoost / Logistic Regression>_
- **Pipeline:** Preprocessing (encoding / scaling) and the classifier are bundled in a single scikit-learn `Pipeline`, saved at `best_model/best_model_pipeline.pkl`
- **Performance:** _<add accuracy / precision / recall / F1 / ROC-AUC>_

---

## 🖥️ How to Use the App

1. Adjust the sliders and dropdowns for applicant details (age, income, experience, loan amount, credit score, interest rate, etc.).
2. Click **Predict Loan**.
3. The result appears as **Loan Approved** (green) or **Loan Rejected** (red).

---

## 🛠️ Tech Stack

- **Python**
- **Pandas**, **NumPy** – data handling
- **Matplotlib**, **Seaborn** – data visualization / EDA
- **scikit-learn** – model building and pipeline
- **Streamlit** – web interface

---


