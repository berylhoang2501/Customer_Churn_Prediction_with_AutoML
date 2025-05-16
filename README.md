# Customer Churn Prediction

This project uses **AutoML** (PyCaret) to predict customer churn on the Telco Customer Churn dataset from Kaggle. The goal is to identify customers likely to leave the service, enabling businesses to implement retention strategies.


![FINAL_PROJECT](https://github.com/user-attachments/assets/e5610af7-caf3-4b02-9a83-5fa29f1330e1)


## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [License](#license)

## Project Overview
The project leverages **PyCaret**, an AutoML framework, to train and evaluate machine learning models for predicting customer churn. The LightGBM model is used for final predictions, with key features analyzed to understand churn drivers.

<img width="659" alt="Ảnh màn hình 2025-05-16 lúc 15 07 32" src="https://github.com/user-attachments/assets/1b45a1e6-871a-4222-8488-0cb586bb65f0" />


**Objectives**:
- Predict customer churn with high accuracy.
- Identify key factors influencing churn (e.g., financial metrics, tenure).
- Provide actionable insights for retention strategies.

## Dataset
The dataset used is the **Telco Customer Churn** dataset from Kaggle:
- `WA_Fn-UseC_-Telco-Customer-Churn.csv`: Contains customer information, including demographics, services, billing, and churn status.

**Note**: Due to data sensitivity, the dataset is not included. Download it from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) or contact the repository owner for access.

## Installation
1. Clone the repository:
```
git clone https://github.com/berylhoang2501/Customer_Churn_Prediction_with_AutoML
cd Customer-Churn-Prediction
```

2. Create a virtual environment and install dependencies:
   
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

## Usage

Run the Jupyter Notebook to train and evaluate the AutoML model:
```
jupyter notebook notebooks/Customer_Churn_Prediction_with_AutoML.ipynb
```

## Results

- Model Performance (LightGBM on test set):

Accuracy: 0.848

Precision: 0.843

Recall: 0.855

F1 Score: 0.849 (after tuning)

<img width="265" alt="Ảnh màn hình 2025-05-16 lúc 15 18 29" src="https://github.com/user-attachments/assets/025f4ed0-3169-4956-81b1-69d4629d057d" />

- F1 Score Comparison:

<img width="610" alt="Ảnh màn hình 2025-05-16 lúc 15 15 40" src="https://github.com/user-attachments/assets/05e8e9be-ca2b-4c96-934f-d500ece03c58" />

Tuned model: 0.8473 (average F1 Score).

Initial model: 0.8451 (average F1 Score).

Observation: The tuned model slightly outperforms the initial model based on F1 Score, indicating improved balance between precision and recall.

## Key Findings:

- Financial Metrics: MonthlyCharges and TotalCharges are the most influential features, indicating pricing strategies significantly impact churn. Adjusting pricing or offering discounts for high-cost customers could reduce churn.

- Tenure: Longer customer tenure reduces churn likelihood. Loyalty programs or enhanced service value can extend customer retention.
Actionable Insights: Focus on financial incentives and loyalty programs to retain customers.
