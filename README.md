# Credit Card Fraud Prediction

## Context of Project
With the rise in popularity of cashless transactions, many users all around the world have switched towards using payment methods like credit cards. Given the digital nature of credit cards, it is pertinent that we focus on predicting potential fraudulent transactions and reduce potential losses incurred to customers, businesses and banks.

## Objective
Our team aims to detect if a credit card transaction is fraudulent.

## Repository Structure
```
📦Production
 ┣ 📜README.md
 ┃
 ┣ 📂data
 ┃ ┣ 📜raw_data.csv
 ┃ ┣ 📜train_data.csv
 ┃ ┗ 📜test_data.csv
 ┃
 ┗ 📜Model Run with Test Data.ipynb
   ┗ Trained Random Forest model with Lasso feature selection

📦Staging
 ┣ 📜README.md
 ┃
 ┣ 📂data
 ┃ ┣ 📜raw_data.csv
 ┃ ┣ 📜train_data.csv
 ┃ ┗ 📜test_data.csv
 ┃
 ┗ 📂Models
   ┣ 📜Logistic Regression
   ┣ 📜Random Forest
   ┗ 📜XGBoost

📦Development
 ┣ 📜README.md
 ┃
 ┗ 📂src
   ┣ 📂EDA
   ┃ ┗ 📜EDA.ipynb
   ┃
   ┗ 📂features
     ┗ 📜feature_engineering.ipynb
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

We chose Random Forest with Group Lasso as our final model for prediction of test cases.

## How to run the Project
- Download files from above Google Drive link, add to `/data` folder

- Steps of running the files:
    1. `dev` branch: EDA and Feature Engineering .ipynb files
    2. `staging` branch: Model training .ipynb files
    3. `prod` branch: Final model.ipynb <TO UPDATE>



        
