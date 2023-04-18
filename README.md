# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd import numpy as np import seaborn as sns df = pd.read_csv("Loan_data.csv") print(df) df.info() df.isnull().sum() df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0]) df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0]) df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0]) df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].median()) df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median()) df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median()) df.isnull().sum()

```
# OUPUT

