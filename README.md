Project Overview
This project aims to analyze Zomato restaurant data using Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn. The analysis focuses on understanding restaurant preferences, online ordering trends, and customer ratings.
Libraries Used
NumPy: For efficient numerical computations and handling large datasets.
Pandas: To manage and manipulate data easily with DataFrames.
Matplotlib: For creating high-quality visualizations like plots and charts.
Seaborn: For generating informative statistical graphics with a high-level interface.
Getting Started
Clone the repository: Download the project files from GitHub.
Install required libraries:
bash
pip install pandas numpy matplotlib seaborn
Load the dataset: Place the Zomato dataset CSV file in the project folder.
Data Preparation
Step 1: Import Libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
Step 2: Load the DataFrame
dataframe = pd.read_csv("Zomato data.csv")
print(dataframe.head())
Step 3: Clean the Data
Convert the "rate" column to float by removing the denominator:
def handleRate(value):
    value = str(value).split('/')
    return float(value[0])

dataframe['rate'] = dataframe['rate'].apply(handleRate)

Step 4: Check for Null Values

print(dataframe.info())
