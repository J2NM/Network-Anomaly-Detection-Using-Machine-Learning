# Network Anomaly Detection Using Machine Learning

## About this project
This project is a part of the AAI-501 course in the Applied Artificial Intelligence Program at theUniversity of San Diego (USD).
This project will focus on detecting abnormal patterns in network traffic that may indicate cybersecurity threats. The goal will be to classify network activity as normal or anomalous using machine learning techniques. 
-- Project Status: [Completed]

### Team Members

Ashley Figueroa – Data Lead

Cameron Aljilani – Research Lead

Juan Norena – Project Manager

## Dataset
### Network Anomality Dataset - Kaggle

Source: https://www.kaggle.com/datasets/amineipad/network-anoamly-dataset/data

The dataset contains 1,654 records with five columns: inbound rate, outbound rate, inbound bandwidth utilization, outbound bandwidth utilization, and a binary label indicating normal or anomalous activity. It is designed for binary classification problems in network anomaly detection, enabling researchers and practitioners to train and evaluate machine learning models that identify unusual traffic patterns. The features reflect quantitative network performance indicators, making the dataset suitable for cybersecurity analysis, intrusion detection experiments, and performance monitoring research.

### The dataset includes features such as:

- Connection duration
- Protocol type
- Source bytes
- Destination bytes
- Service type
- Connection status flag

## Installation
```
To use this project, first clone the repo.

git init

gh repo clone J2NM/Network-Anomaly-Detection-Using-Machine-Learning
```

## Project structure
```
Network Anomaly Detection AAI-501 Final project
│
├── README.md
├── requirements.txt
│── network_anomaly_dataset.csv
│
├── notebook
│   ├── AAI501_Final_Project_Network_Anomaly_Detection_Using_Machine_Learning.ipynb
│
├── Table of contents
│   ├── 1. Introduction
│   ├── 2. Dataset Description
│   ├── 3. Data Cleaning & Preprocessing
│   ├── 4. Exploratory Data Analysis (EDA)
│   ├── 5. Feature Engineering: Time-Aware Approximation Without Explicit Timestamps
│   ├── 5.1. Validation of Sequential Assumption
│   ├── 6. Time-Series Analysis
│   ├── 7. Model training
│   ├── 7.1. Train/Test Split
│   ├── 7.2. Logistic Regression Model
│   ├── 7.3. Gradient Boosting Model
│   ├── 7.4. Side-by-Side Model Comparison
│   ├── 7.5. Confusion Matrix Visualization
│   ├── 7.5.1 Confusion Matrix Visualization Using Stratified K-Fold Cross-Validation
│   ├── 7.5.2. Single-Split vs. Stratified K-Fold Out-Of-Fold Predictions
│   ├── 7.6. ROC Curve Comparison
│   ├── 7.6.1. ROC Curve Comparison (Single Split)
│   ├── 7.6.2. ROC Curve Comparison (Stratified K-Fold)
│
├── figures
│   ├──Confusion matrix 1 fold.png
│   ├──Confusion matrix K-fold.png
│   ├──Deviation from local baseline.png
│   ├──Feature engineering effect-inbound traffic.png
│   ├──Plots 1.png
│   ├──ROC K-fold.png
│   ├──ROC Single split.png
│   ├──Time series analisys.png
│   ├──correlation matrix.png
│
├── presentation
│   └── final_project_slides.pptx
│
└── report
    └── final_project_paper.pdf
```

### Methods used

- Machine learning
- Time series analysis
- Logistic regression
- Gradient boosting model
- Stratified K-Fold Out-Of-Fold Predictions

### Language 
- Python

### Project abstract

This project developed supervised learning models to detect anomalous network behavior using the Kaggle Network Anomaly dataset. The dataset did not contain explicit timestamps, so we could not use a standard time-series approach. Instead, we ran a row-to-row difference analysis during exploratory data analysis and found that changes between adjacent observations were small and stable (mean difference near zero, standard deviation approximately 0.07). This allowed us to treat the row index as a temporal proxy. We then applied time-aware feature engineering by generating lagged variables, rolling statistics, and normalized deviation metrics (delta and z-score). These additions expanded the feature space from 5 to 29 columns while preventing data leakage.
	We evaluated two classifiers: Logistic Regression and Gradient Boosting (n_estimators = 150, learning_rate = 0.05, max_depth = 3). The initial single stratified train/test split produced perfect performance for Gradient Boosting, which led us to also run Stratified K-Fold Cross Validation (k=5) with out-of-fold predictions. Gradient Boosting maintained exceptional performance (Accuracy 0.9958 ± 0.0041) compared with Logistic Regression (Accuracy 0.9709 ± 0.0101). The engineered features proved critical to improving both the single-split and K-Fold model performance, demonstrating that sequential structure can be extracted from non-temporal data and used for anomaly detection in network traffic.

### LICENSE

MIT License

Copyright (c) 2026 J2NM

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
