---
layout: default
title: 'Data Preprocessing'
---

# Data Preprocessing

An essential part of the ML process.

## 1. Acquiring data
This seems obvious, but what is really important here is collecting the best data available for the job. Are the data:
* current?
* extensive?

## 2. Import necessary libraries
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

## 3. Importing datasets
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
