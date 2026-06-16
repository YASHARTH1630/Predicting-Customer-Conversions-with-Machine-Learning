# Customer Conversion Prediction using LightGBM

## Overview

This project predicts whether a website visitor will convert into a customer using demographic, behavioral, and marketing-related data. The objective is to help businesses identify high-potential customers and improve marketing effectiveness through data-driven decision making.

## Problem Statement

Customer conversion is a key business metric. By analyzing user behavior, traffic sources, and purchase history, machine learning models can identify visitors who are more likely to convert, enabling targeted marketing and improved customer acquisition strategies.

## Dataset Features

The dataset contains information related to:

* Customer demographics
* Traffic source
* Device type
* Website engagement metrics
* Product views
* Previous purchases
* Discount interactions

## Feature Engineering

The following features were created to improve model performance:

* **Previous_Buyer** – Indicates prior purchase activity or discount interaction.
* **Engagement** – Combines user activity and time spent on the website.
* **Product_per_Minute** – Measures browsing intensity.
* **Purchase_Rate** – Historical purchases relative to product views.
* **Referral_Discount** – Captures interaction between referral traffic and discounts.
* **Time_On_Site_log** – Log transformation of session duration.

## Models Evaluated

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest
* XGBoost
* LightGBM

## Final Model Performance

### LightGBM (Hyperparameter Tuned)

| Metric   | Value  |
| -------- | ------ |
| Accuracy | 65.69% |
| F1 Score | 0.562  |

### Confusion Matrix

| Actual / Predicted | Non-Converter | Converter |
| ------------------ | ------------- | --------- |
| Non-Converter      | 1135          | 686       |
| Converter          | 206           | 573       |

## Key Insights

* Customer engagement is one of the strongest predictors of conversion.
* Users exposed to discounts are more likely to convert.
* Previous purchasing behavior significantly increases conversion probability.
* Referral traffic contributes positively to customer conversion.

## Tech Stack

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* LightGBM
* Joblib

## Project Structure

```text
customer-conversion-prediction/
│
├── requirements.txt
├── README.md
|──Dataset.zip
|   |──train.csv
|   |──public_test.csv
├── notebooks/
│   ├── lightgbm_model.pkl
│   ├── scaler.pkl
│   └── feature_columns.pkl
├──
│   └── experiment.ipynb
└── reports/
    └── project_report.txt
```

## Installation

```bash
pip install -r requirements.txt
```

## Business Impact

This project demonstrates how machine learning can be used to predict customer conversion, improve campaign targeting, optimize marketing spend, and support business decision-making through predictive analytics.
