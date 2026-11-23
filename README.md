# Loan Approval Prediction – Machine Learning Classification

A beginner-friendly end-to-end machine learning classification project that predicts whether a customer's loan is approved or rejected using customer and financial features.

## Project Overview

- **Problem type:** Binary classification
- **Use case:** Customer loan approval prediction
- **Target column:** `Loan_Approved`
  - `1` = Approved
  - `0` = Rejected
- **Model:** Logistic Regression

## Workflow

1. Load the loan approval dataset using Pandas.
2. Inspect the dataset and identify missing values.
3. Handle missing values:
   - `Income`: fill missing values with the median.
   - `Employment_Type`: fill missing values with the mode.
4. Encode the `Employment_Type` categorical feature using `LabelEncoder`.
5. Separate features (`X`) and target (`y`).
6. Split the data into training and testing sets (80% / 20%).
7. Train a Logistic Regression classifier.
8. Evaluate predictions using accuracy, a classification report, and a confusion matrix.

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository Structure

```text
loan-approval-classification/
│
├── loan_approval_classification.ipynb
├── loan_approval_1000.csv
├── requirements.txt
├── README.md
├── DATASET_REQUIRED.txt
└── .gitignore
```

> The CSV is a required input file and was not included with the uploaded notebook. Add your `loan_approval_1000.csv` file to the project root (the same folder as the notebook) before running it. Do not upload private or confidential customer data.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/loan-approval-classification.git
cd loan-approval-classification
```

### 2. Create and activate a virtual environment (recommended)

**Windows PowerShell**
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Add the dataset

Place `loan_approval_1000.csv` in the repository root. The notebook expects this exact filename and reads it with:

```python
df = pd.read_csv("loan_approval_1000.csv")
```

The notebook uses the columns `Income`, `Employment_Type`, and `Loan_Approved`. Make sure your CSV contains these columns and that `Loan_Approved` contains the binary labels `0` and `1`.

### 5. Run the notebook

```bash
jupyter notebook
```

Open `loan_approval_classification.ipynb` and run the cells from top to bottom.

## Evaluation

The notebook reports:
- Accuracy score
- Precision, recall, and F1-score (classification report)
- Confusion matrix

Actual evaluation values depend on the dataset used. No performance result is claimed in this README.

## Important Note

This is an educational machine learning demonstration, not a production-ready loan decision system. Real lending decisions require careful validation, fairness testing, explainability, privacy safeguards, and compliance with applicable regulations.

## Author

**Akthar Ahamed**

