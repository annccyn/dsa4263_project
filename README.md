# Credit Card Fraud Prediction

## Context of Project
With the rise in popularity of cashless transactions, many users all around the world have switched towards using payment methods like credit cards. Given the digital nature of credit cards, it is pertinent that we focus on predicting potential fraudulent transactions and reduce potential losses incurred to customers, businesses and banks.

## Objective
Our team aims to detect if a credit card transaction is fraudulent.

## Overall Repository Structure
```
📦Production
 ┣ 📜README.md                                        <- README file for production branch
 ┃
 ┣ 📂data
 ┃ ┣ 📜raw_data.csv                                   <- Raw data from data source
 ┃ ┣ 📜train_data.csv                                 <- Train data
 ┃ ┗ 📜test_data.csv                                  <- Test data
 ┃
 ┣ 📂features
 ┃ ┗📜feature_engineering.ipynb                       <- Feature engineering jupyter notebook
 ┃
 ┗ 📜Model Run with Test Data.ipynb                   <- Trained Random Forest model with Lasso feature selection

📦Staging
 ┣ 📜README.md                                        <- README file for production branch
 ┃
 ┣ 📂data
 ┃ ┣ 📜raw_data.csv                                   <- Raw data from data source
 ┃ ┣ 📜train_data.csv                                 <- Train data
 ┃ ┗ 📜test_data.csv                                  <- Test data
 ┃
 ┣ 📂features
 ┃ ┗📜feature_engineering.ipynb                       <- Feature engineering jupyter notebook
 ┃
 ┗ 📂Models
   ┣ 📜Logistic Regression                            <- Logistic Regression model jupyter notebook
   ┣ 📜randomforest.ipynb                             <- Random Forest model jupyter notebook
   ┗ 📜xgboost.ipynb                                  <- XGBoost model jupyter notebook

📦Development
 ┣ 📜README.md
 ┃
 ┗ 📂src
   ┣ 📂EDA
   ┃ ┗ 📜EDA.ipynb                                    <- Exploratory data analysis for hypothesis and visualisation
   ┃
   ┗ 📂features
     ┗ 📜feature_engineering.ipynb                    <- Feature engineering jupyter notebook
```

## Datasets used:
Synthetically generated dataset was obtained from [Hugging Face](https://huggingface.co/datasets/Nooha/cc_fraud_detection_dataset).
- Data dictionary can be found in `DataDictionary.txt`.


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
    *  `/src/final_model.ipynb`
