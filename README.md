# 📘 Purchase Value Prediction from Multi-Session User Behavior
IIT Madras BS in Data Science – Machine Learning Project

This project was completed as part of the Data Science & Machine Learning coursework at IIT Madras, and submitted on Kaggle.
The objective is to predict a customer’s purchase value based on their digital behavior across multiple sessions.

# 🚀 Project Overview

Modern e-commerce platforms collect large volumes of user interaction data—session activity, devices, traffic sources, clicks, and more.
The goal of this competition is to model customer intent and predict the final purchase amount they might spend.

This project builds a complete ML pipeline including:

Exploratory Data Analysis (EDA)

Data cleaning & preprocessing

Feature engineering (categorical encodings, numerical transformations)

Handling multi-session data

Zero-inflated target modeling

Two-stage prediction architecture

Model evaluation and submission generation

# 🎯 Problem Statement

For each customer ID in the test set, predict:
purchaseValue (continuous target)
The competition uses R² score as the official evaluation metric.

# 📂 Repository Structure
```bash
├── data/
│   ├── external/         # Documentation, data dictionary, kaggle link
│   └── raw/              # Raw data (Training & Test Csv's)
│
├── notebooks/
│   └── main_notebook.ipynb   # Full Kaggle notebook used in the project
│
├── src/
│   ├── utils/                # Helper scripts
│   └── modeling/             # Model code 
│
├── reports/
│   └── figures/              # EDA charts, model plots
│
├── .gitignore
├── README.md
└── LICENSE
```
Note: Dataset is not included in the repository due to Kaggle terms of use.

# 🔍 Key Approaches Used
## 1️⃣ Exploratory Data Analysis

Checked missing values

Plotted distributions

Correlation matrix

Session-level analysis

User-level aggregation

## 2️⃣ Preprocessing

Handled missing values

Min-max scaling for continuous features

Frequency-based encoding for categorical features

Rank encoding & target encoding for high-cardinality features

PCA for dimensionality reduction

## 🧠 Model
This project was a regression model, the goal of this was to try out 3 models and create the submission on the best model.

Models tested:
1. XGBOOST Regeressor
2. LightGBM Regressor
3. RandomForest Regressor

This project uses a regression-based approach to predict the continuous target variable purchaseValue.

Initially, multiple methods were explored to address the zero-inflation problem (Since ≈80% of users had purchaseValue = 0):

| Method Tried            | Description                                                                          | Result               |
| ----------------------- | ------------------------------------------------------------------------------------ | -------------------- |
| Log transform on target | Applied log(1 + purchaseValue) to normalize skew and reduce zero-inflation           | **Best performance** |

## 🔍 Approach

The log-transformed regression method delivered the highest R² score on the validation set.

The target was transformed as:

y_log = log(1 + purchaseValue)

After prediction, the exponential inverse transform was applied:

purchaseValue = exp(y_log_pred) - 1

## 🤖 Models Evaluated

| Model                                     | Notes                                            |
| ----------------------------------------- | ------------------------------------------------ |
| XGBoost Regressor                         | Performed well but prone to overfitting          |
| LightGBM Regressor                        | Competitive score, fast training                 |
| **RandomForest Regressor (Final Choice)** | **Best performance with log-transformed target** |

## 🏁 Final Result

The RandomForest Regressor trained on the log-transformed target generated the highest public test score and was used to produce the final Kaggle submission.

## 💡 What I Learned

This project helped me strengthen skills in:

End-to-end ML pipeline design

Working with large behavioral datasets

Handling zero-inflated regression

Best practices for Kaggle competitions

Feature engineering & advanced encodings

Model tuning & evaluation

## 🛠 Tech Stack

Python

Pandas, NumPy

Scikit-learn

LightGBM

Matplotlib / Seaborn

Kaggle Notebooks

## 📎 Links

🔗 **Kaggle Project Page:** [Notebook Link](https://www.kaggle.com/code/rahulvenu13/23ds1000053-notebook-t22025/)
🔗 **Competition Link:** [Kaggle Competition](https://www.kaggle.com/competitions/engage-2-value-from-clicks-to-conversions)

## 🤝 Contact

If you’d like to discuss this project or opportunities:

Rahul Venu
<p>
📧 <a href="mailto:rahulvenuklr@gmail.com?subject=Project%20Inquiry&body=Hello%20Rahul,">Email</a>
💼 <a href="https://www.linkedin.com/in/rahulvs13/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
🐙 <a href="https://github.com/rahul-venu" target="_blank" rel="noopener noreferrer">GitHub</a>
</p>








