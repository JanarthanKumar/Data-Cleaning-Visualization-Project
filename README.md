

Data Cleaning & Visualization Project

Overview
This project demonstrates a complete data preprocessing and exploratory data analysis (EDA) pipeline using Python. It takes raw employee/sales data from an Excel file, performs rigorous data cleaning, handles missing values and outliers, transforms categorical data, and generates insightful visualizations using pandas and matplotlib.

Prerequisites
To run this notebook, you will need Python installed along with the following libraries:

pandas

matplotlib

openpyxl (required by pandas to read Excel files)

You can install the required dependencies using:

Bash
pip install pandas matplotlib openpyxl
Dataset
The initial dataset (data_sales.xlsx) contains employee records with the following columns:

Name: Employee name

Age: Employee age

Salary: Employee salary

Join_Date: The date the employee joined the company

Department: Department name (e.g., HR, Finance, IT)

Project Workflow
1. Data Cleaning
Missing Values Handling:

Replaced missing Age values with the median age.

Replaced missing Salary values with the mean salary.

Dropped records with missing Join_Date values.

Data Standardization:

Standardized Join_Date into a uniform DD/MM/YYYY format.

Stripped leading/trailing whitespaces and converted all text data (strings) to lowercase to ensure consistency.

Duplicate Removal: Identified and dropped duplicate records based on the Name and Age columns.

Outlier Detection: Filtered out salary outliers using the Interquartile Range (IQR) method.

2. Data Transformation
One-Hot Encoding: Converted the categorical Department column into binary dummy variables (e.g., Department_HR, Department_IT) for easier analysis.

Export: Saved the fully cleaned and transformed dataset to a new file named cleaned_data.csv.

3. Data Visualization
After cleaning the data, the project generates several visualizations to explore the dataset:

Bar Chart: Department Distribution (Count of employees in HR vs. IT).

Histogram: Salary Distribution to visualize the frequency of different salary ranges.

Line Plot: Salary trends based on Age.

Scatter Plot: A color-coded scatter plot of Salary vs. Age separated by Department (HR in Blue, IT in Green).

How to Use
Clone the repository to your local machine.

Ensure your input data file (data_sales.xlsx) is placed in the correct path or update the file path in the notebook.

Open Data Cleaning & Visualization Project.ipynb using Jupyter Notebook or any compatible IDE (like VS Code).

Run all cells sequentially to execute the data cleaning steps, export the cleaned CSV, and view the visual plots.
