# Dialysis Abnormality Classification

An end-to-end machine-learning pipeline for classifying normal and abnormal dialysis sessions from time-series medical records.

## Project Overview

This project processes raw dialysis records into session-level features and evaluates machine-learning models while reducing the risk of data leakage between training and evaluation data.

The current main pipeline uses folder-based labels, session segmentation, statistical and temporal feature extraction, feature selection, XGBoost, class balancing, and threshold tuning.

## Key Results

- Processed 6,279 dialysis sessions
- Extracted 328 statistical and temporal features
- Selected the top 30 features for the final XGBoost model
- Used group-aware evaluation to prevent source-group overlap
- Achieved mean balanced accuracy of approximately 0.86
- Achieved mean F1-score of approximately 0.87

## Pipeline
```text
Raw Excel Records
        |
        v
Data Cleaning and Missing-Value Handling
        |
        v
Session Segmentation
        |
        v
Statistical and Temporal Feature Extraction
        |
        v
328 Session-Level Features
        |
        v
Top-30 Feature Selection
        |
        v
XGBoost and Threshold Tuning
        |
        v
Group-Aware Evaluation
```

## Dataset

The dataset contains dialysis-machine records divided into normal and abnormal groups.

The original files are not included because they contain private medical information. This repository does not publish patient identifiers or raw medical records.

## Data Processing

The pipeline includes:

- Reading and standardizing Excel records
- Handling missing values using global statistics
- Segmenting records into dialysis sessions
- Removing sessions that are too short or incomplete
- Extracting statistical and temporal characteristics
- Preventing source-group overlap between training and evaluation data

## Feature Engineering

Examples of extracted features include:

- Mean, standard deviation, minimum, and maximum
- Median, quartiles, and range
- Absolute-difference statistics
- First-, middle-, and last-third means
- Linear trend and slope
- Minimum position and change from session start

Important features included measurements related to systolic and diastolic blood pressure, alerts, and temporal variation.

## Modeling

The project evaluates several machine-learning approaches, including:

- PCA and KNN baselines
- Random Forest
- XGBoost
- Feature-selection experiments
- Class-balancing methods
- Classification-threshold tuning

The final reported result uses XGBoost with the top 30 selected features.

## Evaluation

The main evaluation metrics are:

- Accuracy
- Balanced accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

Group-aware evaluation is used to reduce leakage caused by records from the same source appearing in both training and validation sets.

## Main Result

| Metric | Mean Result |
|---|---:|
| Balanced Accuracy | 0.86 |
| F1-score | 0.87 |
| Recall | 0.90 |

Results are based on cross-validation and rounded for presentation.

## Privacy

- Raw medical records are not published
- Patient-identifying information is excluded
- Only aggregated metrics and non-identifying figures are shown

## Limitations

- The dataset comes from a limited number of source files
- Results should not be interpreted as clinical validation
- Further testing on independent institutions and larger datasets is required
- Threshold tuning and feature selection must be performed carefully to avoid optimistic evaluation

## Future Improvements

- Build a fully reproducible modular Python pipeline
- Add SHAP-based model explainability
- Evaluate external datasets
- Compare additional time-series and deep-learning models
- Add automated tests for preprocessing and feature extraction

## Technologies

- Python
- pandas
- NumPy
- scikit-learn
- XGBoost
- imbalanced-learn
- matplotlib
