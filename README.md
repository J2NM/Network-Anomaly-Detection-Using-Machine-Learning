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
# Technical report
	
