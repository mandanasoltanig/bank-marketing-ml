# 📊 Bank Marketing Machine Learning Project

## 📌 Project Overview

This project predicts whether a client will subscribe to a **bank term deposit** after a direct marketing campaign. Using the UCI Bank Marketing dataset, the objective is to build a machine learning model that helps banks identify customers who are most likely to subscribe **before making a phone call**, allowing marketing teams to prioritize leads and reduce unnecessary outreach.

This project follows the complete machine learning pipeline, including:

- Data acquisition
- Data cleaning
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model development
- Hyperparameter tuning
- Model evaluation
- Business recommendations

---

## 🎯 Business Problem

Bank telemarketing campaigns are expensive and time-consuming. Since only a small percentage of customers subscribe to a term deposit, contacting every customer is inefficient.

The goal of this project is to develop a predictive model that estimates the probability of subscription before the marketing call takes place.

---

## 📂 Dataset

**Source:** UCI Bank Marketing Dataset

https://archive.ics.uci.edu/ml/datasets/bank+marketing

The dataset contains over **41,000 customer records** collected during direct marketing campaigns conducted by a Portuguese banking institution.

### Target Variable

- **y**
  - yes → Client subscribed to a term deposit
  - no → Client did not subscribe

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)

---

## 📋 Project Workflow

### Phase 1 – Data Collection

- Loaded the Bank Marketing dataset
- Explored dataset structure
- Identified missing values and data types

---

### Phase 2 – Data Preparation

Performed:

- Data cleaning
- Duplicate removal
- Outlier treatment
- Feature engineering
- Encoding categorical variables
- Scaling numerical features
- Train/Test Split

Special handling included:

- Keeping **"unknown"** values as valid categories
- Removing the **duration** feature to avoid data leakage since call duration is only known after the marketing call.

---

### Phase 3 – Exploratory Data Analysis

Key analyses included:

- Customer demographics
- Job distribution
- Age distribution
- Previous campaign outcomes
- Subscription rates
- Correlation analysis
- Class imbalance visualization

The dataset is highly imbalanced, with approximately **11% positive subscriptions**.

---

### Phase 4 – Machine Learning Models

The following models were trained and compared:

- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

To address class imbalance:

- SMOTE oversampling
- Class weighting

Hyperparameters were optimized using:

- GridSearchCV
- Cross Validation

---

## 📊 Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Since the dataset is imbalanced, **ROC-AUC**, **Recall**, and **F1-score** were considered more informative than Accuracy.

---

## 🏆 Best Model

After comparing all models, the **Random Forest** achieved the best overall performance with the highest ROC-AUC while maintaining a good balance between precision and recall.

The model was selected because it provides strong predictive performance using only information available before contacting the customer.

---

## 🔍 Important Features

Some of the most influential predictors include:

- Previous campaign outcome (`poutcome`)
- Euribor interest rate (`euribor3m`)
- Number of employees (`nr.employed`)
- Employment variation rate (`emp.var.rate`)
- Contact month
- Contact type

---

## 💼 Business Recommendations

- Score customers before launching marketing campaigns.
- Prioritize customers with the highest predicted probability of subscribing.
- Reduce unnecessary calls.
- Improve campaign efficiency.
- Retrain the model periodically since economic conditions change over time.

---

##  Links

Dataset
https://archive.ics.uci.edu/dataset/222/bank+marketing

Trello Board
https://trello.com/b/mfdeqxJ9/bank-marketing-ml

Presentation Slides
https://docs.google.com/presentation/d/1jcmEA6DmcRl6FrhXfdr7luhoKM5p9xzn/edit?usp=sharing&ouid=101958444504053526965&rtpof=true&sd=true

GitHub Repository
https://github.com/mandanasoltanig/bank-marketing-ml
