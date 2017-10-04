---
layout: default
title: 'Pandas'
---

# Pandas Cheat Sheet

A collection of everything I have learned (and sometimes forget) about the Python data analysis library [pandas](http://pandas.pydata.org/).

## Table of Contents

* [Python basics](#basics)
* [Series](#series)
* [Sources](#sources)

## <a name='basics'></a>Python Basics

Importing libraries
``` python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline # plot within jupyter notebook
```

Defining functions
``` python
def function_name(parameter1, parameter2):
    # do something with the parameters
    return final_variable
```

Lists
``` python
list1 = [1, 2, 3, 4, 5]
list2 = ['a', 'b', 'c', 'd']
type(list1) # list
len(list1) # 5
```

Dictionaries
``` python
entrees = {
    'Filet Mignon' : 29.99,
    'Big Mac' : 3.99,
    'Pizza Slice' : 1.99,
    'Salmon' : 29.99
}
entrees['Big Mac'] # 3.99

# We can create dictionaries of dictionaries
desserts = {
    'Cake' : 3.49,
    'Ice Cream' : 1.79
}
menu = {
    'Entrees' : entrees,
    'Desserts' : desserts
}
menu['Entrees']['Big Mac'] # 3.99
```

## <a name='series'></a>Series

A one column dataframe can be 'squeezed' into a series.
``` python
series1 = pd.read_csv('filename1.csv', squeeze=True)
series2 = pd.read_csv('filename2.csv', usecols=['column1'], squeeze=True)
```

Several attributes of a pandas series:
``` python
series1.values # returns an array of the values
series1.index # returns the indices
series1.dtype # type of data in the series
series1.is_unique # returns False if there are duplicate entries
series1.shape # number of rows by columns (always 1) in the series
series1.name # name of the series ... which is mutable!
series1.name = 'Some new name'
```

Sorting series values and indices.
``` python
series1.sort_values() # sort in ascending order
series1.sort_values(ascending=False) # but can be in descending order!
```

By default `sort_values()` returns a copy of the series. To mutate the original:
``` python
series1.sort_values(inplace=True)
series1 = series1.sort_values()

# to return the series to the original, we can sort the index.
series1.sort_index(inplace=True)
```

Determine if a value is contained in a series.
``` python
value1 in series1 # probably False, because this is equivalent to:
value1 in series1.index

# instead, do
value1 in series1.values # True or False
```

## <a name='sources'></a>Sources

Much of what I have learned is a result of countless hours wrestling with pandas and finding help on [Stack Overflow](https://stackoverflow.com/questions/tagged/pandas). However, there exists a bevy of helpful media, including (note that this list is still growing!):

**Books**

* [Python Machine Learning](https://www.amazon.com/Python-Machine-Learning-scikit-learn-TensorFlow/dp/1787125939/ref=dp_ob_image_bk)

**Online Courses**

* [Data Analysis with Pandas and Python](https://www.udemy.com/data-analysis-with-pandas/learn/v4/overview)
* [Python for Data Science and Machine Learning](https://www.udemy.com/python-for-data-science-and-machine-learning-bootcamp/learn/v4/)
* [Machine Learning A-Z](https://www.udemy.com/machinelearning/learn/v4/)
* [Spark and Python for Big Data](https://www.udemy.com/spark-and-python-for-big-data-with-pyspark/learn/v4/)
