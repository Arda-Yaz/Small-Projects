# Kaggle Titanic Project

This repository contains my work on the Kaggle Titanic challenge. The goal is to explore the dataset, perform feature engineering, and build predictive models to understand what factors most influence survival.

(0.78229)

## Project Overview

- **Objective:** Predict Titanic passenger survival using various features.
- **Approach:** Data exploration, feature engineering, model building, and evaluation.
- **Key Ideas Tested:**
  - Adding a **Family Size** feature.
  - Extracting insights from the **Cabin** information.
  - Using **Fare** as a proxy for cabin sections.

## Data Exploration & Feature Engineering

### Family Size Feature

- **Idea:**  
  Create a new column (`FamilySize`) combining the `SibSp` and `Parch` features to capture the effect of traveling with family.
- **Hypothesis:**  
  Larger families might have different survival probabilities.
- **Outcome:**  
  Including this feature resulted in a decrease in model accuracy on the validation set.

### Cabin Feature

- **Observation:**  
  Noticed that passengers assigned to certain cabins had higher survival rates.
- **Attempt:**  
  Derived a new feature based on cabin numbers to capture this pattern.
- **Challenge:**  
  Approximately 80% of the cabin data is missing, making it difficult to extract reliable insights.

### Fare as a Proxy for Cabin Sections

- **Motivation:**  
  Hypothesized that similar fare values might indicate similar cabin locations (or sections).
- **Experiment:**  
  Created a new feature from the `Fare` column with the assumption that passengers paying similar fares might belong to similar cabin sections.
- **Outcome:**  
  - **Training:** Model accuracy improved with this feature.
  - **Kaggle Submission:** No change in the final score, indicating the feature didn’t generalize to the hidden test set.

## Model Evaluation

- **Metric Used:** Accuracy score.
- **Comparisons Made:**  
  - The **Family Size** feature unexpectedly reduced performance.
  - The **Fare-based** feature showed promise in the training phase but did not translate into better performance on the Kaggle test data.

## Conclusion & Future Work

- **Summary:**  
  - Some engineered features (like `FamilySize`) were not beneficial.
  - Using `Fare` as a proxy for cabin information had mixed results.
- **Next Steps:**  
  - Explore different imputation techniques for missing cabin data.
  - Test alternative feature extraction methods.
  - Apply more robust model tuning, such as hyperparameter optimization, to further improve performance.
