Student Name: **Samar M. Balousha**

Academic Number: **2320222601**

   **Pattern Recogniction Course**

   **Intelligence Systems & Computer Engineering**

   **Al-Aqsa University**

---

# 🍷 Wine Quality Classification using SVM and XGBoost

This repository contains the implementation of supervised learning classifiers for the **Wine Quality Dataset** as part of the *Pattern Recognition (ENGS3302)* course at Al-Aqsa University.

The project focuses on classifying wine quality based on physicochemical features using **Support Vector Machines (SVM)** and **XGBoost**, with an emphasis on understanding margin-based classifiers and ensemble learning methods.

---

## Project Objectives

* Apply supervised machine learning techniques to a real-world dataset
* Compare **Hard Margin SVM**, **Soft Margin SVM**, and **XGBoost**
* Analyze the impact of margin flexibility on classification performance
* Evaluate models using appropriate performance metrics

---

## Dataset

* Source: UCI Machine Learning Repository – Wine Quality Dataset
* Two datasets were used:

  * Red Wine
  * White Wine
* The datasets were merged, and a new feature **Type** was added:

  * Red = 1
  * White = 0

### Target Definition

Wine quality was converted into a binary classification problem:

* **Good (1):** Quality ≥ 6
* **Not Good (0):** Quality < 6

Rare quality scores (3 and 9) were removed to reduce noise.

---

## Exploratory Data Analysis (EDA)

EDA was performed to understand the data distribution and relationships:

* Analysis of class imbalance

  <img width="834" height="573" alt="Screenshot 2026-02-08 103505" src="https://github.com/user-attachments/assets/f5a9894a-1322-4580-9af1-72a588b114ee" />

* Detection of outliers using box plots

  <img width="1324" height="433" alt="Screenshot 2026-02-08 103613" src="https://github.com/user-attachments/assets/7966c94d-9ff2-4d3f-908d-6cfe26f244e0" />

* Correlation analysis between features and wine quality
   <img width="764" height="660" alt="Screenshot 2026-02-08 103701" src="https://github.com/user-attachments/assets/1d32984c-fd33-4dd7-8664-718a61978b2c" />

---

## Models Implemented

### 1. Hard Margin SVM

* High penalty parameter (C = 100)
* Assumes perfectly separable data
* Sensitive to noise and outliers

### 2. Soft Margin SVM

* Penalty parameter (C = 1.0)
* Uses RBF kernel to model non-linear boundaries
* More suitable for real-world data

### 3. XGBoost Classifier

* Gradient boosting ensemble method
* Captures complex feature interactions
* Provides strong performance on imbalanced and noisy datasets

---

## Model Evaluation

Models were evaluated using:

<img width="571" height="209" alt="Screenshot 2026-02-08 112052" src="https://github.com/user-attachments/assets/8714845e-228e-46c6-8e6e-8f5f3fd9c262" />

* Accuracy
* F1-Score
* ROC Curve and AUC
<img width="733" height="741" alt="Screenshot 2026-02-08 112347" src="https://github.com/user-attachments/assets/e61b307e-5aa7-4471-963f-5c301aa53b07" />


XGBoost achieved the highest overall performance, followed by Soft Margin SVM.

---

## Requirements

* Python 3.x
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn (SVC, StandardScaler, train_test_split)
* XGBoost

---


