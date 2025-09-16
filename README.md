
# NAME:SUNIL KUMAR P.B.
# REGISTER NUMBER:212223040213
# EXNO2
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
   import pandas as pd 
   import numpy as np 
   import matplotlib.pyplot as plt 
   import seaborn as sns 
   df=pd.read_csv("/content/titanic_dataset.csv")
   df
   
<img width="1141" height="962" alt="image" src="https://github.com/user-attachments/assets/4cb2db61-7370-4306-9421-b43e2e6098a1" />

df.info()

<img width="810" height="660" alt="image" src="https://github.com/user-attachments/assets/f2bb221d-0db7-4fa3-83f2-f6b927603182" />

df.shape

<img width="192" height="70" alt="image" src="https://github.com/user-attachments/assets/45a0706a-170a-4804-9eb3-3c6ab1b4917b" />

import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv") 
df.set_index("PassengerId",inplace=True)
print(df.set_index)
<img width="880" height="952" alt="image" src="https://github.com/user-attachments/assets/04f9990b-3376-49a5-bcfa-f27924bceabb" />

df.describe()

<img width="834" height="388" alt="image" src="https://github.com/user-attachments/assets/e1a807bd-266b-45ff-b1da-ca50f71c116f" />

df.nunique()

<img width="257" height="403" alt="image" src="https://github.com/user-attachments/assets/3b0b63a9-da05-4ca7-a8d8-719538fd4fb1" />

df["Survived"].value_counts()
<img width="463" height="125" alt="image" src="https://github.com/user-attachments/assets/e7a420ce-5853-46a4-a292-f95215a912e2" />

per=(df["Survived"].value_counts()/df.shape[0]*100).round(2) per
<img width="486" height="114" alt="image" src="https://github.com/user-attachments/assets/a467e832-2daa-42e8-b2c8-bfe55a33f6d6" />

sns.countplot(data=df,x="Survived")
<img width="830" height="658" alt="image" src="https://github.com/user-attachments/assets/68ab23e3-15b6-4dda-a5b0-eb9c739491f2" />

df
<img width="834" height="340" alt="image" src="https://github.com/user-attachments/assets/fe5e39ab-f0d3-4623-a3a6-d7c1cba6b5b2" />
df.Pclass.unique()

<img width="256" height="76" alt="Screenshot 2025-08-29 130432" src="https://github.com/user-attachments/assets/1ddb922c-a864-450d-8d3c-6bbab05f61f9" />



df.rename(columns={'sex':'Gender'},inplace=True) df
<img width="803" height="293" alt="image" src="https://github.com/user-attachments/assets/ec2f2b7f-a925-486d-83a5-067926eab700" />

import seaborn as sns 
df=pd.read_csv("/content/titanic_dataset.csv") sns.catplot(x="Sex",col='Survived',kind="count",data=df,height=5, aspect=.7)
<img width="848" height="607" alt="image" src="https://github.com/user-attachments/assets/6251a6e7-0a5d-4d67-9609-f0f492162c5d" />

sns.catplot(x='Survived',hue='Sex',data=df,kind='count')
<img width="810" height="714" alt="image" src="https://github.com/user-attachments/assets/83589fe9-72b4-40ca-982d-2d9262bf35ea" />

df.boxplot(column='Age',by="Survived")
<img width="777" height="667" alt="image" src="https://github.com/user-attachments/assets/28add0d4-0f6f-4af9-98a8-46b8d4f23d82" />

sns.scatterplot(x=df['Age'],y=df["Fare"])
<img width="826" height="647" alt="image" src="https://github.com/user-attachments/assets/d556d43e-6e93-4c13-bc8c-569d474391fa" />

import matplotlib.pyplot as plt fig,ax1=plt.subplots(figsize=(8,5)) pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=df)
<img width="808" height="544" alt="image" src="https://github.com/user-attachments/assets/46bbd345-a4c2-4943-a163-63c3a561b8dd" />

sns.catplot(data=df,col='Survived',x='Sex',hue='Pclass',kind='count')
<img width="831" height="396" alt="image" src="https://github.com/user-attachments/assets/79f97970-6a26-43b0-9c34-ecff97b7f6b6" />

import seaborn as sns corr=df.corr() sns.heatmap(corr,annot=True)
<img width="853" height="748" alt="image" src="https://github.com/user-attachments/assets/d20578d1-fc38-40a9-9695-019c9155180d" />

sns.pairplot(df)
<img width="805" height="469" alt="image" src="https://github.com/user-attachments/assets/11edfa7c-2917-4ea2-892d-2e923e714732" />

# RESULT
    Code are sucessfully executed.     
