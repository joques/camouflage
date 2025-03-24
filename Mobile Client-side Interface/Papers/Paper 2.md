# Title: A Machine Learning-Based Credit Card Fraud Detection Using the GA Algorithm for Feature Selection  

**Authors:** Emmanuel Ileberi, Yanxia Sun, and Zenghui Wang  
**Digital Object Identifier:** [https://doi.org/10.1186/s40537-022-00573-8](https://doi.org/10.1186/s40537-022-00573-8)  
**Published in:** Journal of Big Data (2022)  


## Abstract
The recent advances of e-commerce and e-payment systems have sparked an increase in financial fraud cases such as credit card fraud. It is therefore crucial to implement mechanisms that can detect credit card fraud. Features of credit card fraud play an important role when machine learning is used for fraud detection, and they must be chosen properly. This paper proposes a machine learning (ML)-based credit card fraud detection engine using the genetic algorithm (GA) for feature selection. After the optimized features are chosen, the proposed detection engine uses the following ML classifiers: Decision Tree (DT), Random Forest (RF), Logistic Regression (LR), Artificial Neural Network (ANN), and Naïve Bayes (NB). To validate the performance, the proposed credit card fraud detection engine is evaluated using a dataset generated from European cardholders. The results demonstrated that the proposed approach outperforms existing systems.


## Problem & Objective
The research addresses the growing threat of credit card fraud, which has increased with the expansion of e-commerce and digital payment systems. Traditional methods such as encryption and tokenization help secure transactions but do not fully prevent fraud.

### Key Issues Identified:
- Credit card fraud is difficult to detect due to constantly changing fraudulent patterns.
- Highly imbalanced datasets (fraud cases are rare compared to normal transactions) make detection challenging.
- Many machine learning (ML) models for fraud detection lack reproducibility because real credit card data is confidential and anonymized.
- Existing ML fraud detection models have low accuracy and struggle with imbalanced data.

### Proposed Solution
The paper introduces an ML-based fraud detection system that integrates Genetic Algorithm (GA) for feature selection and five ML classifiers:
- Decision Tree (DT)
- Random Forest (RF)
- Logistic Regression (LR)
- Artificial Neural Network (ANN)
- Naïve Bayes (NB)

The model is trained and tested using a real-world dataset from European credit cardholders.


## Literature Review
The authors review past research on credit card fraud detection using ML, highlighting the limitations of existing approaches:
1. **Lack of feature selection:** Many studies used all features, which can reduce accuracy.
2. **Imbalanced datasets:** Fraudulent transactions are much fewer than legitimate ones, leading to poor classifier performance.
3. **Algorithm comparisons:** Prior studies used classifiers such as SVM, k-NN, and Logistic Regression, but results varied.
4. **Oversampling techniques:** Some studies addressed data imbalance using SMOTE, but feature selection was not optimized.

The authors argue that applying GA for feature selection can improve ML performance.

## Research Methodology

###  Dataset
- The dataset consists of 284,807 transactions over two days.
- Only 0.172% of the transactions are fraudulent (highly imbalanced).
- Features include Time, Amount, and 28 anonymized features (V1-V28).
- SMOTE (Synthetic Minority Oversampling Technique) is used to balance the dataset.

### Feature Selection with Genetic Algorithm (GA)
- GA is used to select the most relevant features, reducing computation cost and improving accuracy.
- The fitness function is based on the RF classifier to ensure robust feature selection.

#### Benefits of GA-based feature selection:
- Avoids overfitting.
- Handles both continuous and categorical features.
- Works well with imbalanced data.

### Machine Learning Classifiers Used
The study tests five supervised learning models:
1. **Logistic Regression (LR)** – Used for binary classification, computes probabilities.
2. **Decision Tree (DT)** – Breaks down data into decision nodes based on feature values.
3. **Random Forest (RF)** – Uses multiple decision trees and averages their outputs.
4. **Naïve Bayes (NB)** – Based on Bayes' Theorem, assumes feature independence.
5. **Artificial Neural Network (ANN)** – Mimics the human brain, with input, hidden, and output layers.

## Fraud Detection Framework
The proposed GA-ML fraud detection system follows these steps:

1. **Data Preprocessing:**
   - Normalize input features using min-max scaling.
   - Apply SMOTE to balance the dataset.
2. **Feature Selection with GA:**
   - GA selects the best subset of features.
3. **Model Training & Testing:**
   - Train ML models using the selected features.
   - Evaluate models on test data.

### Performance Metrics
To assess model effectiveness, the study uses:
- **Accuracy:** Measures overall correctness.
- **Recall (True Positive Rate):** Measures fraud detection ability.
- **Precision:** Measures correctness of fraud detections.
- **F1-Score:** Balances precision and recall.
- **AUC (Area Under Curve):** Measures classifier performance (closer to 1 is better).

## Experimental Results
The experiments were conducted using Google Colab with Scikit-Learn.

### Model Performance on Different Feature Sets
The best-performing feature vector (v5) yielded:
- **RF:** 99.98% accuracy, 95.34% precision
- **DT:** 99.89% accuracy
- **ANN:** 99.08% accuracy

### Comparison with Full Feature Set
- Using all features resulted in lower accuracy compared to GA-selected features.
- RF performed best, followed by DT and ANN.
