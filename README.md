# AI-Based Predictive Maintenance Using Machine Learning

## Project Overview

This project focuses on building a machine learning-based predictive maintenance system to predict machine failure using industrial machine-condition data. Predictive maintenance is important in real-world industries because unexpected machine failure can cause production delays, downtime, and increased maintenance costs.

The objective of this project is to analyze machine operating conditions such as temperature, rotational speed, torque, tool wear, and machine type, and use machine learning to identify whether a machine is at risk of failure.

## Problem Statement

In industrial environments, machines often generate operational data through sensors and monitoring systems. However, machine failures are usually rare and difficult to detect early. This project aims to develop a classification model that can predict possible machine failure before it occurs, allowing maintenance teams to take early action.

## Dataset

The project uses the AI4I 2020 Predictive Maintenance Dataset. The dataset contains machine-related features such as:

* Air temperature
* Process temperature
* Rotational speed
* Torque
* Tool wear
* Machine type
* Machine failure label

The target variable is:

```text
Machine failure
```

Where:

```text
0 = No failure
1 = Machine failure
```

## Tools and Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Random Forest Classifier
* Logistic Regression
* Joblib
* GitHub

## Project Workflow

The project was completed using the following steps:

1. Data loading and understanding
2. Data cleaning
3. Exploratory Data Analysis
4. Feature engineering
5. Model training
6. Model evaluation
7. Threshold tuning
8. Feature importance analysis
9. Final prediction function
10. Model saving for future use

## Exploratory Data Analysis

The dataset was analyzed to understand the relationship between machine operating conditions and failure occurrence.

Important findings from the analysis:

* Failed machines generally had higher torque.
* Failed machines had higher tool wear.
* Failed machines showed lower rotational speed compared to non-failed machines.
* Machine type also showed differences in failure rate.
* Type L machines showed the highest failure rate among the machine types.

## Feature Engineering

New features were created to improve model understanding and predictive performance.

Engineered features include:

```text
Temperature difference = Process temperature - Air temperature
Power indicator = Torque × Rotational speed
Torque per speed = Torque / Rotational speed
```

These features helped represent machine load, temperature variation, and operating intensity more effectively.

## Machine Learning Models

Two machine learning models were trained and compared:

1. Logistic Regression
2. Random Forest Classifier

The Random Forest model was selected as the final model because it performed better overall and provided strong results for machine failure prediction.

## Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

In predictive maintenance, recall is very important because missing an actual machine failure can lead to unexpected downtime and maintenance cost.

## Final Model Results

The final selected model was:

```text
Random Forest Classifier with threshold 0.30
```

Final model performance:

| Metric    |  Score |
| --------- | -----: |
| Accuracy  | 99.05% |
| Precision | 88.89% |
| Recall    | 82.35% |
| F1-score  | 85.49% |

The prediction threshold was adjusted from 0.50 to 0.30 to improve failure detection. This increased recall and made the model more suitable for predictive maintenance use cases.

## Feature Importance

The Random Forest model identified the most important features for predicting machine failure.

Top important features:

1. Tool wear
2. Torque per speed
3. Rotational speed
4. Power indicator
5. Torque

This shows that machine usage, load, and speed-related behavior are important factors in predicting failure risk.

## Practical Use

A prediction function was created to estimate the failure risk of a new machine based on input values such as:

* Machine type
* Air temperature
* Process temperature
* Rotational speed
* Torque
* Tool wear

The model returns a failure probability and classifies the machine as either:

```text
Machine is at risk of failure
```

or

```text
Machine is not at risk of failure
```

## Files in This Project

```text
predictive-maintenance-ai/
│
├── Predictive_Maintenance_AI_Project.ipynb
├── predictive_maintenance_random_forest_model.pkl
├── feature_columns.json
├── final_threshold.json
├── predictive_maintenance_test_results.csv
├── README.md
```

## Conclusion

This project developed a predictive maintenance machine learning system using industrial machine-condition data. The analysis showed that tool wear, torque, rotational speed, and engineered load-based features are important indicators of machine failure.

The final Random Forest model with threshold tuning achieved strong performance and can support early failure detection. This project demonstrates practical skills in data analysis, feature engineering, machine learning, model evaluation, and real-world industrial AI applications.
