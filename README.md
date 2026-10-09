ML-Algorithms-Comparison
Comparison of Machine Learning Algorithms Using OpenML Datasets

This repository presents an experimental comparison of three classical machine learning algorithms for classification tasks using datasets from OpenML. The project is implemented in Python using the scikit-learn library.

The goal is to evaluate the performance of different classification algorithms across datasets with varying characteristics and levels of complexity.

Datasets

Three datasets were selected for the experiments:

Dataset	Description	Characteristics
breast-w	Breast cancer prediction	Binary classification
diabetes	Diabetes prediction	Numerical features
credit-g	Credit risk assessment	Numerical and categorical features
Machine Learning Algorithms

The following algorithms were evaluated:

k-Nearest Neighbors (k-NN) — A distance-based classification algorithm that assigns a class based on the nearest training samples.
Random Forest — An ensemble learning method that combines multiple decision trees to improve predictive performance and robustness.
Multi-Layer Perceptron (MLP Classifier) — A feedforward neural network capable of learning complex, non-linear relationships in data.
Methodology and Preprocessing

A consistent preprocessing and evaluation workflow was applied to compare the algorithms fairly.

Missing Value Imputation: Missing values were handled using imputation techniques, such as mean imputation.
Feature Scaling: StandardScaler was used to standardize numerical features, particularly for k-NN and MLP.
Categorical Encoding: OneHotEncoder was used to convert categorical variables into numerical representations, especially for the credit-g dataset.
Model Evaluation: Stratified 5-fold cross-validation was used to assess model performance across different data splits.
Evaluation Metrics

The following metrics were used to evaluate the classification models:

Accuracy: The proportion of correctly classified samples.
Precision: The proportion of positive predictions that are correct.
Recall: The proportion of actual positive samples correctly identified.
Macro F1-score: The unweighted average of the F1-scores across all classes.
Results and Key Findings

The experiments highlighted differences in performance across the three algorithms and datasets.

Random Forest: Achieved the strongest and most consistent overall performance, reaching 96.71% accuracy on breast-w and 75.40% accuracy on credit-g. It handled mixed numerical and categorical features effectively without requiring extensive hyperparameter tuning.
MLP Classifier: Achieved 76.44% accuracy on diabetes. However, its performance was more sensitive to hyperparameter choices and feature scaling.
k-Nearest Neighbors (k-NN): Performed effectively on the breast-w dataset but struggled with credit-g, achieving an F1-score of 61.20%. This may be attributed in part to the increased dimensionality resulting from One-Hot Encoding.

Overall, Random Forest provided the most reliable results across the evaluated datasets, while MLP performance depended more heavily on preprocessing and parameter configuration. The results also demonstrate how dataset characteristics and feature dimensionality can influence classification performance.

Technologies Used
Python
scikit-learn
NumPy
pandas
OpenML
Project Goals
Compare classical machine learning algorithms on different classification tasks.
Investigate the impact of preprocessing techniques on model performance.
Evaluate classifiers using cross-validation and multiple performance metrics.
Understand the strengths and limitations of distance-based, ensemble, and neural network approaches.
Conclusion

This project provides a practical comparison of three widely used classification algorithms. The findings emphasize the importance of appropriate preprocessing, evaluation methodology, and algorithm selection when working with datasets of different structures and complexity.
