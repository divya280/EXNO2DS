# EXNO2DS
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
### NAME: V. DIVYASHREE
### REGISTER NO: 212223230051
```
import pandas as pd
df=pd.read_csv('/content/titanic_dataset.csv')
df
```
![image](https://github.com/user-attachments/assets/3908081e-1004-4e6d-81fa-47ff95ee0c35)
```
df.isnull().sum()
```
![image](https://github.com/user-attachments/assets/65acfb05-f368-4a0f-852a-c374fdfcb865)
```
df.dropna(inplace=True)
```
![image](https://github.com/user-attachments/assets/a38806b7-c830-4540-8135-3797ee33a065)
```
df.isnull().sum()
```
![image](https://github.com/user-attachments/assets/664d2230-b6d4-4c6e-8959-3b1ec807ffde)
```
df.info()
```
![image](https://github.com/user-attachments/assets/3dc9a215-e903-4e82-83f2-499cf45ffed5)

```
df.set_index("PassengerId",inplace=True)
df.describe()
```
![image](https://github.com/user-attachments/assets/8646e7ec-94bc-4d3c-ae44-050acad1aef5)
```
df
```
![image](https://github.com/user-attachments/assets/3d034bb3-3810-42c5-addb-4b70d9751034)
```
df.nunique()
```
![image](https://github.com/user-attachments/assets/5173106d-92df-461c-9a19-13dd64ebfdc2)
```
df["Survived"].value_counts()
```
![image](https://github.com/user-attachments/assets/f7c5f6fe-283c-4226-a629-f7a185816b3d)

```
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```
![image](https://github.com/user-attachments/assets/6206d5c0-17b4-4ce8-b6f0-0b79131e6c57)
```
import matplotlib.pyplot as plt
import seaborn as sns

sns.countplot(data=df,x="Survived")
```
![image](https://github.com/user-attachments/assets/189b02be-ddf2-409f-b63b-b3149360ef22)
```
df.Pclass.unique()
```
![image](https://github.com/user-attachments/assets/e646262e-c8fc-4b31-83b5-8b4bee705151)

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```
![image](https://github.com/user-attachments/assets/705ab247-c4c2-4be5-8933-f90ba7120be2)
```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
```
![image](https://github.com/user-attachments/assets/2df7950a-462d-4950-9df9-0387fe2ae768)
```
sns.catplot(data=df,col = "Survived",x="Gender",hue="Pclass",kind="count")
```
![image](https://github.com/user-attachments/assets/9b3beb07-e953-4d33-b9bc-451b36518e9b)





# RESULT
        The Exploratory Data Analysis on the given data set has been performed.
