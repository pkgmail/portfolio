# Heart Disease Risk Prediction

In this repo, we predict the risk of heart disease based on various factors. It uses dataset from https://www.kaggle.com/datasets/mahdifaour/heart-disease-dataset/data?select=Heart_Disease+%281%29.csv. It predicts the risk (CHDRisk) of getting heart disease based on:

 - sex
 - age
 - education
 - smokingStatus
 - cigsPerDay
 - BPMeds
 - prevalentStroke
 - prevalentHyp
 - diabetes
 - totChol
 - sysBP
 - diaBP
 - BMI
 - heartRate
 - glucose

The model is trained using K-Nearest-Neighbour algorithm with K-Fold and GridSearchCV to choose the best hyperparameters. 

## Installation
`pip install -r requirements.txt`  
Run the above command to install the required packages


## Execution
### Data preprocessing

The original dataset is stored under the data directory - Heart_Disease.csv. It has been preprocessed to clean and split into training and test datasets (Heart_Disease_Train.csv and Heart_Disease_Test.csv) with 80:20 ratio. These files could be generated again by running Heart_Disease_Preprocessing.ipynb Jupyter Notebook. Note that random seed has been kept at 42 throughout the code.

### Prediction
Heart_Disease.ipynb Jupyter Notebook scales the training data, uses GridSearchCV and KFold to find the best hyperparameters for K-Nearest-Neighbours. Accuracy has been chosen as the performance metric.
The best model is used for prediction on the test dataset. Confusion Matrix is plotted for viewing the performance on the test dataset.

The following hyperparameters have been chosen for tuning. If required, more could be added to the dictionary.

 - n_neighbors
 - weights
 - p (Manhattan distance or Euclidean distance)



