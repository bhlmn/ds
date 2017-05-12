---
layout: default
title: 'Data Preprocessing'
---

# Data Preprocessing

An essential part of the ML process.

## 1. Acquire data (MLA-Z)
This seems obvious, but what is really important here is collecting the best data available for the job. Are the data:
* current?
* extensive?

## 2. Import necessary libraries (MLA-Z)
Python:
```python
import numpy as np # powerful math/matrix functions
import matplotlib.pyplot as plt # data visualization
import pandas as pd # import and manage datasets
```
R:
```R
library(ggplot2) # data visualization
library(lubridate) # improved date/time handling
```

## 3. Import datasets (MLA-Z)
1. Ensure that the working directory/directory structure is in order!
2. Load data
3. Distinguish between independent variables (features) and dependent variable

Python:
```python
# load csv file using pandas
dataset = pd.read_csv('Data.csv')

# save feature matrix, in this case all columns save the last
X = dataset.iloc[:, :-1].values 

# save dependent variable vector ... NOTE! Python begins indexing at 0! So here we
# are grabbing the fourth column with index 3
y = dataset.iloc[:, 3].values
```

R:
```R
# set working directory, if needed
setwd('~/ml/data/')
```

## 4. Handle missing data (MLA-Z)
* We *could* delete observations with missing data *if* we have sufficient observations.
* Imputation, e.g. fill in missing data with average of a column

Python:
```python
# Take care of missing data
from sklearn.preprocessing import Imputer # scikit-learn imputation

# Use imputer class, note that strategy could be mean, median, or most_frequent
# axis = 0 will perform the strategy by columns, axis = 1 does so by rows.
imputer = Imputer(missing_values = 'NaN', strategy = 'mean', axis = 0)

# perform imputation on features (X) columns 2 and 3
imputer = imputer.fit(X[:, 1:3])
X[:, 1:3] = imputer.transform(X[:, 1:3])
```

R:
```R
# replace missing data with column means, specify each column
dataset$Age <- ifelse(is.na(dataset$Age), mean(dataset$Age, na.rm = TRUE), dataset$Age)
dataset$Salary <- ifelse(is.na(dataset$Salary), mean(dataset$Salary, na.rm = TRUE), dataset$Salary)

# --- or ... another way to do it --- #
dataset$Age[is.na(dataset$Age)] <- mean(dataset$Age, na.rm = TRUE)
dataset$Salary[is.na(dataset$Salary)] <- mean(dataset$Salary, na.rm = TRUE)
```

## 5. Encode categorical data (MLA-Z)
Python (Note that in python you have to turn a categorical variable with *n* categories into *n* dummy variables):
```python
# Encode categorical data
from sklearn.preprocessing import LabelEncoder, OneHotEncoder

# Create LabelEncoder object
labelencoder_X = LabelEncoder()

# Encode first column as categorical
X[:, 0] = labelencoder_X.fit_transform(X[:, 0])

# Create appropriate dummy variables for first column (0)
onehotencoder = OneHotEncoder(categorical_features = [0])
X = onehotencoder.fit_transform(X).toarray()

# Make dependent variable categorical
labelencoder_y = LabelEncoder()
y = labelencoder_y.fit_transform(y)
```

R (much simpler!):
```R
# make Country column a factor
dataset$Country <- factor(dataset$Country, 
                          levels = c('France', 'Spain', 'Germany'),
                          labels = c(1, 2, 3))
                          
# do the same for Purchased column
dataset$Purchased <- factor(dataset$Purchased, 
                            levels = c('No', 'Yes'),
                            labels = c(0, 1))
```

## 6. Splitting training and test datasets (MLA-Z)
Python:
```python
# Split dataset into training and test sets, note that random_state is the python equivalent to R's set.seed(), 
# and test_size = 0.2 turns 20% of the dataset into the test dataset
from sklearn.cross_validation import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2, random_state = 0)
```

R:
```R
# we will do with with caTools
# install.packages('caTools')
library(caTools)

# equivalent to random_state in python code above
set.seed(123)

# Split dataset into training and test sets, note here that SplitRatio is for size of the training set
split <- sample.split(dataset$Purchased, SplitRatio = 0.8)

# Create training and test sets
df.train <- dataset[split, ]
df.test <- dataset[!split, ]
```

## 7. Feature scaling (MLA-Z)
For many types of machine learning models, it is essential to scale (or normalize) features so they all have the same impact on the dependent variable.

Python:
```python
# Feature scaling
from sklearn.preprocessing import StandardScaler

# scale features of X
sc_X = StandardScaler()
X_train = sc_X.fit_transform(X_train)

# sc_X is already fitted, only need to transform X_test
X_test = sc_X.transform(X_test)
```

R:
```R
# Scale numeric columns of training and test set. Note that for small datasets we would want to scale df.test with
# the same mean and standard deviation as df.train, but for large datasets this shouldn't be an issue
df.train[2:3] <- scale(df.train[2:3])
df.test[2:3] <- scale(df.test[2:3])
```
