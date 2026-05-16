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

## Data Privacy

The original dialysis dataset is not included in this repository due to privacy and data protection concerns. This repository only includes the machine learning workflow, preprocessing logic, model training process, and evaluation results.

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

## Experimental Results

The best test result in this notebook achieved approximately:

- Accuracy: 92.96%
- Balanced Accuracy: 92.11%
- Macro F1-score: 88.47%

Another experiment using RandomUnderSampler achieved approximately:

- Accuracy: 92.10%
- Balanced Accuracy: 93.42%
- Macro F1-score: 87.66%

## Notebook

The main implementation is provided in:

```text
dialysis_pca_knn_rule_based.ipynb
```

## What I Learned

Through this project, I practiced building a complete machine learning workflow, including data preprocessing, session segmentation, feature engineering, dimensionality reduction, imbalance handling, model tuning, and evaluation.

## Future Improvements

- Add more robust cross-validation
- Compare with Random Forest, XGBoost, and deep learning models
- Improve feature engineering for time-series signals
- Add model explainability analysis
- Package the pipeline into reusable modules
