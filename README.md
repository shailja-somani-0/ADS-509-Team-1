# ADS-509-Team-1
Final Project for Summer 2024 ADS 509 Team 1: Roger Qiu, Jesse Gutierrez and Shailja Somani

This project aims to classify text descriptions as either related to Tesla or Toyota using various machine learning models. The best performing model is then used to classify new descriptions.

## Table of Contents
- [Introduction](#introduction)
- [Data](#data)
- [Models](#models)
- [Setup](#setup)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction
The goal of this project is to build a classification model that categorizes text descriptions as referring to either Tesla or Toyota. The project involves data preprocessing, vectorization using TF-IDF, training multiple classifiers, and selecting the best model based on accuracy.

## Data
The dataset used in this project consists of text descriptions labeled as either 'tesla' or 'toyota' pulled from a news API (https://newsapi.org/ \) using the following key: d6995599193044b0a5f954c098da84d6. The API references news articles from the last 29-days referencing the automanufacturers Toyota or Tesla. The text data is preprocessed to remove null values and converted into a string format suitable for vectorization.

## Models
The following machine learning models are evaluated in this project:
- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest
- Naive Bayes
- K-Nearest Neighbors (KNN)
- Gradient Boosting
- AdaBoost
- Decision Tree
- XGBoost

The best performing model is selected based on accuracy.

## Setup
To set up the project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/shailja-somani-0/ADS-509-Team-1.git
   cd tesla-vs-toyota-classification

2. Install the below packages already not installed and then restart the kernel

!pip install newsapi-python
!pip install textblob
!pip install xgboost
!pip install imblearn
!pip install pyLDAvis==3.4.1 --user
!pip install contractions

## Usage
To run the classifcation model and run new descriptions:
1. Run the script with the models and select the best one
    python train_and_select_model.py
2. Classify a new text description

## Results
The results of the model evaluations will be printed in the console and the best performing model will be saved for future use. The accuracy of each model is displayed and the best model is used for new classifications.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This example provides a comprehensive overview of the project, including the purpose, data, models used, setup instructions, usage guidelines, and contribution information. You can customize it further to match the specifics of your project.
