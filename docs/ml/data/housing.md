---
layout: default
title: 'Housing Dataset'
---

# The Housing Dataset

This dataset contains information about houses in the Boston area collected in 1978. It is small, containing only 506 observations, and contains 14 variables. The dataset can be found [here](https://archive.ics.uci.edu/ml/machine-learning-databases/housing/housing.data).

## Variables

Drawing from the [University of Toronto's Computer Science](http://www.cs.toronto.edu/~delve/data/boston/bostonDetail.html) department, the 14 variables are:

1. **CRIM** - per capita crime rate by town
2. **ZN** - proportion of residential land zoned for lots over 25,000 sq.ft.
3. **INDUS** - proportion of non-retail business acres per town.
4. **CHAS** - Charles River dummy variable (1 if tract bounds river; 0 otherwise)
5. **NOX** - nitric oxides concentration (parts per 10 million)
6. **RM** - average number of rooms per dwelling
7. **AGE** - proportion of owner-occupied units built prior to 1940
8. **DIS** - weighted distances to five Boston employment centres
9. **RAD** - index of accessibility to radial highways
10. **TAX** - full-value property-tax rate per $10,000
11. **PTRATIO** - pupil-teacher ratio by town
12. **B** - 1000(Bk - 0.63)^2 where Bk is the proportion of blacks by town
13. **LSTAT** - % lower status of the population
14. **MEDV** - Median value of owner-occupied homes in $1000's

The Toronto CS team notes that "**MEDV** seems to be censored at 50.00 (corresponding to a median price of $50,000); Censoring is suggested by the fact that the highest median price of exactly $50,000 is reported in 16 cases, while 15 cases have prices between $40,000 and $50,000, with prices rounded to the nearest hundred. Harrison and Rubinfeld do not mention any censoring."

## Loading the data

``` python
import pandas as pd
data_url = 'https://archive.ics.uci.edu/ml/machine-learning-databases/housing/housing.data'
# this url has no header info, so column names must be specified
colnames = ['CRIM', 'ZN', 'INDUS', 'CHAS', 'NOX', 'RM', 'AGE', 'DIS',
            'RAD', 'TAX', 'PTRATIO', 'B', 'LSTAT', 'MEDV']
# load dataset into pandas
df = pd.read_csv(data_url, header=None, sep='\s+', names=colnames)
```
