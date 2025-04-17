# Credit Card Fraud Prediction

## Context of Project
Credit card fraud poses a persistent and evolving threat in today's digital economy, undermining financial institutions, e-commerce businesses, and consumer trust in digital payment platforms. In 2023, global e-commerce fraud losses were estimated to exceed $48 billion, with North America accounting for over 42% of these losses (Mastercard, 2024). The rapid growth of online transactions has opened new entry points for increasingly sophisticated fraud tactics (Cherif et al., 2022), from digital skimming (Mastercard, 2024) to synthetic identity fraud (Mastercard, n.d.). Less technically-intensive social engineering techniques like phishing are also evolving, highlighting the growing urgency for adaptive, data-driven solutions that go beyond traditional rule-based fraud detection systems. 

Industries have adopted supervised machine learning models such as logistic regression and Random Forest to address evolving fraud tactics. (Afriyie et al., 2023). However, current approaches still face limitations, including class imbalance in datasets, which leads to ineffective predictions, changing fraud patterns over time (data drift), and underutilization of behavioural features that could improve detection accuracy (Cherif et al., 2023).

To address these limitations, our project analyzes a large-scale, labeled dataset of over 2.6 million U.S. credit card transactions collected between 2021 and 2023 to identify behavioral indicators of fraud. We first apply supervised machine learning models, using logistic regression as a baseline, and build on this using Random Forest and XGBoost — two widely adopted models in fraud detection. By engineering behavioural and temporal features, and applying targeted sampling strategies and feature selection, we aim to develop a more robust fraud detection model that captures the subtle behavioral indicators of fraudulent activity while addressing limitations in existing fraud detection methods. This repository details our exploratory findings, modelling approach, and evaluation results, contributing practical insights to the development of more effective and interpretable fraud detection systems.

## Objective
Our team aims to detect if a credit card transaction is fraudulent.

## Overall Repository Structure
```
📦Production
 ┣ 📜README.md                                        <- README file for production branch
 ┃
 ┣ 📜DataDictionary.txt                               <- Data dictionary for raw data
 ┃
 ┣ 📜requirements.txt                                 <- Package requirements to run files
 ┃
 ┣ 📂data
 ┃ ┣ 📜raw_data.csv                                   <- Raw data from data source
 ┃ ┣ 📜train_data.csv                                 <- Train data
 ┃ ┗ 📜test_data.csv                                  <- Test data
 ┃
 ┣ 📂EDA
 ┃ ┗ 📜EDA.ipynb                                      <- Exploratory data analysis for hypothesis and 
 ┃
 ┣ 📂features
 ┃ ┗ 📜feature_engineering.ipynb                      <- Feature engineering jupyter notebook
 ┃
 ┗ 📂models                                   
   ┣ 📂testing_models
   ┃ ┣ 📜logistic_regression_staging.ipynb            <- Logistic Regression model jupyter notebook
   ┃ ┣ 📜random_forest_staging.ipynb                  <- Random Forest model jupyter notebook
   ┃ ┗ 📜xgboost_staging.ipynb                        <- XGBoost model jupyter notebook
   ┃
   ┗ 📂final_model
     ┗ 📜final_model.ipynb                            <- Trained XGBoost model with Lasso feature selection
```

## Datasets used:
Synthetically generated dataset was obtained from [Hugging Face](https://huggingface.co/datasets/Nooha/cc_fraud_detection_dataset).
- Data dictionary can be found in `DataDictionary.txt`. The data dictionary is for the raw data features. Data dictionary for engineered features can be found in the report.

For our code, we referred to the following csv files, uploaded in [Google Drive](https://drive.google.com/file/d/1kYtxS3LhSl9DR_ONA7qdJCclRGx4t3bK/view?usp=drive_link).
- raw_data.csv (downloaded from hugging face)
- train_data.csv (after data cleaning and feature engineering)
- test_data.csv

## Our methodology
Utilising the labels in the original dataset, our project considered following supervised machine learning methods:
- Logistic Regression (baseline)
- Random Forest Classifier
- XGBoost Classifier

We chose XGBoost with Group Lasso as our final model for prediction of test cases.

## How to run the Project
Download files from above Google Drive link, add to `/data` folder

Running the files:
* `dev` branch:
    * `/src/EDA/EDA.ipynb`
    * `/src/features/feature_engineering.ipynb`
* `staging` branch:
    * `/models/<training model>.ipynb`
* `prod` branch:
    *  `/models/final_model.ipynb`
