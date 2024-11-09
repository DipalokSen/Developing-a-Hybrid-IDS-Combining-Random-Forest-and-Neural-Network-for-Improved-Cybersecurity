# Developing-a-Hybrid-IDS-Combining-Random-Forest-and-Neural-Network-for-Improved-Cybersecurity
# Project Overview
This project aims to develop a hybrid Intrusion Detection System (IDS) that combines the strengths of both Random Forest (a classical machine learning model) and Neural Networks (a deep learning model) to detect network intrusions. We use the NSL-KDD dataset, which contains labeled network traffic data, for training and testing the IDS. The system is designed to classify network traffic into two categories: normal and attack.

# Project Structure
The project includes the following main steps:

Data Preprocessing: Cleaning, transforming, and encoding the data to make it suitable for machine learning models.
Hybrid Model Creation: Two hybrid approaches are used to combine Random Forest and Neural Networks.
### Approach 1: Random Forest for feature selection, followed by a Neural Network for classification.
### Approach 2: Random Forest as an initial classifier to create additional features, then a Neural Network for final classification.
Model Evaluation: Evaluate both approaches using classification metrics (accuracy, precision, recall, and F1 score) to determine the best performing model.
Conclusion and Visualization: Summarize the results and visualize model performance using graphs.
# Dataset
The NSL-KDD dataset, a modified version of the KDD Cup 1999 dataset, is used for this project. This dataset includes both normal network traffic and various types of network attacks. You can download the NSL-KDD dataset here.

The dataset includes:

Categorical features such as protocol_type, service, and flag.
Numerical features representing different network parameters.
A target column representing normal or different types of attacks, which we convert to binary labels (0 for normal, 1 for attacks).
Requirements
