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
Note: Dataset is not included in the repository due to Kaggle terms of use.

# 🔍 Key Approaches Used
## 1️⃣ Exploratory Data Analysis

Checked missing values

Plotted distributions

Correlation matrix

Session-level analysis

User-level aggregation


