<H3>Sree Niveditaa Saravanan</H3>
<H3>212223230213</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
### STEP 1:
Importing the libraries<BR>
### STEP 2:
Importing the dataset<BR>
### STEP 3:
Taking care of missing data<BR>
### STEP 4: 
Encoding categorical data<BR>
### STEP 5: 
Normalizing the data<BR>
### STEP 6:
Splitting the data into test and train<BR>

##  PROGRAM:
### Import Libraries
```
from google.colab import files
import pandas as pd
import seaborn as sns
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from scipy import stats
import numpy as np

```
### Read the dataset
```
df=pd.read_csv("Churn_Modelling.csv")
df.head()
df.tail()
df.columns
```
### Check the missing data
```
df.isnull().sum()
df.duplicated()
```
### Assigning Y
```
y = df.iloc[:, -1].values
print(y)
```
### Check for duplicates
```
df.duplicated()
```
### Check for outliers
```
df.describe()
```
### Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)

```
### Checking datasets after dropping string values data from dataset
```
data.head()
```
### Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```
### Split the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```
### Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```

## OUTPUT:

### Data checking
![{22F3FEF0-DAD5-443F-9944-F6288A3E89AF}](https://github.com/user-attachments/assets/33b04adf-de66-47f7-bc4d-a5c5f0212fb7)
### Missing Data
![image](https://github.com/user-attachments/assets/364b7666-45db-42f4-90bf-463051fc9b68)
### Duplicates identification
![{B693C602-7082-4009-AFC0-3DC51B43C749}](https://github.com/user-attachments/assets/294edd2c-2aba-4c62-bebf-49398b700c4c)
### Values of 'Y'
![{0672104E-3265-4BBB-A5C5-3F7F93ACC246}](https://github.com/user-attachments/assets/366e23c2-4b42-48a2-b9af-4f043c6c6a80)
### Outliers
![{7A5348E5-38F2-455D-8677-5FD47B486184}](https://github.com/user-attachments/assets/6c48aca2-0845-4f04-a63e-7f75e4c30515)
### Checking datasets after dropping string values data from dataset
![{118824E0-A4FD-495A-A06E-960A166A8C00}](https://github.com/user-attachments/assets/f327157c-8a34-4104-8375-e1f7c52640e4)
### Normalize the dataset
![{72F66BE5-220C-4E33-AB4E-FD87A12CD44F}](https://github.com/user-attachments/assets/a3296541-7f0c-4ddb-9c2e-e96b98727ba0)
### Split the dataset
![{0F179DD0-6D89-4484-A652-EA098A623F35}](https://github.com/user-attachments/assets/cc6a6f1b-f8d3-4dfa-81c7-df44bba1e836)
### Training and testing model
![{E08C6A2C-CA78-4835-AF3B-79B5DC17A57C}](https://github.com/user-attachments/assets/ef436960-539d-48b8-8331-9a8b36e63a1c)

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


