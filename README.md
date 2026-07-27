<H3>ENTER YOUR NAME: Mohamed Saudh R</H3>
<H3>ENTER YOUR REGISTER NO: 212225240085</H3>
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
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

data = pd.read_csv("Churn_Modelling.csv")
print(data)
X=data.iloc[:,:-1].values
print(x)
y=data.iloc[:,-1].values
print(y)
print(data.isnull().sum())

print(data.duplicated())

print(data.describe())

data = data.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()

scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)

X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)

print(X_train)
print(y_train)
print(X_test)
print(y_test)
```




## OUTPUT:
dataset:
<img width="1481" height="336" alt="image" src="https://github.com/user-attachments/assets/c28b4dce-6c4c-4334-a7b3-6894c6d1ff38" />
x_data:
<img width="1522" height="333" alt="image" src="https://github.com/user-attachments/assets/8e3f9c55-7d72-478f-b3a2-c52c29078a2d" />
y_data:
<img width="1487" height="50" alt="image" src="https://github.com/user-attachments/assets/964d697e-5726-4301-8844-efe3d3ad7d1f" />
Null values:
<img width="1505" height="366" alt="image" src="https://github.com/user-attachments/assets/e3a88283-f4bc-49d8-b62a-8d384181beba" />
Duplicated values:
<img width="1520" height="301" alt="image" src="https://github.com/user-attachments/assets/acf95d90-c041-4e48-8a35-1a4ee3f3f27f" />
Description:
<img width="1542" height="285" alt="image" src="https://github.com/user-attachments/assets/828493cd-a7fa-4cd4-9d6d-85d04115b665" />
Normalized data:
<img width="1487" height="337" alt="image" src="https://github.com/user-attachments/assets/167777e9-bdad-42c7-8f14-78bc82dbf931" />
trained_data:

<img width="471" height="192" alt="image" src="https://github.com/user-attachments/assets/9518c71b-2792-493c-b94d-6de73162df24" />

tested_values:

<img width="512" height="191" alt="image" src="https://github.com/user-attachments/assets/6b9454ed-c94d-4f19-a9a1-4e165e599b3e" />




## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


