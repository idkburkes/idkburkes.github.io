
# Reading Notes 12 - Pandas #

Pandas is a Python library that makes manipulating data from .csv files very easy and beginner friendly. It has a lot of tools that makes it possible to take huge sets of data and derive useful insights with only a few functions. Pandas is commonly used alongside NumPy to make use of numpy arrays. In pandas, data is organized into what are know as "dataframes".I will outline some of the most useful pandas functions below.


## Imports ##
The convention for importing numpy and pandas looks like this
```python
import numpy as np 
import pandas as pd
```

## Dataframe Creation ##
I believe the most common for creating dataframes is to load data from a .csv
```python
filename = "/kaggle/input/80-cereals/cereal.csv"
df = pd.read_csv(filename) 
```

## Viewing Data ## 
```python
# views the top 5 entries of the dataframe
df.head()  

# views the bottom 3 entries of the dataframe
df.tail()  

# display the dataframe index
df.index  

# display the frame columns
df.columns 

# shows quick statistic summary such as count, mean, standard deviation, min, 1/2/3 quartiles and max
df.describe() 

```

## Selecting Data ##
```python
# Selections a single column "A"
df["A"] 

# You can also use slicing to select a range of indices
df[0:3]

# You can select column's values using boolean indexing to select data
df[df["A"] > 0]

```