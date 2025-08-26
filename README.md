Credit Card Fraud Detection

This project implements a **machine learning pipeline** to detect fraudulent credit card transactions using a synthetic dataset. The goal is to classify transactions as **fraudulent** or **legitimate** while addressing the challenges of data imbalance.

Project Overview

Credit card fraud is a major issue in the financial industry, causing billions in losses annually. Detecting fraud early helps reduce losses and protect customers.  

This project builds a **foundational fraud detection model** using Python and popular data science libraries.

Dataset

The dataset is **synthetically generated** to simulate real-world transactions for learning purposes.

Columns:
- `TransactionID` — Unique identifier for each transaction  
- `TransactionDate` — Date of transaction  
- `Amount` — Transaction amount (in currency)  
- `TransactionType` — Type: *Payment, Withdrawal, Purchase*  
- `IsFraud` — Label (1 = Fraud, 0 = Legitimate)  


Project Components

Data Preprocessing
- Convert timestamps to datetime  
- Extract time-based features (day of week, day of month)  
- One-hot encode categorical variables  
- Normalize transaction amount  
- Handle missing values  

Model Training
- Split data into **train (80%)** and **test (20%)**  
- Train a **Random Forest Classifier**  
- Evaluate with **Accuracy, Precision, Recall, F1-score**  

Imbalance Handling
Fraud detection faces **class imbalance** (very few fraud cases). Techniques used:  
- Class weighting in Random Forest  
- **SMOTE (Synthetic Minority Oversampling Technique)**  

Results Summary
- **Basic Random Forest**: High accuracy but poor fraud detection (bias towards majority class).  
- **With Class Weights**: Limited improvement.  
- **With SMOTE Oversampling**: Better recall for fraud detection, but more false positives.  

Key takeaway: **Handling class imbalance is critical in fraud detection.**

Technologies Used
- **Python 3.x**  
- **Pandas, NumPy** (data processing)  
- **Scikit-learn** (ML models & evaluation)  
- **Imbalanced-learn (SMOTE)** (imbalance handling)  
- **Matplotlib, Seaborn** (visualization)  
