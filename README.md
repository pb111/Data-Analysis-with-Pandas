# Data Analysis with Pandas


Pandas is an open source library for data analysis in Python. In this project, I explore pandas and important data analysis tools of pandas. 


## Table of contents


The contents of this project are divided into various categories which are listed below:-


1.	Introduction to Pandas

2.	Key features of Pandas

3.	Advantages of Pandas

4.	Importing Pandas

5.	Data structures in Pandas

6.	Pandas series

7.	Pandas dataframe

8.	Pandas panel

9.	Data import with pandas

10.	Dataset description

11.	Exploratory data analysis

12.	Handle missing values with pandas

13.	Indexing and slicing in pandas        
        
14.	Indexing and reindexing in pandas
             
15.	MultiIndex or Advanced indexing
             
16.	Sorting in pandas
              
17.	Categorical data in pandas
            
18.	Basic functionality in pandas

19.	Descriptive statistics in pandas

20.	Statistical functions in pandas

21.	Window functions in pandas

22.	Aggregations in pandas

23.	Iteration in pandas

24.	Function application in pandas

25.	Pandas GroupBy operations

26.	Pandas merging and joining
 
27.	Pandas concatenation operation

28.	Reshaping by melt and pivot

29.	Reshaping by stacking and unstacking

30.	Options and customization with pandas

31.     References


================================================================================


## 1. Introduction to Pandas


Today, Python is considered as the most popular programming language for doing data science work.  The reason behind this popularity is that Python provides great packages for doing data analysis and visualization work. 

**Pandas** is one of those packages that makes analysing data much easier. Pandas is an open source library for data analysis in Python. It was developed by Wes McKinney in 2008. Over the years, it has become the standard library for data analysis using Python.

According to the Wikipedia page on Pandas, 

“Pandas offers data structures and operations for manipulating numerical tables and time series. It is free software released under the three-clause BSD license. The name is derived from the term "panel data", an econometrics term for data sets that include observations over multiple time periods for the same individuals.”

In this project, I explore Pandas and various data analysis tools provided by Pandas.


================================================================================


## 2. Key features of Pandas

Some key features of Pandas are as follows:-

1.	It provides tools for reading and writing data from a wide variety of sources such as CSV files, excel files, databases such as SQL, JSON files.
2.	It provides different data structures like series, dataframe and panel for data manipulation and indexing.
3.	It can handle wide variety of data sets in different formats – time series, heterogeneous data, tabular and matrix data.
4.	It can perform variety of operations on datasets. It includes subsetting, slicing, filtering, merging, joining, groupby, reordering and reshaping operations.
5.	It can deal with missing data by either deleting them or filling them with zeros or a suitable test statistic.
6.	It can be used for parsing and conversion of data.
7.	It provides data filtration techniques.
8.	It provides time series functionality – date range generation, frequency conversion, moving window statistics, data shifting and lagging.
9.	It integrates well with other Python libraries such as Scikit-learn, statsmodels and SciPy.
10.	It delivers fast performance. Also, it can be speeded up even more by making use of Cython (C extensions to Python).


================================================================================


## 3. Advantages of Pandas
Pandas is a core component of the Python data analysis toolkit. Pandas provides data structure and operations facilities, which is particularly useful for data analysis. There are various advantages of using Pandas for data analysis. These advantages are as follows:-
1.	**Data representation** - It represents data in a form that is very much suited for data analysis through its Dataframe and Series data structures.
2.	**Data subsetting and filtering** - It provides for easy subsetting and filtering of data. It provides procedures that are suited for data analysis.
3.	**Concise and clear code** - It provides functionality to write clear and concise code. It allows us to focus on the task at hand, rather than have to write tedious code.


================================================================================


## 4. Importing Pandas
In order to use Pandas in our work, we need to import the Pandas library first. We can import the Pandas library with the following command:-
`import pandas`
Usually, we import the Pandas library by appending the alias `as pd`.  It makes things easier because now instead of writing `pandas.command` we need to write `pd.command`. So, we 
will import pandas with the following command:-
`import pandas as pd`
Also, I will import Numpy as well, because it is very useful library for scientific computing with Python. I will import Numpy with the following command:-
`import numpy as np`


================================================================================


## 5. Data structures in Pandas
Pandas provide easy to use data structures. 
There are three main data structures in Pandas. They are:-
-	Series
-	Dataframe
-	Panel
These data structures are built on top of Numpy array, which means they are fast.
I have described these data structures in the following sections.


================================================================================


## 6. Pandas Series
A Pandas Series is a one-dimensional array like structure with homogeneous data.  


The data can be of any type (integer, string, float, etc.). The axis labels are collectively called index. 
For example, the following series is a collection of integers 10, 20, 30, 40, 50, 60, 70, 80, 90, 100.

### Key Points of Pandas Series
-	Homogeneous data
-	Size of series immutable
-	Values of data mutable


### Series Constructor
A Pandas Series can be created using the following constructor −
`pandas. Series (data, index, dtype, copy)`

The parameters of the constructor are as follows –

-	**data** - data takes various forms like ndarray, list, dictionary, constants, etc.


-	**index**- index values must be unique, hashable and have the same length as data.   
                  The default index is RangeIndex (0, 1, 2, …, n) if no index is passed.
      
-	**dtype** - dtype is for data type. If none, data type will be inferred.

-	**copy** - Copy input data. Default value is False.


================================================================================


## 7. Pandas DataFrame

A Dataframe is a two-dimensional data structure. So, data is aligned in a tabular fashion in rows and columns. 
Its column types can be heterogeneous:  - that is, of varying types. It is similar to structured arrays in NumPy with mutability added.

### Properties of Dataframe are as follows:-
-	The dataframe is conceptually analogous to a table or spreadsheet of data. 
-	Its columns are of different types – float64, int, bool, and so on.
-	A Dataframe column is a Series structure.
-	Its size is mutable – columns can be inserted and deleted.
-	It has labelled axes (rows and columns).
-	It can be thought of as a dictionary of Series structures where both the rows and   
             columns are indexed, denoted as `index` in the case of rows and `columns` in the 
             case of columns.     
-	It can perform arithmetic operations on rows and columns.

### Dataframe Constructor

Dataframe is the most commonly used data structure in pandas. 

A pandas Dataframe can be created using the following constructor-
`pandas.DataFrame(data, index, columns, dtype, copy)`

The constructor accepts many different types of arguments: 
-	Dictionary of 1D ndarrays, lists, dictionaries, or Series structures 
-	2D NumPy array
-	Structured or record ndarray    
-	Series structures    
-	Another Dataframe structure 

The parameters description of the constructor is as follows –
-**data** - data takes various forms like ndarray, series, map, lists, dict, constants and also another DataFrame.
-**index**- Index or array-like 
         Index to use for resulting frame. Will default to RangeIndex if no indexing information   
         part of  input data and no index provided.     
-**columns**- Index or array-like


              Column labels to use for resulting frame. Will default to RangeIndex (0, 1, 2, …, n) if no column labels are  provided.         
            
-**dtype** - data type of each column

-**copy** - boolean, default False
            Copy data from inputs. Only affects DataFrame / 2d ndarray input

### Dataframe Creation
A pandas Dataframe can be created using various inputs like –
-	Lists
-	Dict
-	Series
-	Numpy ndarrays
-	Another Dataframe


================================================================================


## 8. Pandas Panel
A panel is a 3D container of data. 

The term Panel data is derived from **econometrics** and is partially responsible for the name pandas − pan(el)-da(ta)-s.

The names for the 3 axes are intended to give some semantic meaning to describing operations involving panel data. 

They are −
`items − axis 0`, each item corresponds to a DataFrame contained inside.
`major_axis − axis 1`, it is the index (rows) of each of the DataFrames.
`minor_axis − axis 2`, it is the columns of each of the DataFrames.


================================================================================



## 9. Data Import with Pandas
Pandas input output API provides several functions that can be used to import and export various file formats. 

Below is the list of file formats and the corresponding functions to import these file formats.

- Flat files - read_csv()
- Excel files - read_excel(), ExcelWriter()
- JSON files - read_json()
- HTML tables - read_html()
- SAS files - read_sas()
- SQL files - read_sql(), read_sql_query(), read_sql_table()
- STATA files - read_stata()
- pickle object - read_pickle()
- HDF5 files - read_hdf()

In this project, I work with the **BlackFriday dataset** which is a comma-separated values (CSV) file type. In a CSV file type, the data is stored as a comma-separated values where each row is separated by a new line, and each column by a comma (,).
So, I use the **read_csv()** function to import the file as follows:-
`data = 'C:/datasets/BlackFriday.csv'`
`df = pd.read_csv(data)`



================================================================================


## 10. Dataset description
I have used **BlackFriday** dataset for this project. The dataset is the sample of the transactions made in a retail store.
The dataset contains 12 variables and 537577 instances.
I have downloaded this dataset from the following url:-
https://www.kaggle.com/mehdidag/black-friday


================================================================================


## 11. Exploratory Data Analysis

The next step is to conduct exploratory data analysis.

### check the type of df
I have imported the dataset. The next step is to check its type. We can check its type with the following command:-
`type(df)`
We can see that the `df` is the pandas dataframe.

### check shape of dataframe
The next step is to check the shape of the dataframe. We can check the shape of the dataframe as follows:-
`df.shape`
### view the first five rows of the dataframe
We can view the first 5 rows of the dataframe with **head()** function as follows:-
`df.head()`

### view concise summary of dataframe
We can view the concise summary of dataframe with **info()** method as follows:-
`df.info()`


================================================================================


## 12. Handle missing values with pandas
We can check the total number of missing values in each column in the dataset with the following command:-
`df.isnull().sum()`





### isna() and notna() functions to detect 'NA' values
Pandas provides `isna()` and `notna()` functions to detect 'NA' values. 
These are also methods on Series and Dataframe objects.
Examples of isna() and notna() commands.

detect ‘NA’ values in the dataframe	
`df.isna().sum()`

detect ‘NA’ values in a particular column in the dataframe
`pd.isna(df[‘col_name’])`
`df[‘col_name’].notna()`
All the missing values are encoded as `NA` values. If the missing values are encoded in different ways we should encode them first.

### Encode missing numerical values
Missing values are encoded in different ways. They can appear as `NaN`, `NA`, `?`, `zeros`, `xx`, `-1` or a blank space `“ ”`. 
We can use various pandas methods to deal with missing values. 
But, pandas always recognize missing values as `NaN`.  So, it is essential that we should first convert all the `?`, `zeros`, `xx`, `-1` or `“ ”` to `NaN`. If the missing values isn’t identified as `NaN`, then we have to first convert or replace 
such `non NaN` entry with a `NaN`.

### Convert '?' to ‘NaN’
`df[df == '?'] = np.nan`




### Handle missing numerical values
There are several methods to handle missing values. Each method has its own advantages and disadvantages. The choice of the method is subjective and depends on the nature of data and the missing values. In this section, I have listed the most commonly used methods to deal with missing values. They are as follows:-

- Drop missing values with dropna() method
- Fill missing values with zeros
- Fill missing values with a test statistic
- Fill missing values backward or forward

In this section, I have fill the missing values with forward or backward filling.

The **pad or fill** option fill values forward, while **bfill or backfill** option fill values backward. 
The following code helps us to achieve this task:-
`df = df.fillna(method = 'pad')`
Still, the `Product_Category_2` and `Product_Category_3` have 1 missing value.
The first element of each column are NaN. So, in this case **pad** or **fill** option does not work. Here, we should use **bfill** or **backfill** options as follows:-
`df = df.fillna(method = 'backfill')`

### Check with ASSERT statement
Finally, we should check for missing values programmatically. If we drop or fill missing values, we expect no missing values. 
We can write an assert statement to verify this. So, we can use an assert statement to programmatically check that no missing or unexpected '0' value is present. This gives confidence that our code is running properly.
Assert statement will return nothing if the value being tested is true and will throw an AssertionError if the value is false.

Asserts
•	assert 1 == 1   (return Nothing if the value is True)
•	assert 1 == 2   (return AssertionError if the value is False)

`assert pd.notnull(df).all().all()`

The above command does not throw any AssertionError. So, it is confirmed that there are no missing values in the dataframe.


================================================================================


## 13.	Indexing and slicing in pandas
In this section, I will discuss how to slice and dice the data and get the subset of pandas dataframe.
Pandas provides three types of Multi-axes indexing. Those three types are mentioned in the following table:-
- 1. .loc() - Label based
- 2. .iloc() - Integer based
- 3. .ix()  - Both Label and Integer based
Starting with pandas 0.20.0, the .ix indexer is deprecated, in favor of the more strict .iloc and .loc indexers. So, I will not discuss it here and limit the discussion to .loc and .iloc indexers.

### Label based indexing using .loc indexer


Pandas provide **.loc indexer** to have purely label based indexing. When slicing, the start bound is also included. 
Integers are valid labels, but they refer to the label and not the position.

.loc() indexer has multiple access methods like −

- A single scalar label

- A list of labels

- A slice object

- A Boolean array


**Syntax**-

.loc() takes two single/list/range operator separated by ','. 

The first one indicates the row and the second one indicates columns.

Below are the examples of selecting data using .loc() indexer:-


make a copy of dataframe
`df1 = df.copy()`

 select first row of dataframe
`df1.loc[0]`


select first five rows for a specific column
`df1.loc[:,'Purchase'].head()`


Select all rows for multiple columns, say list[]

`df1.loc[:,['Age','Occupation']]`



Select first five rows for multiple columns, say list[]

`df1.loc[[0, 1, 2, 3, 4],['Age','Occupation']]`


Select range of rows for all columns
`df1.loc[0:4]`


The above functionality can also be given by
`df1.head()`



### Integer position based indexing using .iloc() indexer

Pandas provides **.iloc indexer** for integer position based indexing.

.iloc is primarily integer position based (from 0 to length-1 of the axis), but may also be used with a boolean array. 

.iloc will raise IndexError if a requested indexer is out-of-bounds, except slice indexers which allow out-of-bounds indexing.  Allowed inputs of .iloc indexer are:-




- An integer e.g. 5.

- A list or array of integers [4, 3, 0].

- A slice object with ints 1:7.

- A boolean array.


### Rows selection using .iloc indexer

Below are the examples of row selection using .iloc indexer

#### select first row of dataframe
`df1.iloc[0]`


#### select second row of dataframe
`df1.iloc[1]`


#### select last row of dataframe
`df1.iloc[-1]`


#### select second last row of dataframe
`df1.iloc[-2]`


### Columns selection using .iloc indexer


#### select first column of dataframe
`df1.iloc[:,0]`


#### select second column of dataframe
`df1.iloc[:,1]`



#### select last column of dataframe
`df1.iloc[:,-1]`



#### select second last column of dataframe
`df1.iloc[:,-2]`


### Multiple row and column selections using .iloc indexer



#### select first five rows of dataframe
`df1.iloc[0:5]`



#### select first five columns of data frame with all rows
`df1.loc[:, 0:5]`


#### select 1st, 5th and 10th rows with 1st, 4th and 7th columns
`df1.iloc[[0,4,9]], [0,3,6]]`


#### select first 5 rows and 5th, 6th, 7th columns of data frame
`df1.iloc[0:5, 5:8]`



### Indexing first occurrence of maximum or minimum values

Pandas provide two functions **idxmax()** and **idxmin()** that return index of first occurrence of maximum or minimum values over requested axis. NA/null values are excluded from the output.

get index of first occurence of maximum Purchase value 

`df1['Purchase'].idxmax()`


get the row with the maximum Purchase value 

`df1.loc[df1['Purchase'].idxmax()]`

### Indexing a single value with at() and iat()

Pandas provides **at()** and **iat()** functions to access a single value for a row and column pair by label or by integer position.

get value at 1st row and Purchase column pair

`df1.at[1, 'Purchase']`

get value at 1st row and 11th column pair

`df1.iat[1, 11]`


### Boolean indexing in pandas

**Boolean indexing** is the use of boolean vectors to filter and select the data. The operators for boolean indexing are -

- 1. | for or, 

- 2. & for and,

- 3. ~ for not. 


These must be grouped by using parentheses. Using a boolean vector to index a Series works exactly as in a NumPy ndarray.


Conditional selections with boolean arrays using **df.loc[selection]** is the most common method to use with Pandas DataFrames. With boolean indexing or logical selection, we can pass an array or Series of True/False values to the .loc indexer to select the rows where the Series has True values. Then, we will make selections based on the values of different columns in dataset.


We can use a boolean True/False series to select rows in a pandas dataframe where there are true values. Then, a second argument can be passed to .loc indexer to select other columns of the dataframe with the same label. The columns are referred to by name for the loc indexer and can be a single string, a list of columns, or a slice ":" operation.


make a copy of dataframe df

`df2 = df.copy()`

get the purchase amount with a given user_id and product_id

`df2.loc[((df2['User_ID'] == 1000001) & (df2['Product_ID'] == 'P00069042')), 'Purchase']`


### Indexing with isin() method

The **isin()** method of Series, returns a boolean vector. It is true wherever the Series elements exist in passed list. This allows you to select rows where one or more columns have values we want to access. The same method is available for Index objects. It is useful for the cases when we don't know which of the sought labels are in fact present.

DataFrame also has an **isin()** method. When calling isin, we pass a set of values as either an array or dict. If values is an array, isin returns a DataFrame of booleans that is the same shape as the original DataFrame, with True wherever the element is in the sequence of values.
`values=[1000001,'P00069042','F',0-17,10,'A',2,0,3,6,14,8370]`

`df2_indexed=df2.isin(values)`

`df2_indexed.head(10)`


We can combine DataFrame's isin with the **any()** and **all()** methods to quickly select subsets of the data that meet a given criteria. We can select a row where each column meets its own criterion as follows:-

`row_mask = df2.isin(values).any(1)`

`df[row_mask]`


### The where() method and masking

We can select values from a Series with a boolean vector and it returns a subset of the data. To guarantee that the output has the same shape as the original data, we can use the where method in Series and DataFrame.

We can select values from a DataFrame with a boolean criterion. It also preserves input data shape.

The below code is equivalent to 

`df2[df2==0]`

It replaces values with `NaN` where the condition is false.


### Indexing with query() method

There is a **query()** method in the DataFrame objects that allows selection using an expression. This method queries the columns of a DataFrame with a boolean expression.

`df2.query('(Product_Category_1 > Product_Category_2) & (Product_Category_2 > Product_Category_3)')`


================================================================================


## 14. Indexing and reindexing in pandas

Reindexing changes the row labels and column labels of a DataFrame. To reindex means to conform the data to match a given set of labels along a particular axis.

Multiple operations can be accomplished through indexing like:−

- Reorder the existing data to match a new set of labels.

- Insert missing value (NA) markers in label locations where no data for the label existed.


### Create a new dataframe

First of all, I will create a new dataframe as follows:-

let's create a new dataframe 

`food = pd.DataFrame({'Place':['Home', 'Hotel', 'Home', 'Hotel'],
                   'Time': ['Lunch', 'Dinner', 'Lunch', 'Dinner'],
                   'Food':['Soup', 'Rice', 'Soup', 'Chapati'],
                   'Price($)':[10, 20, 30, 40]})`


### Set an index 

DataFrame has a **set_index()** method which takes a column name (for a regular Index) or a list of column names (for a MultiIndex). This method sets the dataframe index using existing columns.

I will create a new, re-indexed DataFrame with **set_index()** method as follows:-

`food_indexed1=food.set_index('Place')`

`food_indexed1`

`food_indexed2=food.set_index(['Place', 'Time'])`

`food_indexed2`

### Reset the index


There is a function called **reset_index()** which transfers the index values into the DataFrame’s columns and sets a simple integer index. This is the inverse operation of set_index().

`food_indexed2.reset_index()`


================================================================================


## 15. MultiIndex or Advanced indexing

In this section, I will explore indexing with a MultiIndex and other advanced indexing strategies.

### Hierarchical indexing or MultiIndex

The MultiIndex object is the hierarchical analogue of the standard index object which stores the axis labels in pandas objects. A MultiIndex is an array of tuples where each tuple is unique. 

A MultiIndex can be created from a list of arrays (using **MultiIndex.from_arrays()**), an array of tuples (using **MultiIndex.from_tuples()**), a crossed set of iterables (using **MultiIndex.from_product()**), or a DataFrame (using **MultiIndex.from_frame()**). The Index constructor will attempt to return a MultiIndex when it is passed a list of tuples.


To demonstrate the concept of hierarchical or multiple indexing, first I will create a hypothetical dataframe as follows:-

`sales=pd.DataFrame([['books','online', 200, 50],['books','retail', 250, 75], 
                    ['toys','online', 100, 20],['toys','retail', 140, 30],
                    ['watches','online', 500, 100],['watches','retail', 600, 150],
                    ['computers','online', 1000, 200],['computers','retail', 1200, 300],
                    ['laptops','online', 1100, 400],['laptops','retail', 1400, 500],
                    ['smartphones','online', 600, 200],['smartphones','retail', 800, 250]],
                    columns=['Items', 'Mode', 'Price', 'Profit'])`



### Create the hierarchical index in pandas

We can create a hierarchical index in pandas using the **set_index()** function which is used for indexing. First the data is indexed on `Items` and then on `Mode` column as follows:-

`sales1=sales.set_index(['Items', 'Mode'])`



### View index in hierarchical index

One can view the details of index as shown below:-

`sales1.index`
### Swap the column in hierarchical index

Now, I will swap the "Items" and "Mode" columns in the above hierarchical dataframe as shown below:-

`sales2=sales1.swaplevel('Mode', 'Items')`


================================================================================


## 16. Sorting in pandas

Pandas provides two kinds of sorting. They are:-


- 1. Sorting by label

- 2. Sorting by actual value


They are described below:-


### 1. Sorting by label

We can use the **sort_index()** method to sort the object by labels. DataFrame can be sorted by passing the axis arguments and the order of sorting. By default, sorting is done on row labels in ascending order.

The following examples illustrate the idea of sorting by label.

sort the dataframe df2 by label
`df2.sort_index()`


### Order of sorting

By passing the Boolean value to ascending parameter, the order of the sorting can be controlled. 

sort the dataframe df2 by label in reverse order
`df2.sort_index(ascending=False)`



### Sorting by columns

By passing the axis argument with a value 0 or 1, the sorting can be done on the row or column labels. 

The default value of axis=0. In this case, sorting can be done by rows. 

If we set axis=1, sorting is done by columns.


sort the dataframe df2 by columns

`df2.sort_index(axis=1)`


### 2. Sorting by values

The second method of sorting is sorting by values. Pandas provides **sort_values()** method to sort by values. It accepts a 'by' argument which will use the column name of the DataFrame with which the values are to be sorted.

The following example illustrates the idea:-


`df2.sort_values(by=['Product_Category_1'])`




#### Sort by multiple columns

`df2.sort_values(by=['Product_Category_1', 'Product_Category_2'])`


#### Sort in descending order

`df2.sort_values(by='Product_Category_1', ascending=False)`


================================================================================


## 17. Categorical data in pandas


We can check the data types of variables in the dataset with the following command:-

`df3 = df.copy()`

`df3.dtypes`

Our dataset has 5 categorical variables. They are **Product_ID**, **Gender**, **Age**, **City_Category** and **Stay_In_Current_City_Years**. They have data types as **object**.






### Description of categorical data

The **describe()** method on categorical data will produce similar output to a Series or DataFrame of type string.

`df3['Gender'].describe()`


### Working with categorical data

Categorical data has a categories and a ordered property, which list their possible values and whether the ordering matters or not. These properties are exposed as `s.cat.categories` and `s.cat.ordered`. 

If we don't manually specify categories and ordering, they are inferred from the passed arguments.

`s.cat.categories`

`s.cat.ordered`

where `s` is a series object.


### Unique values in categorical data

We can get the unique values in a series object by **unique()** method. It returns categories in the order of appearance, and it only includes values that are actually present.

`df3['Gender'].unique()`
### Rename categories

Renaming categories is done by assigning new values to the `Series.cat.categories` property or by using the `rename_categories()` method.


### Append new categories

Appending categories can be done by using the `add_categories()` method.


### Remove categories

Removing categories can be done by using the `remove_categories()` method. Values which are removed are replaced by np.nan.


### Setting categories

If we want to remove and add new categories in one step (which has some speed advantage), or simply set the categories to a predefined scale, we can use `set_categories()` method.


### Reordering categories

Reordering the categories is possible via the `Categorical.reorder_categories()` and the `Categorical.set_categories()` methods. 



### Operations on categorical data 

There are several operations like `Series.min()`, `Series.max()`, `Series.median()` and `Series.mode()` which are possible with categorical data. 



### Frequency counts of categorical data

Series methods like `Series.value_counts()` will return the frequency counts of the categories present in the series.

`df3['Gender'].value_counts()`


`Series.value_counts()` will return the frequency counts of the categories in descending order. To get the categories in ascending order we should set `ascending=True` as follows:-

`df3['Gender'].value_counts(ascending=True)`


================================================================================


## 18. Basic functionality in pandas


### Series basic functionality



The following table lists the important attributes or methods in Series basic functionality.



- **axes** - Returns a list of the row axis labels


- **dtype** - Returns the dtype of the object.


- **empty** - Returns True if series is empty.


- **ndim** - Returns the number of dimensions of the underlying data, by definition 1.


- **size** - Returns the number of elements in the underlying data.


- **values** - Returns the Series as ndarray.


- **head()** - Returns the first n rows.


- **tail()** - Returns the last n rows.




### Dataframe basic functionality



The following tables lists the important attributes or methods in Dataframe basic functionality.



- **T** - Transposes rows and columns.


- **axes** - Returns a list with the row axis labels and column axis labels as the only members.


- **dtypes** - Returns the dtypes in this object.


- **empty** -  True if NDFrame is entirely empty [no items]; if any of the axes are of length 0.


- **ndim** -  Number of axes / array dimensions.


- **shape** -  Returns a tuple representing the dimensionality of the Dataframe.


- **size** - Number of elements in the NDFrame.


- **values** - Numpy representation of NDFrame.


- **head()** - Returns the first n rows.


- **tail()** - Returns last n rows.


================================================================================


## 19. Descriptive statistics in pandas



There exists a large number of methods for computing descriptive statistics and other related operations on Series, DataFrame, and Panel. Most of these are aggregations (hence producing a lower-dimensional result) like sum(), mean(), and quantile(), but some of them, like cumsum() and cumprod(), produce an object of the same size. Generally speaking, these methods take an axis argument, just like ndarray.{sum, std, …}, but the axis can be specified by name or integer.


- Series: no axis argument needed.


- DataFrame: “index” (axis=0, default), “columns” (axis=1).


- Panel: “items” (axis=0), “major” (axis=1, default), “minor” (axis=2).



### Functions and description


The following table list down the important functions under Descriptive Statistics in Python Pandas. 

- 1     **count()** -	Number of non-null observations

- 2	  **sum()** -	Sum of values


- 3	  **mean()**  -	Mean of values


- 4	 **median()** -	Median of values


- 5	 **mode()**  -	Mode of values


- 6	 **std()**   -	Standard deviation of the values


- 7	 **min()**   -	Minimum value


- 8	 **max()**   -	Maximum value


- 9	 **abs()**   -	Absolute value


- 10 **prod()**  -	Product of values


- 11 **cumsum()** -	Cumulative sum


- 12 **cumprod()** - Cumulative product



The dataframe is a heterogeneous data structure. So, the different column values have different data types. Generic operations don't work with all functions.


Functions like **sum()**, **cumsum()** work with both numeric and character (or) string data elements without any error. 
In practice, character aggregations are never used generally. These functions do not throw any exception.


Functions like **abs()**, **cumprod()** throw exception when the dataframe contains character or string data because such operations cannot be performed.


### Summarizing data

The **describe()** function computes the summary statistics of the numerical columns in the dataframe.

This function gives the mean, std and IQR values. It excludes the character columns and gives summary about numeric columns. 
It includes the argument which is used to pass necessary information regarding what columns need to be considered for summarizing. It takes the list of values; by default, 'number'.

- object − Summarizes string columns

- number − Summarizes numeric columns

- all − Summarizes all columns together

`df4=df.describe()`

`df4.describe()`


================================================================================


## 20. Statistical functions in pandas

Statistical functions help us to understand and analyze the behavior of data. In this section, I will discuss few statistical functions, which we can apply on Pandas objects.

### Percent_change

Series, datFrames and panel, all have the function **pct_change()**. This function compares every element with its prior element and computes the change percentage.

By default, the pct_change() operates on columns; if you want to apply the same row wise, then use axis=1() argument.


### Covariance

Covariance is applied on series data. The series object has a method **cov()** to compute covariance between series objects. NA values will be excluded automatically.

**Series.cov()** can be used to compute covariance between series (excluding missing values).

Analogously, **dataFrame.cov()** to compute pairwise covariances among the series in the dataFrame, also excluding NA/null values.

`df5=df.copy()`

`df5.cov()`



### Correlation

**Correlation** shows the linear relationship between any two array of values (series). There are multiple methods to compute the correlation. These methods are listed below:-

**Method name**  	  **Description**

- pearson (default)	-  Standard correlation coefficient

- kendall           	-  Kendall Tau correlation coefficient

- spearman	        -  Spearman rank correlation coefficient

All of these are currently computed using pairwise complete observations.

Any non-numeric columns will be automatically excluded from the correlation calculation.


### Data Ranking


Data Ranking produces ranking for each element in the array of elements. In case of ties, assigns the mean rank. 


The **rank()** method produces a data ranking with ties being assigned the mean of the ranks (by default) for the group.


The **rank()** is also a dataframe method and can rank either the rows (axis=0) or the columns (axis=1). NaN values are excluded from the ranking.

It optionally takes a parameter ascending which true by default. If it is set to false, data is ranked in descending order, with larger values assigned a smaller rank.

The **rank()** supports different tie-breaking methods, specified with the method parameter as follows:-

- **average** - average rank of tied group

- **min** - lowest rank in the group

- **max** - highest rank in the group

- **first** - ranks assigned in the order they appear in the array



### Common statistical functions

There are a number of common statistical functions. These are listed below:-

**Method**    - **Description**

- **count()** - Number of non-null observations

- **sum()** -   Sum of values


- **mean()** -  Mean of values

- **median()** - Arithmetic median of values

- **min()** -	Minimum

- **max()** - 	Maximum

- **std()** -	Standard deviation

- **var()** -	Variance

- **skew()** -	Skewness

- **kurt()** -	Kurtosis

- **quantile()** -	Quantile

- **apply()** -	Generic apply

- **cov()** -	Covariance

- **corr()** -	Correlation

The **apply()** function takes an extra **func** argument and performs generic rolling computations. The **func** argument should be a single function that produces a single value from an ndarray input.


================================================================================


## 21. Window functions in pandas

For working with numerical data, Pandas provide few variants like **rolling**, **expanding** and **exponentially moving weights** for window statistics. 

Among these are **count**, **sum**, **mean**, **median**, **correlation**, **variance**, **covariance**, **standard deviation**, **skewness** and **kurtosis**.

The **rolling()** and **expanding()** functions can be used directly from DataFrameGroupBy objects.

In this section, we work with rolling, expanding and exponentially weighted data through the corresponding objects, **Rolling**, **Expanding** and **EWM**.



### .rolling() Function

This function can be applied on a series of data. Specify the **window=n** argument and apply the appropriate statistical function on top of it.

`df6=df.copy()`

`df6.rolling(window=3).mean()`


Since the window size is 3, for first two elements there are nulls and from third the value will be the average of the n, n-1 and n-2 elements. We can also apply various functions.



### .expanding() Function

This function can be applied on a series of data. We specify the **min_periods=n** argument and apply the appropriate statistical function on top of it.

`df6.expanding(min_periods=3).mean()`


### .ewm() Function

**ewm** is applied on a series of data. We have to specify any of the com, span, halflife argument and apply the appropriate statistical function on top of it. It assigns the weights exponentially.

`df6.ewm(com=0.5).mean()`


Window functions are used in finding the trends within the data graphically by smoothing the curve. If there is a lot of variation in the data, then we can apply window functions to smooth out the curve or the trend.


================================================================================


## 22. Aggregations in pandas

Once the rolling, expanding and ewm objects are created, several methods are available to perform aggregations on data.


### Apply aggregation on a whole dataframe


`df6=df.copy`


`df6.aggregate(np.sum)`


### Apply aggregation on a single column of a dataframe

`df6=df.copy()`

`df6['Purchase'].aggregate(np.sum)`


### Apply multiple functions on a single column of a dataframe

`df6['Purchase'].aggregate([np.sum, np.mean])`


### Apply aggregation on multiple columns of a dataframe

`df6[['Product_Category_1', 'Product_Category_2', Product_Category_3']].aggregate(np.mean)`

### Apply multiple functions on multiple columns of a dataframe

`df6[['Product_Category_1', 'Product_Category_2', 'Product_Category_3']].aggregate([np.sum, np.mean])`

### Apply different functions to different columns of a dataframe

df6.aggregate({'Product_Category_1' : np.sum ,'Product_Category_2' : np.mean})


================================================================================


## 23. Iteration in pandas

The behaviour of basic iteration over pandas objects depends on the type. When iterating over a series, it is regarded as array-like, and basic iteration produces the values. Other data structures, like dataframe and panel, follow the **dict-like** convention of iterating over the **keys** of the objects.
Iterating a dataframe gives column names.

To iterate over the rows of the DataFrame, we can use the following functions −

- **iteritems()** − to iterate over the (key,value) pairs

- **iterrows()** − iterate over the rows as (index,series) pairs

- **itertuples()** − iterate over the rows as namedtuples


================================================================================


## 24. Function application in pandas

There are three important methods that enable us to apply our own or another library's functions to pandas objects. These methods differentiate on their scope of usage. These functions expect to operate on an entire dataframe, row- or column-wise operation, or element wise operation. These methods are described below:-

- Table wise Function Application: **pipe()**

- Row or Column Wise Function Application: **apply()**

- Element wise Function Application: **applymap()**


### Table-wise function application:pipe()

Custom operations can be performed by passing the function and the appropriate number of parameters as pipe arguments. Thus, operation is performed on the whole DataFrame.

For example, if we want to add a value 10 to all the elements in the DataFrame. Then, we can make use of **pipe()** function as follows:-


`def addten(x1,x2):`
       ``return x1+x2`

`df7=df.copy()` 

`df7.pipe(addten,10)``


### Row or Column Wise Function Application: apply()

Arbitrary functions can be applied along the axes of a DataFrame or Panel using the **apply()** method. It takes an optional axis argument. By default, the operation performs column wise, taking each column as an array-like.

`df7.apply(np.mean)`

By passing axis parameter, operations can be performed row wise.

`df7.apply(np.mean,axis=1)`

`df.apply(lambda x: x.max() - x.min())`

### Element Wise Function Application: applymap()

The methods **applymap()** on dataframe and analogously **map()** on series accept any Python function. It takes a single value and returns a single value.

`df7.applymap(lambda x:x*100)`


================================================================================


## 25. Pandas GroupBy operations

A groupby operation involves one of the following operations on the original object. They are as follows:−

- **Splitting** the Object


- **Applying** a function


- **Combining** the results



The split step is the most straightforward out of these. In many situations, we may wish to split the data set into groups and perform operations on those groups.

In the apply functionality, we can perform the following operations :−

- **Aggregation** − compute a summary statistic (or statistics) for each group. Some examples are:- 

     - Compute group sums or means.                  
                  
     - Compute group sizes / counts.


- **Transformation** − perform some group-specific computations and return a like-indexed object. Some examples are :-

    - Standardize data (zscore) within a group.
    
    - Filling NAs within groups with a value derived from each group.



- **Filtration** − discarding the data with some condition.  Some examples are :-

    - Discard data that belongs to groups with only a few members.
    
    - Filter out data based on the group sum or mean.
    
       
- Some combination of the above: **GroupBy** will examine the results of the apply step and try to return a sensibly combined result if it doesn't fit into either of the above two categories.


### Split Data into Groups

Pandas object can be split into any of their objects. There are multiple ways to split an object as follows :-

- obj.groupby('key')

- obj.groupby(['key1','key2'])

- obj.groupby(key,axis=1)


The following example illustrates the idea:-

`df8=df.copy()`

`df8.groupby('Gender')`

view groups of Gender column

`df8.groupby('Gender').groups`

### group by with multiple columns


`df8.groupby(['Gender', 'Age']).groups`


### Iterate through groups


With the groupby object in hand, we can iterate through the object similar to itertools.obj.


`df8_grouped = df8.groupby('Gender')`


`for Age, Occupation in df8_grouped:`

   `print Age`
   
   `print Occupation`
   
  
   
### Select a group


Using the **get_group()** method, we can select a single group.


`df8_grouped = df8.groupby('City_Category')`


`print(df8_grouped.get_group('A')`


### Aggregation functions with groupby

An aggregation function returns a single aggregated value for each group. Once the group by object is created, several aggregation operations can be performed on the grouped data as follows:-

apply aggregation function sum with groupby

`df8.groupby('Gender').sum()`


alternative way to apply aggregation function sum

`df8.groupby('Gender').agg(np.sum)`


Another way to see the size of each group is by applying the **size()** function as follows:-

`df8_grouped = df8.groupby('Gender')`

`print(df8_grouped.agg(np.size))`


### Applying multiple aggregation functions at once

With grouped series, you can also pass a list or dict of functions to do aggregation with, and generate dataframe as output as follows:-

`df8.groupby('Gender')['Purchase'].agg([np.sum, np.mean])`


### Transformations

Transformation on a group or a column returns an object that is indexed the same size of that is being grouped. Thus, the transform should return a result that is the same size as that of a group chunk.

`df9=df.copy()`

`score = lambda x: (x - x.mean()) / x.std()*10`

`print(df9.groupby('Gender')['Purchase'].transform(score).head(5))`


### Filtration

Filtration filters the data on a defined criteria and returns the subset of data. The **filter()** function is used to filter the data.

`df10=df.copy()`

`df10.groupby('Gender').filter(lambda x: len(x) > 4)`


================================================================================


## 26. Pandas merging and joining 


Pandas has full-featured, high performance in-memory join operations that are very similar to relational databases like SQL. These methods perform significantly better than other open source implementations like base::merge.data.frame in R. The reason for this is careful algorithmic design and the internal layout of the data in DataFrame.


Pandas provides a single function, **merge**, as the entry point for all standard database join operations between DataFrame objects.


The syntax of the merge function is as follows:-



`pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, sort=True)`



The description of the parameters used is as follows−


- **left** − A DataFrame object.


- **right** − Another DataFrame object.


- **on** − Columns (names) to join on. Must be found in both the left and right DataFrame objects.


- **left_on** − Columns from the left DataFrame to use as keys. Can either be column names or arrays with length equal to the length of the DataFrame.


- **right_on** − Columns from the right DataFrame to use as keys. Can either be column names or arrays with length equal to the length of the DataFrame.


- **left_index** − If True, use the index (row labels) from the left DataFrame as its join key(s). In case of a DataFrame with a MultiIndex (hierarchical), the number of levels must match the number of join keys from the right DataFrame.


- **right_index** − Same usage as left_index for the right DataFrame.


- **how** − One of 'left', 'right', 'outer', 'inner'. Defaults to inner. 


- **sort** − Sort the result DataFrame by the join keys in lexicographical order. Defaults to True, setting to False will improve the performance substantially in many cases.


Now, I will create two different DataFrames and perform the merging operations on them as follows:-

 merge two dataframes on a key

`pd.merge(batsmen, bowler, on='id')`


merge two dataframes on multiple keys

`pd.merge(batsmen, bowler, on=['id', 'subject_id'])`



### Merge using 'how' argument

The **how** argument to merge specifies how to determine which keys are to be included in the resulting table. If a key combination does not appear in either the left or the right tables, the values in the joined table will be **NA**.

Here is a summary of the how options and their SQL equivalent names −

- **Merge Method** -	**SQL Equivalent**	- **Description**

-  left            -     LEFT OUTER JOIN	-   Use keys from left object

- right	           -     RIGHT OUTER JOIN	-   Use keys from right object

- outer	           -     FULL OUTER JOIN	-   Use union of keys

- inner	           -     INNER JOIN	             -   Use intersection of keys

left join

`pd.merge(batsmen, bowler, on='subject_id', how='left')`


right join

`pd.merge(batsmen, bowler, on='subject_id', how='right')`


outer join

`pd.merge(batsmen, bowler, on='subject_id', how='outer')`


inner join

`pd.merge(batsmen, bowler, on='subject_id', how='inner')`


================================================================================


## 27. Pandas concatenation operation


Pandas provides various facilities for easily combining together series, dataframe and panel objects.


The **concat()** function does all of the heavy lifting of performing concatenation operations along an axis while performing optional set logic (union or intersection) of the indexes (if any) on the other axes.

The syntax of the **concat()** function is as follows:-

`pd.concat(objs, axis=0, join='outer', join_axes=None, ignore_index=False, keys=None, levels=None, names=None, verify_integrity=False, copy=True)`


The description of the arguments is as follows:-


- **objs** − This is a sequence or mapping of Series, DataFrame, or Panel objects.


- **axis** − {0, 1, ...}, default 0. This is the axis to concatenate along.


- **join** − {'inner', 'outer'}, default 'outer'. How to handle indexes on other axis(es). Outer for union and inner for intersection.


- **ignore_index** − boolean, default False. If True, do not use the index values on the concatenation axis. The resulting axis will be labeled 0, ..., n - 1.


- **join_axes** − This is the list of index objects. Specific indexes to use for the other (n-1) axes instead of performing inner/outer set logic.


- **keys** : sequence, default None. Construct hierarchical index using the passed keys as the outermost level. If multiple levels passed, should contain tuples.


- **levels** : list of sequences, default None. Specific levels (unique values) to use for constructing a MultiIndex. Otherwise they will be inferred from the keys.


- **names** : list, default None. Names for the levels in the resulting hierarchical index.


- **verify_integrity** : boolean, default False. Check whether the new concatenated axis contains duplicates. This can be very expensive relative to the actual data concatenation.


- **copy** : boolean, default True. If False, do not copy data unnecessarily.


Now, I will create two dataframes and do concatenation as follows:-

batsmen = pd.DataFrame({
   'id':[1,2,3,4,5],
   'Name': ['Rohit', 'Dhawan', 'Virat', 'Dhoni', 'Kedar'],
   'subject_id':['sub1','sub2','sub4','sub6','sub5']})

bowler = pd.DataFrame(
   {'id':[1,2,3,4,5],
   'Name': ['Kumar', 'Bumrah', 'Shami', 'Kuldeep', 'Chahal'],
   'subject_id':['sub2','sub4','sub3','sub6','sub5']})
team=[batsmen, bowler]

`pd.concat(team)`

associate keys with the dataframes

`pd.concat(team, keys=['x', 'y'])`


We can see the index of the resultant dataframe is duplicated. So each index is repeated.

If the resultant object has to follow its own indexing, we can set **ignore_index** option to true as follows:-

`pd.concat(team, keys=['x', 'y'], ignore_index=True)`


If two objects need to be added along axis=1, then the new columns will be appended as follows:-

`pd.concat(team, axis=1)`



### Concatenating using append

A useful shortcut to concat are the append instance methods on Series and DataFrame. These methods actually predated concat. They concatenate along axis=0, namely the index as follows :−

`batsmen.append(bowler)`


================================================================================


## 28. Reshaping by melt and pivot

### Melt creates wide-to-long format dataframe

When we take a closer look at our original dataframe, we can see that our dataset is not in the tidy data format.

The columns `Product_Category_1`, `Product_Category_2` and `Product_Category_3` contain values of product_category rather than variables. We should reorganize our dataframe into tidy data format.

The **melt()** function is useful to convert a DataFrame from **wide-to-long** format where one or more columns are identifier variables, while all other columns are considered measured variables. The measured variables are then "unpivoted" to the row axis, leaving non-identifier columns, "variable" and "value". The names of those columns can be customized by supplying the var_name and value_name parameters.

We can convert our dataset into long data format using the **melt()** function as follows:-

`df11=df.copy()`

`pd.melt(frame=df11, id_vars=['User_ID','Product_ID', 'Gender','Age','Occupation','City_Category',
                             'Marital_Status','Purchase'],                          
                    value_vars=['Product_Category_1','Product_Category_2','Product_Category_3'], 
                    var_name='Product_Category', value_name='Amount')`


### Pivot creates long-to-wide format dataframe

I have melt three columns `Product_Category_1`, `Product_Category_2` and `Product_Category_3` into a single column named `Product_Category` with **melt()** function. So, I have converted the above dataframe from wide to long format.

Now, I will convert the above column `Product_Category` from long to wide format with **pivot()** function. **pivot()** function takes 3 arguments with the following names - index, columns, and values. As a value for each of these parameters we need to specify a column name in the original table. Then the **pivot()** function will create a new table, whose row and column indices are the unique values of the respective parameters. The cell values of the new table are taken from column given as the values parameter.

`df13=df12[['Product_Category', 'Amount']]`

`df14=df13.pivot(index=None, columns='Product_Category', values='Amount')`


### Reshaping with pivot_table function

Before calling the pivot() function, we need to ensure that our dataset does not have rows with duplicate values for the specified columns. If there are duplicate entries for rows in the dataset, the pivot() function, will throw a value error.

In this case, the **pivot_table()** method comes to rescue. It works like pivot, but it aggregates the values from rows with duplicate entries for the specified columns. The syntax of the pivot_table() function is given below:-


`df.pivot_table(values=None, index=None, columns=None, aggfunc='mean', fill_value=None, margins=False, dropna=True, margins_name='All')`


================================================================================


## 29. Reshaping by stacking and unstacking

There are two other methods called **stack()** and **unstack()** which closely resemble the **pivot()** method. These methods are designed to work together with multiindex objects. The functionality of these methods is described below:-


### Stacking

Stacking means "pivot" a level of the (possibly hierarchical) column labels, returning a DataFrame with an index with a new inner-most level of row labels. So. stacking a dataframe means moving or pivoting the innermost column index to become the innermost row index. 

It returned a reshaped dataframe or series having a multi-level index with one or more new inner-most levels compared to the current dataframe. The new inner-most levels are created by pivoting the columns of the current dataframe.


- if the columns have a single level, the output is a Series.

- if the columns have multiple levels, the new index level(s) is (are) taken from the prescribed level(s) and the output is a DataFrame.

In this case, we looked at a dataframe with single level hierarchical indices on both axes. Stacking takes the most-inner column index (height, weight), makes it the most inner row index and reshuffles the cell values accordingly.

`cols=pd.MultiIndex.from_tuples([('weight', 'kg'), ('weight', 'pounds')])`

`df15=pd.DataFrame([[75,165], [60, 132]],
                 index=['husband', 'wife'],
                 columns=cols)`

`df15.stack()`


## Unstacking

It is the inverse operation of stacking. It means "pivot" a level of the (possibly hierarchical) row index to the column axis, producing a reshaped dataframe with a new inner-most level of column labels.

I will convert the stacked dataframe df16 back to original form as follows:-


`df16.unstack()`


================================================================================


## 30. Options and customization with pandas



Pandas provide API to customize some aspects of its behavior. In most cases, we would like to adjust the display related options.


The API is composed of five relevant functions. They are as follows :−


- 1. **get_option()**


- 2. **set_option()**


- 3. **reset_option()**


- 4. **describe_option()**


- 5. **option_context()**


Let us now understand how the functions operate.


### 1. get_option(param)

**get_option()** takes a single parameter and returns the value as given in the output below –

display maximum rows

`pd.get_option("display.max_rows")`


display maximum columns

`pd.get_option("display.max_columns")`

### 2. set_option(param,value)


**set_option()** takes two arguments and sets the value to the parameter as shown below –


set maximum rows

`pd.set_option("display.max_rows", 80)`

`pd.get_option("display.max_rows")`


# set maximum columns

`pd.set_option("display.max_columns", 30)`

`pd.get_option("display.max_columns")`




### 3. reset_option(param)


**reset_option()** takes an argument and sets the value back to the default value.

 display maximum rows

`pd.reset_option("display.max_rows", 80)`

`pd.get_option("display.max_rows")`


display maximum columns

`pd.reset_option("display.max_columns")`

`pd.get_option("display.max_columns")`



## 4. describe_option(param)

**describe_option()** prints the description of the argument.


description of the display maximum rows parameter

`pd.describe_option("display.max_rows")`






## 5. option_context()

**option_context()** context manager is used to set the option in with statement temporarily. Option values are restored automatically when you exit with block.

set the parameter value with option_context

`with pd.option_context("display.max_rows",10):`
      `print(pd.get_option("display.max_rows"))`
      `print(pd.get_option("display.max_rows"))`


There is a difference between the first and the second print statements. The first statement prints the value set by **option_context()** which is temporary within the with context itself. After with context, the second print statement prints the configured value.


================================================================================


## 31. References


The material in this project is taken from the following books and websites:-


1.	https://en.wikipedia.org/wiki/Pandas_(software)

2.	https://pandas.pydata.org/

3.	https://www.tutorialspoint.com/python_pandas

4.	Python for Data Analysis by Wes McKinney

5.	Mastering pandas by Femi Anthony


