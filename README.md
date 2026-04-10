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

## Project structure
```
Network Anomaly Detection AAI-501 Final project
│
├── README.md
├── requirements.txt
│
├── data
│   ├── raw
│   │   └── network_anomaly_dataset.csv
│   │
│   └── processed
│       └── cleaned_network_data.csv
│
├── notebooks
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_preprocessing.ipynb
│   └── 03_model_experiments.ipynb
│
├── src
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── classification_models.py
│   ├── clustering_models.py
│   └── evaluation_metrics.py
│
├── figures
│   ├── feature_distributions.png
│   ├── correlation_matrix.png
│   └── model_performance.png
│
├── results
│   ├── model_results.csv
│   └── confusion_matrix.png
│
├── presentation
│   └── final_project_slides.pptx
│
└── report
    └── final_project_paper.pdf
```
# Technical report
	
