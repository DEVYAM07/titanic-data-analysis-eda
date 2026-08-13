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

3️⃣ Summary Statistics

->Calculates summary statistics (mean, median, standard deviation, quartiles) for continuous columns.

->Measures distribution shape and skewness for passenger age.

```
# Descriptive statistics and skewness calculation for age
df['Age'].describe()
df['Age'].skew()
```

4️⃣ Visual Analysis

->Plots continuous variables using histograms and Kernel Density Estimation (KDE) curves.

->Examines distribution spread and detects age ranges across passengers (0.42 to 80 years).

```
# Age distribution plots
df['Age'].plot(kind='hist', bins=20)
df['Age'].plot(kind='kde')
```

## 📊 Datasets & Schema

| Dataset | Records | Description | Primary Key | Key Features |
| :--- | :---: | :--- | :--- | :--- |
| **`train.csv`** | 891 | Historical passenger manifest and survival records | `PassengerId` | `Survived`, `Pclass`, `Sex`, `Age`, `Fare`, `Embarked` |
| **`test.csv`** | 418 | Historical passenger manifest for testing model predictions | `PassengerId` | `Survived`, `Pclass`, `Sex`, `Age`, `Fare`, `Embarked` |


💡 Key Insights Discovered

->Age Distribution: Passenger age in train.csv follows an approximately normal distribution with a slight right skew (skewness ≈ 0.389) and a median age of 28.0 years (mean of ~29.7 years).

->Missing Values: train.csv exhibits a ~19.8% missing value rate in the Age column, which means handling or imputing missing data will be necessary before building predictive machine learning models.

🚀 How to Run

1. Clone the Repository

```
git clone https://github.com/DEVYAM07/titanic-data-analysis-eda.git
cd titanic-data-analysis-eda
```

2. Install Dependencies

```
pip install pandas numpy matplotlib seaborn jupyter
```

3. Launch Notebook Pipeline

```
jupyter notebook notebooks/Titanic_Data_Analysis.ipynb
```

🧰 Tech Stack

Language: Python 3.8+

Data Manipulation: pandas, numpy

Visualization: matplotlib, seaborn

Thanks for checking out this project! Feel free to star ⭐️ the repository if you found it helpful!
