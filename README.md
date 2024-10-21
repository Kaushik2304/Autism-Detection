# Autism Spectrum Disorder (ASD) Prediction Using Machine Learning

## Project Overview
This project aims to develop a machine learning model and web application for accurately predicting autism traits in individuals of all ages. The early detection provided by this tool can lead to timely intervention, giving patients appropriate support and medication.

## Table of Contents
1. [Introduction](#introduction)
2. [Machine Learning Approach](#machine-learning-approach)
3. [Models Used](#models-used)
4. [Evaluation Metrics](#evaluation-metrics)
5. [Stacking Ensemble Method](#stacking-ensemble-method)
6. [Real-World Impact](#real-world-impact)
7. [Installation](#installation)


## Introduction
Autism Spectrum Disorder (ASD) is a neurodevelopmental disorder that impacts an individual's ability to interact, communicate, and learn. ASD encompasses various conditions marked by challenges in social interaction, behavior, speech, and nonverbal communication.

Machine learning can play a vital role in early ASD detection by analyzing large datasets of behavioral and clinical information. By leveraging predictive models based on genetic markers, brain imaging data, and behavioral assessments, we aim to provide tailored interventions and therapies for individuals with ASD.

## Machine Learning Approach
Our approach includes using various machine learning algorithms to develop predictive models. We leverage a combination of Logistic Regression, XGBoost, and Support Vector Machines (SVM) as base models to capture diverse learning patterns. A Random Forest classifier is used as the meta-learner to aggregate the predictions from these base models.

## Models Used
### 1. Logistic Regression
- Logistic Regression is a linear classification algorithm typically used for binary classification tasks.
- The model is trained on the training dataset (`X` and `Y`) and makes predictions on the test set (`X_test`).
- The model's performance is evaluated using a classification report and a confusion matrix visualized through a Seaborn heatmap.

### 2. XGBoost
- XGBoost (Extreme Gradient Boosting) is known for its high predictive performance and efficiency.
- The classifier is trained on the training dataset (`X` and `Y`) and makes predictions on the test set (`X_test`).
- The confusion matrix is generated and visualized using a Seaborn heatmap.

### 3. SVM (Support Vector Machine)
- An SVM with a Radial Basis Function (RBF) kernel is used for non-linear classification tasks.
- The model is trained and evaluated similarly, with its performance visualized using a confusion matrix heatmap.

### 4. Random Forest (Meta-Learner)
- The Random Forest classifier acts as the meta-learner in our stacking ensemble method.
- It is trained on the transposed validation set predictions and combines the outputs from the base models to produce the final prediction.

## Evaluation Metrics
For each model, the following metrics are calculated:
- **Accuracy**: The ratio of correctly predicted observations to the total observations.
- **Classification Report**: Includes precision, recall, F1-score, and support for each class.
- **Confusion Matrix**: Visualized using a Seaborn heatmap, displaying the number of true positives, true negatives, false positives, and false negatives.

## Stacking Ensemble Method
Stacking is an ensemble learning method where:
- Multiple base models (Logistic Regression, XGBoost, and SVM) are trained to make predictions.
- A Random Forest classifier is used as the meta-learner.
- Predictions from the base models are transposed and used as input for the meta-learner to predict the final outcome.

## Real World Impact
This `README.md` file provides a clear and comprehensive explanation of the project, the models used, and how to run the code. Feel free to adjust it according to your project's specifics or additional requirements.


## Installation
To set up the environment, clone this repository and install the required dependencies using:
```bash
pip install -r requirements.txt
