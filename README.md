🚢 Titanic Data Analysis & Profiling Pipeline

Welcome! 👋 This repository contains a practical exploratory data analysis (EDA) of the Titanic passenger dataset. The project focuses on checking data quality, analyzing missing values, classifying features, and exploring passenger demographics using Python, pandas, and data visualization tools.

## 📁 Repository Structure
```
.
├── data/
│   ├── train.csv                        # Historical Titanic training dataset (891 records)
│   └── test.csv                         # Titanic testing dataset
├── notebooks/
│   └── Titanic_Data_Analysis.ipynb      # End-to-end data analysis notebook
└── README.md                            # Project documentation

```

🛠️ How the Pipeline Works

The workflow is organized into four sequential steps inside Titanic_Data_Analysis.ipynb:

```
┌───────────────────────────┐      ┌───────────────────────────┐
│ 1. Data Assessment        │ ──> │ 2. Column Classification  │
│ Check Records & Nulls     │      │ Numerical & Categorical   │
└───────────────────────────┘      └───────────────────────────┘
                                                 │
                                                 ▼
┌───────────────────────────┐      ┌───────────────────────────┐
│ 4. Visual Analysis        │ <── │ 3. Summary Statistics     │
│ Histograms & Density Plots│      │ Mean, Median & Skewness   │
└───────────────────────────┘      └───────────────────────────┘

```

1️⃣ Data Assessment & Inspection

->Record Count: Inspects 891 passenger records in train.csv across 12 attributes.

->Missing Data: Identifies missing values specifically in train.csv, including ~19.8% missing values in the Age column (177 missing entries out of 891 records).

->Data Audit: Checks data types and summary statistics across available features.

2️⃣ Column Classification

Categorizes features into distinct variable types:

```
# Column Type Classification
numerical_cols = ['Age', 'Fare', 'PassengerId']
categorical_cols = ['Survived', 'Pclass', 'Sex', 'SibSp', 'Parch', 'Embarked']
mixed_cols = ['Name', 'Ticket', 'Cabin']
```
