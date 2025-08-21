# Foundations of Machine Learning – Mini Project 00

This project is part of the "Foundations of Machine Learning" course. It involves building linear and polynomial regression models from scratch using NumPy and comparing them with models built using Scikit-learn. The goal is to understand model behavior, performance, and generalization on a dataset representing student learning metrics.

## Project Overview

This mini project consists of **seven Jupyter notebooks**:

1. **Linear Regression with Single Feature**
2. **Polynomial Regression with Single Feature**
3. **Linear Regression with Full Dataset**
4. **Polynomial Regression with Full Dataset**
5. **Comparison with Scikit-learn**
6. **Logistic Regression Implementation**
7. **Comprehensive Evaluation Metrics (Classification)**

Each notebook builds progressively on core ML concepts like hypothesis formulation, cost minimization via gradient descent, feature scaling, polynomial expansion, model evaluation, and threshold-based classification analysis.

## Dataset

The dataset includes the following columns:

* `EducationLevel`
* `Attendance`
* `TotalHours`
* `AssignmentsCompleted`
* `HackathonParticipation`
* `GitHubScore`
* `PeerReviewScore`
* `CourseName`
* `CapstoneScore` (target variable)

`MemberName` was excluded from modeling.

## Notebook Summaries

### 1. Linear Regression with Single Feature

* Implemented linear regression using `Attendance` as the single feature
* Explored multiple learning rates (`0.00001`, `0.001`, `0.1`, `1.0`)
* Applied feature scaling and visualized convergence
* Concluded that attendance alone was a weak predictor

### 2. Polynomial Regression with Single Feature

* Expanded input feature to polynomial degrees 2 and 3
* Implemented multi-parameter gradient descent
* Observed improvement in R² score with higher degrees
* Cautioned against overfitting beyond degree 2

### 3. Linear Regression with Full Dataset

* Used all features (excluding `MemberName`) with standardization
* Implemented vectorized multi-variable gradient descent
* Best R² score reached: approximately 0.52
* Visualized convergence for multiple learning rates

### 4. Polynomial Regression with Full Dataset

* Generated polynomial features (degree 2 and 3)
* Degree 2 achieved high performance (R² ~ 0.89)
* Degree 3 showed extreme overfitting (R² ~ 0.99 train, but poor CV results)
* Did not use Scikit-learn for training in this notebook

### 5. Scikit-learn Comparison

* Reproduced linear and polynomial models using Scikit-learn pipelines
* Compared coefficients, MSE, and R² scores
* Applied 5-fold cross-validation
* Validated manual results and highlighted overfitting in degree 3

### 6. Logistic Regression Implementation

* Implemented logistic regression from scratch
* Sigmoid function and cross-entropy loss
* Gradient descent for binary classification
* Classified students as Pass (Capstone Score ≥ 75) or Fail
* Evaluated model with confusion matrix, accuracy, precision, recall, and F1-score

### 7. Comprehensive Evaluation Metrics (Classification)

* Extended Notebook 6 evaluation with ROC and Precision–Recall curves
* Calculated AUC and Average Precision Score
* Performed threshold tuning (0.3, 0.5, 0.7)
* **Business Impact Insights:**
  - Threshold 0.3: High recall, lower precision; useful for catching all potential passers
  - Threshold 0.5: Balanced precision and recall; standard classification threshold
  - Threshold 0.7: High precision, lower recall; useful when resources are limited
* Provided visual interpretation of ROC and PR curves

## Key Concepts Applied

* Linear Regression and Polynomial Regression
* Feature Scaling (Z-score standardization)
* Gradient Descent Optimization
* Cost Functions (MSE and Cross-Entropy)
* R² Score Evaluation
* Polynomial Feature Expansion
* Overfitting vs Underfitting
* Cross-Validation (Manual and Scikit-learn)
* Logistic Regression and Binary Classification
* Classification Metrics (Confusion Matrix, Precision, Recall, F1, ROC, PR)
* Threshold Tuning & Business Impact

## Performance Summary

| Model Type                         | R² Score (Train) | Cross-Validation Avg R² |
| ---------------------------------- | ---------------- | ----------------------- |
| Linear (Manual)                    | ~0.52           | Not applied             |
| Polynomial Degree 2 (Manual)       | ~0.89           | Not applied             |
| Polynomial Degree 3 (Manual)       | ~0.99           | Not applied             |
| Linear (Scikit-learn)              | ~0.52           | Consistent              |
| Polynomial Degree 2 (Scikit-learn) | ~0.90           | ~0.79                   |
| Polynomial Degree 3 (Scikit-learn) | ~0.99           | ~-0.34 (overfitting)   |

## Requirements

* Python 3.x
* NumPy
* Matplotlib
* Scikit-learn (for Notebooks 5–7)

## How to Run

1. Clone or download the repository.
2. Open the notebooks in Jupyter Notebook or JupyterLab.
3. Run each cell step by step.
4. For Notebooks 5–7, ensure Scikit-learn is installed (`pip install scikit-learn`).

## Deliverables

* Seven Jupyter Notebooks:
  - **1_linear_regression_single_feature.ipynb**: Linear regression with attendance, multiple learning rates, convergence analysis, evaluation metrics
  - **2_polynomial_regression_single_feature.ipynb**: Polynomial regression (degrees 2 & 3), overfitting analysis
  - **3_linear_regression_full_dataset.ipynb**: Linear regression with all features, multi-dimensional gradient descent
  - **4_polynomial_regression_full_dataset.ipynb**: Polynomial regression with all features, degree comparison, cross-validation
  - **5_sklearn_comparison.ipynb**: Reproduced models with Scikit-learn, performance benchmarking
  - **6_logistic_regression_implementation.ipynb**: Logistic regression from scratch, binary classification
  - **7_comprehensive_evaluation_metrics.ipynb**: Extended classification metrics, ROC/PR curves, threshold tuning, business impact
* Handwritten derivations PDF
* This README file

## Conclusion

This project was built to deepen the understanding of **linear and polynomial regression, logistic regression, and classification metrics**. Implementing each step manually helped reinforce concepts like gradient descent, feature scaling, and model generalization. The final benchmarking with Scikit-learn validated the correctness of the manual implementations and provided insights into threshold-based decision making and business impact.
