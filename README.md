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
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```
#OUPUT
 ![1](https://user-images.githubusercontent.com/121490523/227698521-4fe0ebf0-0c21-4199-88f5-8465eab4cada.png)
![2](https://user-images.githubusercontent.com/121490523/227698535-c38d66a4-53a2-46cc-bf55-521908e944ad.png)
![3](https://user-images.githubusercontent.com/121490523/227698545-6e9ccce0-3e01-43fe-8509-f5bc180c76ac.png)
![4](https://user-images.githubusercontent.com/121490523/227698557-9ad5fae6-2e52-4455-a79a-cc2188973291.png)
![5](https://user-images.githubusercontent.com/121490523/227698560-5f94ae02-de60-4370-a98e-21705768e93d.png)
![6](https://user-images.githubusercontent.com/121490523/227698564-d9896853-139c-4b6d-9fc4-96ed1dcd860d.png)
![7](https://user-images.githubusercontent.com/121490523/227698570-5bf9a9dd-018f-45ee-9ab2-42c7b89ed349.png)

#RESULT
Data cleaning for given data was cleaned and saved to file
