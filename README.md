# Student Mental Health Prediction

## Project Overview
This Machine Learning project predicts whether a student is likely to have Depression, Anxiety, or Panic Attacks based on their demographic and academic data.

## Dataset
The dataset contains information about 100 students, including:
- Age, Gender, CGPA, Marital Status, Year of Study
- Target variables: Depression, Anxiety, Panic Attack, Treatment

## Problem Statement
The dataset is highly imbalanced (fewer students with depression). The goal was to build a model that can accurately identify students at risk.

## Models Compared
1. Random Forest: Accuracy 71.4%, Recall (Depression) 0.38
2. Support Vector Machine (SVM): Accuracy 76.1%, Recall (Depression) 0.38
3. Logistic Regression: Accuracy 76.1%, Recall (Depression) 0.38

*Note: The recall for Class 1 (Depression) is low due to limited data and class imbalance.*

## Final Model
SVM was selected as the final model due to its higher accuracy and precision.
- Model saved as `student_mental_health_svm_model.pkl`
- Scaler saved as `scaler.pkl` (Required for preprocessing new data before prediction)

## Key Learnings
- Data Cleaning & Encoding (Categorical to Numeric)
- Handling Class Imbalance (Attempted Class Weight & Threshold Tuning)
- Error Analysis using Confusion Matrix (Identified False Negatives)
- Feature Scaling for SVM

## How to Use
1. Load the saved model and scaler using `joblib`.
2. Scale the input features using the saved scaler.
3. Predict using the model.
