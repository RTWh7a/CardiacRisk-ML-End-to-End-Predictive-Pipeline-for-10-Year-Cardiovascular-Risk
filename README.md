# CardiacRisk-ML-End-to-End-Predictive-Pipeline-for-10-Year-Cardiovascular-Risk
This repository contains a comprehensive Machine Learning pipeline designed to predict the 10-year risk of Coronary Heart Disease (CHD) using the Framingham dataset. The project transitions from raw clinical data to a production-ready classifier, prioritizing data integrity and model interpretability.

Technical Workflow & Architecture

Exploratory Data Analysis (EDA): Leveraged Pandas and Seaborn to identify feature distributions and high-risk demographic correlations.

Advanced Preprocessing:

Imputation Strategy: Addressed missingness in clinical variables (e.g., glucose, cigsPerDay) to preserve dataset volume.

Outlier Detection: Implemented an Isolation Forest algorithm to identify and prune anomalous clinical observations, ensuring the model generalizes on standard patient profiles.

Feature Scaling: Applied StandardScaler to normalize continuous variables (sysBP, BMI, totChol), preventing gradient bias.

Model Selection & Benchmarking:
Developed and evaluated a suite of classifiers to identify the optimal balance between Sensitivity (Recall) and Precision:

Logistic Regression: Established a statistical baseline.

K-Nearest Neighbors (KNN): Evaluated local feature space clusters.

Decision Trees & Random Forest: Analyzed non-linear feature interactions and feature importance.

Support Vector Machines (SVM): Utilized for high-dimensional boundary optimization.

Performance Metrics: Evaluated using Confusion Matrices, ROC-AUC curves, and F1-scores to minimize False Negatives—critical in a medical diagnostic context.

Deployment & Real-World Utility
The model serves as a Clinical Decision Support System (CDSS). It allows healthcare providers to input routine biometric data and receive a risk score, enabling early preventative interventions (lifestyle changes or medication) years before a cardiac event occurs.
