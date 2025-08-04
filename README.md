# Foundations of Machine Learning – Mini Project 00

This project is part of the "Foundations of Machine Learning" course. It involves building linear and polynomial regression models from scratch using NumPy and comparing them with models built using Scikit-learn. The goal is to understand model behavior, performance, and generalization on a dataset representing student learning metrics.

## Project Overview

This mini project consists of five Jupyter notebooks:

1. **Linear Regression with Single Feature**
2. **Polynomial Regression with Single Feature**
3. **Linear Regression with Full Dataset**
4. **Polynomial Regression with Full Dataset**
5. **Comparison with Scikit-learn**

Each notebook builds progressively on core ML concepts like hypothesis formulation, cost minimization via gradient descent, feature scaling, polynomial expansion, model evaluation, and overfitting analysis.

## Files

Mini_Project_00_[Sashini Jayakodi]/
├── notebooks/
│   ├── 1_linear_regression_single_feature.ipynb
│   ├── 2_polynomial_regression_single_feature.ipynb
│   ├── 3_linear_regression_full_dataset.ipynb
│   ├── 4_polynomial_regression_full_dataset.ipynb
│   └── 5_sklearn_comparison.ipynb
└── README.md

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

## Key Concepts Applied

* Linear Regression and Polynomial Regression
* Feature Scaling (Z-score standardization)
* Gradient Descent Optimization
* Cost Function (MSE)
* R² Score Evaluation
* Polynomial Feature Expansion
* Overfitting vs Underfitting
* Cross-Validation (Manual and Scikit-learn)
* Benchmarking with Scikit-learn

## Performance Summary

| Model Type                         | R² Score (Train) | Cross-Validation Avg R² |
| ---------------------------------- | ---------------- | ----------------------- |
| Linear (Manual)                    | \~0.52           | Not applied             |
| Polynomial Degree 2 (Manual)       | \~0.89           | Not applied             |
| Polynomial Degree 3 (Manual)       | \~0.99           | Not applied             |
| Linear (Scikit-learn)              | \~0.52           | Consistent              |
| Polynomial Degree 2 (Scikit-learn) | \~0.90           | \~0.79                  |
| Polynomial Degree 3 (Scikit-learn) | \~0.99           | \~-0.34 (overfitting)   |

## Requirements

* Python 3.x
* NumPy
* Matplotlib
* Scikit-learn (only used in Notebook 5)

## How to Run

1. Clone or download the repository.
2. Open the notebooks in Jupyter Notebook or JupyterLab.
3. Run each cell step by step.
4. For Notebook 5, ensure Scikit-learn is installed (`pip install scikit-learn`).

## Deliverables

* Five Jupyter Notebooks as described
* Handwritten derivations PDF
* This README file

## Conclusion

This project was built to deepen the understanding of linear models and polynomial regression. Implementing each step manually helped reinforce concepts like gradient descent, feature scaling, and model generalization. The final benchmarking with Scikit-learn validated the correctness of the manual implementations.

