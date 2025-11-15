# Data-Analysis-Project-
Graduation Project: Data Cleaning

This project focuses on cleaning and preparing two datasets as part of a graduation project. The cleaning steps are documented in the Graduation_Project_Cleaning(Finished).ipynb Jupyter Notebook.

Datasets Used

banking_financial_data.csv: Contains financial transaction data.

customer_demographics_data.csv: Contains demographic information about customers.

Dependencies

The cleaning process primarily uses the pandas library in Python.

Cleaning Process

1. Banking Financial Data (banking_financial_data.csv)

This dataset was loaded into a pandas DataFrame named df1.

Initial Inspection: The data was inspected using .shape, .info(), and .describe() to understand its structure and identify preliminary issues.

Missing Data:

df1.isnull().sum() revealed 1002 missing values in the Transaction_ID column.

Action: All rows containing any missing values were removed using df1.dropna().

Duplicate Data:

df1.duplicated().sum() was used to check for duplicate rows. No duplicates were initially found.

Action: df1.drop_duplicates() was run as a final measure to ensure no duplicates remained after cleaning.

2. Customer Demographics Data (customer_demographics_data.csv)

This dataset was loaded into a pandas DataFrame named df2.

Initial Inspection: The data was inspected using .shape, .info(), and .describe().

Missing Data:

df2.isnull().sum() revealed 49 missing values in the Annual_Income column.

Action: Missing Annual_Income values were imputed using the mean of the column (df2['Annual_Income'].fillna(df2['Annual_Income'].mean())).

Duplicate Data:

df2.duplicated().sum() was used to check for duplicate rows. No duplicates were found.

Summary

After these steps, both DataFrames (df1 and df2) are cleaned of missing values and duplicates, making them suitable for further analysis.
