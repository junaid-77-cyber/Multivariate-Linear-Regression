# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.

## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:
### Step1
Start and import the required libraries — pandas for data handling and linear_model from sklearn for regression.

### Step2
Load the dataset from the CSV file using pd.read_csv() and store it in a DataFrame df.

### Step3
Select features and target:
Set X = [['Weight', 'Volume']] (independent variables).
Set y = ['CO2'] (dependent variable).

### Step4
Create a Linear Regression model using linear_model.LinearRegression() and store it in regr.

### Step5
Train the model using regr.fit(X, y) and display the model’s coefficients and intercept.

### Step6
Predict CO2 value for a given weight and volume using regr.predict() and print the predicted result.

## Program:
```
# Developed By: Junaid Sardar S
# Register Number: 212224100028

import pandas as pd
from sklearn import linear_model
df = pd.read_csv(r'C:\Users\Junaid Sardar\Downloads\car (1).csv')
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
print('Predicted CO2 for the corresponding weight and volume:',predictedCO2)
```
## Output:

![alt text](<Screenshot 2025-10-16 090744.png>)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.