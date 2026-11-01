Simple Linear Regression Project (Advertising Data)
A machine learning project built with Python and Scikit-Learn to perform Simple Linear Regression, predicting sales based on TV advertising budgets using a sample dataset.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

🚀 Features
📊 Loads and inspects CSV advertising datasets using pandas.   
📉 Calculates correlation matrices to analyze relationships between features.   
📈 Implements Simple Linear Regression via scikit-learn's LinearRegression model.   
📐 Extracts model parameters such as the intercept ($\beta_0$) and regression coefficient ($\beta_1$).   
📊 Evaluates performance using Mean Absolute Error (MAE) and visualizes the best-fit regression line over scatter plots.   

🛠️ Tech StackLanguage: 
- Python 3.xLibraries:pandas (Data manipulation and CSV reading)   
- numpy (Numerical operations)   
- scikit-learn (Machine learning modeling and metrics evaluation)   
- matplotlib (Data visualization and plotting)

⚙️ Getting Started
Prerequisites
Make sure you have Python installed along with the required libraries:
pip install pandas numpy scikit-learn matplotlib

Installation & Execution
1. Place your dataset file (Advertising1.csv) in the working directory.   
2. Run the script or execute the workflow blocks in your Jupyter Notebook / Google Colab.

📖 Usage
Here is the core code snippet used to load the data, fit the simple linear regression model, and calculate predictions:

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn import metrics

# Load dataset
df = pd.read_csv("Advertising1.csv")

# Define independent (x) and dependent (y) variables
x = df[['TV']]
y = df['Sales']

# Initialize and fit the Linear Regression model
lrm = LinearRegression()
lrm.fit(x, y)

# View model intercept and coefficients
print("Intercept:", lrm.intercept_)
print("Coefficient:", lrm.coef_)

# Make predictions
predictions = lrm.predict(x)

# Evaluate model using Mean Absolute Error
mae = metrics.mean_absolute_error(y, predictions)
print("Mean Absolute Error:", mae)
