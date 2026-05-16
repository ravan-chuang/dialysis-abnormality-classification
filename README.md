# Dialysis Abnormality Classification

A machine learning project for classifying normal and abnormal dialysis sessions from time-series medical data.

The project builds a complete pipeline including data cleaning, session segmentation, missing-value handling, feature extraction, PCA dimensionality reduction, class imbalance handling, and KNN classification.

## Features

- Load dialysis records from Excel files
- Clean and preprocess time-series medical data
- Segment records into dialysis sessions
- Handle missing values with interpolation and median imputation
- Extract statistical and time-series features
- Apply PCA for dimensionality reduction
- Train KNN classifiers with different hyperparameters
- Handle class imbalance using RandomUnderSampler and SMOTE-based methods
- Evaluate models with accuracy, balanced accuracy, macro F1-score, and confusion matrix

## Tech Stack

- Python
- pandas
- NumPy
- scikit-learn
- imbalanced-learn
- matplotlib

## Machine Learning Pipeline

```text
Raw Excel Files
        ↓
Data Cleaning
        ↓
Session Segmentation
        ↓
Missing Value Imputation
        ↓
Feature Extraction
        ↓
Class Imbalance Handling
        ↓
PCA Dimensionality Reduction
        ↓
KNN Classification
        ↓
Model Evaluation
```

## Model Settings

- Classifier: K-Nearest Neighbors
- Dimensionality Reduction: PCA
- Distance Metric: Manhattan distance
- Weighting Strategy: Distance-based weighting
- Imbalance Handling: RandomUnderSampler / SMOTE-based methods

## Best Experimental Result

The best experiment achieved approximately:

- Accuracy: 95.6%
- Balanced Accuracy: 94.3%
- Macro F1-score: 92.5%

## What I Learned

Through this project, I practiced building a complete machine learning workflow, including data preprocessing, feature engineering, dimensionality reduction, imbalance handling, model tuning, and evaluation.

## Future Improvements

- Add more robust cross-validation
- Compare with Random Forest, XGBoost, and deep learning models
- Improve feature engineering for time-series signals
- Add model explainability analysis
- Package the pipeline into reusable modules
