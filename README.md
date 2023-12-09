# Representation-Learning-Parameter-Tuning-and-Classification-Comparisons

## Project Overview
This project involves a comprehensive analysis of the Abalone and Wine datasets using various machine learning algorithms. The aim is to compare the performance of these algorithms in terms of accuracy and identify the best and worst performing algorithms for each dataset. 

## Key Objectives
- Implement Representation Learning using PCA (Principal Component Analysis) and LDA (Linear Discriminant Analysis).
- Perform Parameter Tuning for optimal algorithm performance.
- Compare the classification capabilities of kNN, Naive Bayes, Decision Tree, Random Forest, and Gradient Boosted Tree.
- Utilize 5-fold cross-validation for reliable performance evaluation.

## Datasets
1. **Abalone Dataset**: Used to predict the age of abalone from physical measurements.
2. **Wine Dataset**: Aimed at classifying wines based on their chemical properties.

## Algorithms Used
- k-Nearest Neighbors (kNN)
- Naive Bayes
- Decision Tree
- Random Forest
- Gradient Boosted Tree

## Key Findings
### Table 6.1: Accuracy Percentage for Different Algorithms on Abalone Dataset

| Algorithm               | Best Settings for RAW                  | Accuracy RAW | Best Settings for PCA                  | Accuracy PCA | Best Settings for LDA                  | Accuracy LDA |
|-------------------------|----------------------------------------|--------------|----------------------------------------|--------------|----------------------------------------|--------------|
| **kNN**                 | k=73, weights="distance"               | 28.32%       | k=73, weights="distance"               | 27.17%       | k=73, weights="distance"               | 28.32%       |
| **Complement Naive Bayes** | fit_prior=True                       | 17.56%       | fit_prior=True                         | 20.02%       | fit_prior=True                         | 23.53%       |
| **Decision Tree**       | RAW -> max_depth=5                     | 24.69%       | PCA -> max_depth=4                     | 27.94%       | LDA -> max_depth=4                     | 24.69%       |
| **Random Forest**       | RAW -> max_depth=9, n_estimators=50    | 27.18%       | PCA -> max_depth=4, n_estimators=40    | 26.79%       | LDA -> max_depth=6, n_estimators=40    | 27.94%       |
| **Gradient Tree Boosting** | RAW -> max_depth=5, max_leaf_nodes=4, n_estimators=7 | 26.60% | PCA -> max_depth=4, max_leaf_nodes=4, n_estimators=5 | 23.72% | LDA -> max_depth=2, max_leaf_nodes=16, n_estimators=10 | 26.70% |

### Table 6.2: Accuracy Percentage for Different Algorithms on Wine Dataset

| Algorithm               | Best Settings for RAW                  | Accuracy RAW | Best Settings for PCA                  | Accuracy PCA | Best Settings for LDA                  | Accuracy LDA |
|-------------------------|----------------------------------------|--------------|----------------------------------------|--------------|----------------------------------------|--------------|
| **kNN**                 | k=46, weights="distance"               | 68.15%       | k=46, weights="distance"               | 67.38%       | k=46, weights="distance"               | 68.15%       |
| **Complement Naive Bayes** | fit_prior=True                       | 47.89%       | fit_prior=True                         | 44.46%       | fit_prior=True                         | 44.46%       |
| **Decision Tree**       | RAW -> max_depth=13                    | 58.40%       | PCA -> max_depth=14                    | 58.65%       | LDA -> max_depth=17                    | 59.38%       |
| **Random Forest**       | RAW -> max_depth=14, n_estimators=50   | 68.92%       | PCA -> max_depth=14, n_estimators=50   | 67.57%       | LDA -> max_depth=14, n_estimators=40   | 64.49%       |
| **Gradient Tree Boosting** | RAW -> max_depth=6, max_leaf_nodes=32, n_estimators=10 | 59.57% | PCA -> max_depth=7, max_leaf_nodes=32, n_estimators=10 | 56.55% | LDA -> max_depth=8, max_leaf_nodes=32, n_estimators=10 | 57.97% |

### Summary of Results
- **Abalone Dataset**: Best - kNN; Worst - Naive Bayes
- **Wine Dataset**: Best - Random Forest; Worst - Naive Bayes
