# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1: Create a new file in jupyter notebook.

### STEP 2: Upload the given csv file.
### STEP 3: Write codes for Data Analysis (EDA).
### STEP 4: Plot the result in various formats.
### STEP 5: End the program.



# CODE:
~~~
Developed By : DHANUSH S
Register Number : 212221230020

import pandas pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="Sex",data=df)
df.info()
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~
# OUTPUT :
![gitlogo](hulk-01.png)
![gitlogo](hulk-02.png)
![gitlogo](hulk-03.png)
![gitlogo](hulk-04.png)
![gitlogo](hulk-05.png)
![gitlogo](hulk-06.png)
![gitlogo](hulk-07.png)
![gitlogo](hulk-08.png)
![gitlogo](hulk-09.png)
![gitlogo](hulk-10.png)
![gitlogo](hulk-11.png)
![gitlogo](hulk-12.png)
![gitlogo](hulk-13.png)
![gitlogo](hulk-14.png)


 # Result:
Thus the data of the dataset is analyzed using Exploratory data analysis.