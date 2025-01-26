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
python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
Step 2: Load the DataFrame
python
dataframe = pd.read_csv("Zomato data.csv")
print(dataframe.head())
Step 3: Clean the Data
Convert the "rate" column to float by removing the denominator:
python
def handleRate(value):
    value = str(value).split('/')
    return float(value[0])

dataframe['rate'] = dataframe['rate'].apply(handleRate)
Step 4: Check for Null Values
python
print(dataframe.info())
No NULL values were found in the dataset.
Analysis Questions
Do more restaurants provide online delivery or offline services?
Use count plots to visualize online vs offline orders.
Which types of restaurants are most favored by the public?
Analyze the listed_in(type) column with count plots and group by votes.
What price range is preferred by couples for dining?
Examine the approx_cost(for two people) column with count plots.
Do online orders receive higher ratings than offline orders?
Create box plots to compare ratings based on order type.
Visualizations and Conclusions
Restaurant Type Preferences: Most restaurants fall under the dining category.
Online vs Offline Orders: Most restaurants do not accept online orders.
Rating Distribution: Most restaurants have ratings between 3.5 and 4.
Couples' Preferred Price Range: Most prefer restaurants costing around 300 rupees for two.
Conclusion
This analysis provides insights into customer preferences regarding restaurant types, ordering methods, and pricing. The findings can help restaurant owners tailor their services to effectively meet customer demands.
