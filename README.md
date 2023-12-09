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

| Best Settings | Abalone_Raw | Abalone_PCA | Abalone_LDA |
|---------------|-------------|-------------|-------------|
| **kNN** | k=73, weights="distance" | 28.32% | 27.17% |
| **Complement Naive Bayes** | fit_prior=True | 17.56% | 20.02% | 23.53% |
| **Decision Tree** | See Notes | 24.69% | 27.94% | 24.69% |
| **Random Forest** | See Notes | 27.18% | 26.79% | 27.94% |
| **Gradient Tree Boosting** | See Notes | 26.60% | 23.72% | 26.70% |

*Notes: Decision Tree and Random Forest have specific settings for RAW, PCA, and LDA.*

### Table 6.2: Accuracy Percentage for Different Algorithms on Wine Dataset

| Best Settings | Wine_Raw | Wine_PCA | Wine_LDA |
|---------------|----------|----------|----------|
| **kNN** | k=46, weights="distance" | 68.15% | 67.38% |
| **Complement Naive Bayes** | fit_prior=True | 47.89% | 44.46% | 44.46% |
| **Decision Tree** | See Notes | 58.40% | 58.65% | 59.38% |
| **Random Forest** | See Notes | 68.92% | 67.57% | 64.49% |
| **Gradient Tree Boosting** | See Notes | 59.57% | 56.55% | 57.97% |

*Notes: As with the Abalone dataset, specific settings for each representation technique apply.*

### Summary of Results
- **Abalone Dataset**: Best - kNN; Worst - Naive Bayes
- **Wine Dataset**: Best - Random Forest; Worst - Naive Bayes
