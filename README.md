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
# Requirements
To run this project, you’ll need the following packages:
### pandas==1.3.3
### scikit-learn==0.24.2
### tensorflow==2.6.0
### numpy==1.21.2
### matplotlib==3.4.3                    
# Project Setup and Usage
### 1. Data Preprocessing
Binary Labeling: Convert the target variable (attack_class) into binary labels: 0 for normal and 1 for any attack.
One-Hot Encoding: Convert categorical columns (protocol_type, service, flag) into numerical format.
Feature Scaling: Normalize the feature values to improve model training.
### 2. Training the Hybrid Models
This project uses two approaches to combine Random Forest and Neural Networks.

### Approach 1: Random Forest Feature Selection + Neural Network
Train a Random Forest model on the dataset.
Select the top features based on feature importance scores from the Random Forest.
Train a Neural Network using only the selected important features.
### Approach 2: Random Forest Initial Classifier + Neural Network
Train a Random Forest model to generate initial predictions.
Use the Random Forest output as an additional feature along with the original dataset.
Train a Neural Network using this combined dataset.
# 3. Model Evaluation and Results
Evaluate both models using accuracy, precision, recall, and F1 score. This helps determine the best-performing approach for our IDS.

# 4. Visualizing Results
Generate bar charts to compare model metrics (accuracy, precision, recall, F1 score) across both approaches to visually assess performance.

# Code Usage
To run the project, follow these steps in the main project script:

Import necessary libraries and load the data.
Preprocess the data as described in the preprocessing section.
Train and evaluate models using both approaches.
Visualize the metrics for model comparison.
