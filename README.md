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
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)

df.head(5)

df.tail(5)

df.describe()

df.info()

df.isnull().sum()

df=df[~df.duplicated()]
print(df)

df['Gender'].fillna(value=df['Gender'].mode())

df['LoanAmount'].fillna(value=df['LoanAmount'].median())
```
# OUPUT :
![kavyaa2](https://user-images.githubusercontent.com/119557910/229698726-19062cf1-cb22-48f1-a96a-25d9d5c1ed8c.png)
![ds5](https://user-images.githubusercontent.com/119557910/229698802-67207b8c-2a14-4330-9347-6cb9a35d2c10.png)
![ds6](https://user-images.githubusercontent.com/119557910/229698882-e9a84f69-82fb-4bdc-a553-67de35275e94.png)
![ds7](https://user-images.githubusercontent.com/119557910/229698939-1899914d-9b83-4b2b-9b1e-c1dc782ebd81.png)

##RESULT:
Thus the given data is read cleansed and cleaned.


