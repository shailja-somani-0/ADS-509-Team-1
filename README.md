# ADS-509-Team-1
Final Project for Summer 2024 ADS 509 Team 1: Roger Qiu, Jesse Gutierrez and Shailja Somani

This project aims to:
* Analyze key differences in the text of news articles pertaining to Tesla vs. Toyota.
* Classify text descriptions as either related to Tesla or Toyota using various machine learning models. The best performing model is then used to classify new descriptions.
* Attempt various topic modeling techniques to further dive into underlying themes within the vehicle news textual corpus. 

## Table of Contents
- [Introduction](#introduction)
- [Data](#data)
- [Classification Models](#classification-models)
- [Topic Modeling Models](#topic-modeling-models)
- [Setup](#setup)
- [Classification Models Usage & Results](#classification-models-usage-and-results)
- [Contributing](#contributing)
- [License](#license)

## Introduction
The goal of this project is to build a classification model that categorizes text descriptions as referring to either Tesla or Toyota. The project involves data preprocessing, vectorization using TF-IDF, training multiple classifiers, and selecting the best model based on accuracy.

## Data
The dataset used in this project consists of text descriptions labeled as either 'tesla' or 'toyota' pulled from a news API (https://newsapi.org/ \) using the following key: d6995599193044b0a5f954c098da84d6. The API references news articles from the last 29-days referencing the automanufacturers Toyota or Tesla. The text data is preprocessed to remove null values and converted into a string format suitable for vectorization. Along with removing stop words, punctuation, etc, the tokens 'tesla' and 'toyota' are removed so as not to bias any models.

## Classification Models
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

## Topic Modeling Models
The following topic modeling methods are evaluated:
- Non-Negative Matrix Factorization (NMF)
- Latent Semantic Analysis (LSA)
- Latent Dirichlet Allocation (LDA)
For LDA, the optimal number of topics is determined using perplexity scores. Wordclouds with the top 30 words within each topic are displayed following model creation. 

TF-IDF and Count Vectorizers are used for the aforementioned models. For both vectorizers, the minimum number of documents a term must be in the maximum percentage of documents a term may be in to remain in consideration as a token is defined. These parameters can be changed to best fit your use case. 

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

## Classification Models Usage and Results
To run the classifcation model and run new descriptions:
1. Run the script with the models and select the best one
    python train_and_select_model.py
2. Classify a new text description

The results of the model evaluations will be printed in the console and the best performing model will be saved for future use. The accuracy of each model is displayed and the best model is used for new classifications.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This example provides a comprehensive overview of the project, including the purpose, data, models used, setup instructions, usage guidelines, and contribution information. 
