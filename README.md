## 📘 Project Overview
##### This project aims to predict whether a person has diabetes based on certain diagnostic health measurements.
##### The dataset used is the Pima Indians Diabetes Database, a well-known dataset in machine learning.
##### The objective is to build and evaluate a Logistic Regression model to classify whether a person is diabetic (1) or not (0).

## 📊 Dataset Information
##### Source: Kaggle - Diabetes Database

##                               
##### Pregnancies	:                         Number of times pregnant	:                                  Integer
##### Glucose	Plasma :                     glucose concentration after 2 hours   :                      Integer
##### BloodPressure	 :                    Diastolic blood pressure (mm Hg)	:                           Integer
##### SkinThickness	 :                    Triceps skin fold thickness (mm)	:                           Integer
##### Insulin	:                           2-Hour serum insulin (mu U/ml)	  :                            Integer
##### BMI	    :                           Body Mass Index (weight in kg/(height in m)^2):               Float
##### Diabetes :                          A function that scores the likelihood  :                       Float
##### PedigreeFunction :                  of diabetes based on family history
##### Age	  :                             Age in years	:                                                Integer
##### Outcome	:                           Class variable (0 = Non-diabetic, 1 = Diabetic)	 :             Integer

## Data Preprocessing Steps

####   Load dataset:df = pd.read_csv('diabetes.csv')

####   Check shape, duplicates, and missing values:
#####  Rows: 768
#####  Columns: 9
#####  Duplicates: 0

###   Statistical Summary:
##### Used df.describe() to understand data distribution, mean, and standard deviation.

###   Identify zero values:
##### Certain columns like Glucose, BloodPressure, SkinThickness, Insulin, and BMI contain zero values that may represent missing data.

#### Feature and Target Split:X = df.drop('Outcome', axis=1)
####                          y = df['Outcome']

###    Train-Test Split:
####   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
