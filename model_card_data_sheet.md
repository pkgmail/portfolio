# Model card for "Heart Disease Risk Prediction"

Jump to section:

- [Model details](#model-details)
- [Intended use](#intended-use)
- [Factors](#factors)
- [Metrics](#metrics)
- [Evaluation data](#evaluation-data)
- [Training data](#training-data)
- [Quantitative analyses](#quantitative-analyses)
- [Ethical considerations](#ethical-considerations)
- [Caveats and recommendations](#caveats-and-recommendations)

## Model details

Model trained using K-Nearest-Neighbor to predict the risk of heart disease based on various factors including lifestyle choices.

Author: Prashant Kumar

Date: 04-Jun-2024

Version: 1.0

Model: K Nearest Neighbor

License: Issued under MIT Licence


## Intended use


### Primary intended uses
 - Intended to predict the risk of heart disease and providing feedback to authors.

### Primary intended users
 - Users with a specific interest in research and prediction using machine learning. 
 - Users in medical background with a specific interest in predictive analysis.

### Out-of-scope use cases
 - Not intended to make specific judgments about individuals or demography.
 - Not intended to treat or diagnose without a medical professional.

## Factors

The model considers various demographic, lifestyle, and clinical factors such as age, sex, smoking status, medical history, and vital statistics (e.g., blood pressure, cholesterol levels) to predict heart disease risk. These factors are crucial for accurate risk stratification and personalized health assessments.

### Relevant factors
The model considers various demographic, lifestyle, and clinical factors such as age, sex, smoking status, medical history, and vital statistics (e.g., blood pressure, cholesterol levels) to predict heart disease risk

### Evaluation factors
Various demographic, lifestyle, and clinical factors such as age, sex, smoking status, medical history, and vital statistics.

## Metrics



### Model performance measures
 - Accuracy: Proportion of correctly predicted instances, indicating overall model performance.

 - Confusion Matrix: Breakdown of true positives, true negatives, false positives, and false negatives, showing the model's classification ability.

### Decision thresholds
Threshold is a configurable parameter designed to adjust the levels of false negatives to an acceptable level.

### Approaches to uncertainty and variability

## Evaluation data

### Datasets
The original dataset downloaded from Kaggle - https://www.kaggle.com/datasets/mahdifaour/heart-disease-dataset/data

 - sex: This column represents the gender of the individuals (female- male).

 - age: This column represents the age of the individuals in the dataset. Age is a crucial factor in assessing the risk of coronary heart disease.

 - education: This column represents the level of education of the individuals. It could be coded using categorical values indicating different levels of education attainment.

 - smokingStatus: This column likely represents the smoking status of the individuals, indicating whether they are smokers(yes), non-smokers(no).

 - cigsPerDay: If an individual is a smoker, this column represents the number of cigarettes smoked per day.

 - BPMeds: This column indicates whether the individual is taking blood pressure medications (binary: 0 for not taking, 1 for taking).

 - prevalentStroke: This column indicates whether an individual has had a stroke prior to the study (binary: 0 for no, 1 for yes).

 - prevalentHyp: This column indicates whether an individual has hypertension (binary: 0 for no, 1 for yes).

 - diabetes: This column indicates whether an individual has diabetes (binary: 0 for no, 1 for yes).

 - totChol: This column represents the total cholesterol level of the individuals.

 - sysBP: This column represents the systolic blood pressure of the individuals.

 - diaBP: This column represents the diastolic blood pressure of the individuals.

 - BMI: This column represents the Body Mass Index (BMI) of the individuals, which is a measure of body fat based on height and weight.

 - heartRate: This column represents the resting heart rate of the individuals.

 - glucose: This column represents the fasting blood glucose level of the individuals.

 - CHDRisk: This column likely represents the Ten-Year Coronary Heart Disease (CHD) Risk for each individual, which is the target variable that you may want to predict or analyze.

### Motivation
For research and learning purpose.

### Preprocessing
Preprocessing done to remove missing rows and split into training and test datasets in 80:20 ratio.

## Training data

Review section 4.6 of the [model cards paper](https://arxiv.org/abs/1810.03993).

## Quantitative analyses
### Model Performance Metrics
Accuracy: 0.85 with cross validation on training set.
Accuracy: 0.73 with an adjustable threshold of 0.33 on the test set.
True Positives (TP): 45
True Negatives (TN): 495
False Positives (FP): 118
False Negatives (FN): 73


## Ethical considerations
The model does not aim to diagnose or detect any diseases. It is purely aimed at research and it is not intended to make specific judgments about individuals or demography.

## Caveats and recommendations
Only a small set of data has been used to train/test and it is recommended that a large dataset be used to test the model.