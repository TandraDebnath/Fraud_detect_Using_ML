Credit Card Fraud Detection
This project implements a simple machine learning pipeline to detect fraudulent credit card transactions. It uses a synthetic dataset mimicking real-world transaction records with the goal of classifying transactions as fraudulent or non-fraudulent.

Project Overview
Credit card fraud is a serious issue in the financial industry, causing billions of dollars in losses annually. Detecting fraudulent transactions early is crucial for reducing these losses and protecting customers.

This project builds a foundational fraud detection model using Python and popular data science libraries. The dataset contains features such as transaction amount, type, and date, with labels identifying fraudulent transactions.

Dataset
The dataset used in this project is synthetically created by me to simulate credit card transactions for fraud detection learning purposes.


Columns:

TransactionID — Unique identifier for each transaction.

TransactionDate — Date the transaction occurred.

Amount — Transaction amount in currency.

TransactionType — Type of transaction: Payment, Withdrawal, or Purchase.

IsFraud — Label where 1 indicates fraud and 0 indicates legitimate transaction.

Project Components
Data Preprocessing

Convert transaction timestamps to datetime objects.

Extract additional time-based features (day of week, day of month).

Encode categorical variables with one-hot encoding.

Normalize the transaction amount feature.

Check for and handle missing values.

Model Training

Split data into training and test sets (80-20).

Train a Random Forest classifier to detect fraud.

Evaluate model performance using accuracy, precision, recall, and F1-score.


Imbalance Handling

Apply techniques to handle the severe fraud class imbalance:

Class weighting in Random Forest.

Synthetic Minority Over-sampling Technique (SMOTE).


Results Summary
Basic Random Forest achieved high overall accuracy but failed to detect fraud due to class imbalance.

Using class weights alone did not improve fraud detection significantly.

Applying SMOTE oversampling increased fraud detection recall but also produced more false positives.

The project shows the importance of addressing data imbalance in fraud detection.


Technologies Used
Python 3.x

Pandas, NumPy

Scikit-learn

Imbalanced-learn (SMOTE)

Matplotlib/Seaborn (optional for visualization)



