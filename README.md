# heart_disease_

https://www.kaggle.com/datasets/mirzahasnine/heart-disease-dataset?resource=download
What is heart disease?
Heart disease encompasses several heart conditions. The most common type of heart disease in the United States is coronary artery disease (CAD), which affects the blood flow to the heart. Decreased blood flow can cause a heart attack.


Key risk factors for heart disease include high blood pressure, high blood cholesterol levels, and smoking. About half of people in the United States (47%) have at least one of these three risk factors. Several other medical conditions and lifestyle choices can also put people at a higher risk for heart disease, including diabetes, overweight and obesity, unhealthy diet, physical inactivity, excessive alcohol consumption.

Cardiac rehabilitation (rehab) is an important program for anyone recovering from a heart attack, heart failure, or some types of heart surgery. Cardiac rehab is a supervised program that includes physical activity, education about healthy living, including healthy eating, taking medicine as prescribed, and ways to help you quit smoking, counseling to find ways to relieve stress and improve mental health.

Exploratory Data Analysis (EDA) Objective

The goal of this exploratory data analysis (EDA) is to investigate heart stroke data in relation to demographic, health, and behavioral data. 

EDA Overview

This dataset comprises information from 4,238 individuals, encompassing demographic details (age and education levels from “uneducated” to “postgraduate”),  behavioral factors (smoking habits, number of daily cigarettes, and adherence to blood pressure medications) and health-related data (body-mass index, diabetes presence, hypertension presence, cholesterol levels, glucose levels, systolic and diastolic blood pressure, heart rate, and stroke and heart stroke history). 

Approximately 600 entries contained missing data, primarily in education and glucose level columns. 

The analysis revealed that the “uneducated” group constitutes nearly 50% of the dataset. The group is reported to have the highest mean age (51 years) compared to primary school graduates (47 years), the graduates (48.9 years) and postgraduates (48.1 years). Additionally, "uneducated” group exhibits a higher prevalence of hypertension (35%) compared to the “postgraduate” group (27%) and diabetes (3.7%) compared to the “postgraduate” group (2.1%). This group also registers the highest mean values of blood pressure, glucose levels and increased risks of stroke and heart stroke.

While the “uneducated” group demonstrates the highest overall adherence to blood pressure treatment, when evaluated in relation to the mean number of prevalent cases of hypertension, their adherence rate appears to be the lowest. 

In terms of gender-based differences, the female participants in the group demonstrated higher average cholesterol levels (255 compared to 240) and glucose levels (86 compared to 83), as well as higher blood pressure (255 compared to 240) and an increased BMI (28 compared to 27). However, despite these higher risky dietary behaviors, female participants exhibited a lower risk of heart attack. This lower risk can be attributed to a specific indicator in this data set: adherence to blood pressure medication and treatment. Notably, adherence to blood pressure treatment was significantly higher among women at 12.7% compared to  7.3% among men. 

The correlation analysis indicates a positive though weak linear correlation between the risk of a heart stroke and age, hypertension, blood pressure, glucose level, while education displays a negative correlation. 

Analysis of High Blood Pressure Group

A subgroup  analysis of individuals with systolic blood pressure of 140 and higher and diastolic blood pressure of 90 and higher highlights that the “uneducated” group has the highest risk of diabetes (0.070) compared to the “postgraduate” group (0.014) and the highest mean or maximum values of blood pressure, mean BMI, mean glucose levels. The group carries the higher risk of stroke (2.6%) compared to the postgraduate group (0). Conversely, the “postgraduate” group has the highest risk of heart stroke of 0.35 compared with 0.22 in the group with primary education and 0.28 of the “uneducated” group. 

Machine Learning Insights

Using the XGBoost Classifier algorithm on the entire dataset, I determined that systolic blood pressure, education, number of cigarettes per day and glucose levels are the strongest predictors of heart disease. Notably, the number of cigarettes per day, although weakly correlated in linear analysis, emerged as one of the most powerful predictors in the XGBoost model. 

Logistic Regression

The logistic Regression algorithm demonstrated that the strongest positive predictors of a heart attack is gender (being a male), diabetes diagnosis and age. The strongest negative predictors were education and adherence to blood pressure medication. 

Summary and Recommendations

In summary, education emerges as a significant determinant of heart health. It exhibits negative correlations with several behavioral indicators, including adherence to BP medicines, diabetes, cholesterol, BMI, and glucose level. To promote heart health, preventive education initiatives should focus on males over 50 with limited education, employing. a comprehensive program that emphasizes healthy diets, control of blood pressure and glucose levels. 


Analysis of the predictive probability of the model:

The predict_proba method of the logistic regression model with predicted probability of 0.2, identifies more true positive cases than with predicted probability of 0.5 (180 compared to 36) and decreases the number of false negatives from 278 to 134. This level of probability  increases recall or sensitivity of the model in identifying true positive cases from 11% to 57%.  On the other hand, this change in probability decreases the number of true negatives from 1725 to 1390. The decision about the predicted probability value will be made based on the objective of the model, whether it is to find more true positives or true negatives. 

In addition, I created a model  that shows how each determinant changer the risk of a heart attack



