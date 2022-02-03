# Introduction to Numpy 

Numpy stands for Numerical Python and it's a fundamental package for scientific computing in Python. NumPy provides python with an extensive math library capable of performing numerical computations effectively and efficiently. 


In the following lessons we will learn:

1. How to import NumPy
2. How to create multidimensional NumPy ndarrays using various methods
3. How to access and change elements in ndarrays
4. How to load and save ndarrays
5. How to use slicing to select or change subsets of an ndarray
6. Understand the difference between a view and a copy an of ndarray
7. How to use Boolean indexing and set operations to select or change subsets of an ndarray
8. How to sort ndarrays
9. How to perform element-wise operations on ndarrays
10. Understand how NumPy uses broadcasting to perform operations on ndarrays of different sizes.

# Glossary 

## Category ==> General Purpose 
* numpy.ndarray.dtype = Returns the data-type of the elements on the array. 
* numpy.ndarray.ndim = Return the number of array dimensions(rank) e.g it will return 2 for 4*3 array. 

* numpy.ndarray.shape = Return a tuple representing the array dimensions, e.g., it will return (rows,columns) for a rank 2 array.

* numpy.ndarray.size = Return the number of elements present in the array.

* numpy.save = Save an array to .npy (numpy) format.

* numpy.load = Load array from the .npy files. 

* numpy.random.random = Return random floats values from the interval [0.0, 1.0), in a specified shape.

* numpy.random.randint = Return random integers from the half-open interval [a, b), in a specified shape.

* numpy.random.permutation = Return a randomly permuted sequence from the given list

* numpy.reshape = Returns an array containing the same elements with a new shape, without affecting the the original array.


## Category ==> Array Creation 

* numpy.ones = Return a new array of given shape and type, filled with 1s.

* numpy.zeros = Return a new array of given shape and type, filled with 0s.

* numpy.full = 	Return a new array of given shape and type, filled with a specific value.

* numpy.eye = 	Return a 2-D array with 1s on the diagonal and 0s elsewhere.

* numpy.unique = Return the sorted unique elements of an array.

* numpy.array = Create an n-dimensional array.

* numpy.arange = Return evenly spaced values within a given half-open interval [a, b).

* numpy.linspace = 	Return evenly spaced numbers over a specified interval [a,b].

* numpy.ndarray.copy = Returns a copy of the array  


## Category ==> Operating with Elements and Indices  

numpy.insert	Insert values along the given axis before the specified indices.

numpy.delete	Return a new array, after deleting sub-arrays along a specified axis.

numpy.append	Append values at the end of the specified array.

numpy.hstack	Return a stacked array formed by stacking the given arrays in 
sequence horizontally (column-wise).

numpy.vstack	Return a stacked array formed by stacking the given arrays, will be at least 2-D, in sequence vertically (row-wise).

numpy.sort	Return a sorted copy of an array.

numpy.ndarray.sort	Sort an array in-place

## Category: Set Operations 

numpy.intersect1d	Find the intersection of two arrays.

numpy.setdiff1d	Find the set difference of two arrays.

numpy.union1d	Return the unique, sorted array of values that are in either of the two input arrays.


## Category: Arithmetic and Stattistical Operations 

numpy.add	Element-wise add given arrays

numpy.subtract	Subtract arguments of given arrays, element-wise.

numpy.multiply	Multiply arguments of given arrays, element-wise.

numpy.divide	Returns a true division of the inputs, element-wise.

numpy.exp	Calculate the exponential of all elements in the input array.

numpy.power	First array elements raised to powers from second array, 
element-wise.

numpy.sqrt	Return the non-negative square-root of an array, element-wise.
numpy.ndarray.min	Return the minimum along the specified axis.
numpy.ndarray.max	Return the maximum along a given axis.
numpy.mean
numpy.ndarray.mean	Compute the arithmetic mean along the specified axis.
numpy.median	Compute the median along the specified axis.


# Introduction to Pandas
Pandas is a package for data manipulation and analysis in Python. The name Pandas is derived from the econometrics term Panel Data. Pandas incorporates two additional data structures into Python, namely Pandas Series and Pandas DataFrame. These data structures allow us to work with labeled and relational data in an easy and intuitive manner. These lessons are intended as a basic overview of Pandas and introduces some of its most important features.

# In the following lessons you will learn:

How to import Pandas
How to create Pandas Series and DataFrames using various methods
How to access and change elements in Series and DataFrames
How to perform arithmetic operations on Series
How to load data into a DataFrame
How to deal with Not a Number (NaN) values
The following lessons assume that you are already familiar with NumPy and have gone over the previous NumPy lessons. Therefore, to avoid being repetitive we will omit a lot of details already given in the NumPy lessons. Consequently, if you haven't seen the NumPy lessons we suggest you go over them first.

# Why Use Pandas?
The recent success of machine learning algorithms is partly due to the huge amounts of data that we have available to train our algorithms on. However, when it comes to data, quantity is not the only thing that matters, the quality of your data is just as important. It often happens that large datasets don’t come ready to be fed into your learning algorithms. More often than not, large datasets will often have missing values, outliers, incorrect values, etc… Having data with a lot of missing or bad values, for example, is not going to allow your machine learning algorithms to perform well. Therefore, one very important step in machine learning is to look at your data first and make sure it is well suited for your training algorithm by doing some basic data analysis. This is where Pandas come in. Pandas Series and DataFrames are designed for fast data analysis and manipulation, as well as being flexible and easy to use. Below are just a few features that makes Pandas an excellent package for data analysis:

# Allows the use of labels for rows and columns
Can calculate rolling statistics on time series data
Easy handling of NaN values
Is able to load data of different formats into DataFrames
Can join and merge different datasets together
It integrates with NumPy and Matplotlib
For these and other reasons, Pandas DataFrames have become one of the most commonly used Pandas object for data analysis in Python.


# Pandas Series
A Pandas series is a one-dimensional array-like object that can hold many data types, such as numbers or strings, and has an option to provide axis labels.

# Difference between NumPy ndarrays and Pandas Series
1. One of the main differences between Pandas Series and NumPy ndarrays is that you can assign an index label to each element in the Pandas Series. In other words, you can name the indices of your Pandas Series anything you want.
2. Another big difference between Pandas Series and NumPy ndarrays is that Pandas Series can hold data of different data types.

> One great advantage of Pandas Series is that it allows us to access data in many different ways. Elements can be accessed using index labels or numerical indices inside square brackets, [ ], similar to how we access elements in NumPy ndarrays. Since we can use numerical indices, we can use both positive and negative integers to access data from the beginning or from the end of the Series, respectively. Since we can access elements in various ways, in order to remove any ambiguity to whether we are referring to an index label or numerical index, Pandas Series have two attributes, .loc and .iloc to explicitly state what we mean. The attribute .loc stands for location and it is used to explicitly state that we are using a labeled index. Similarly, the attribute .iloc stands for integer location and it is used to explicitly state that we are using a numerical index. Let's see some examples:


> Pandas DataFrames are two-dimensional data structures with labeled rows and columns, that can hold many data types. If you are familiar with Excel, you can think of Pandas DataFrames as being similar to a spreadsheet. We can create Pandas DataFrames manually or by loading data from a file. In this lesson, we will start by learning how to create Pandas DataFrames manually from dictionaries, and later we will see how we can load data into a DataFrame from a data file.


# There are several things to notice here, as explained below:

We see that DataFrames are displayed in tabular form, much like an Excel spreadsheet, with the labels of rows and columns in bold.
Also, notice that the row labels of the DataFrame are built from the union of the index labels of the two Pandas Series we used to construct the dictionary. And the column labels of the DataFrame are taken from the keys of the dictionary.
Another thing to notice is that the columns are arranged alphabetically and not in the order given in the dictionary. We will see later that this won't happen when we load data into a DataFrame from a data file.
The last thing we want to point out is that we see some NaN values appear in the DataFrame. NaN stands for Not a Number, and is Pandas way of indicating that it doesn't have a value for that particular row and column index. For example, if we look at the column of Alice, we see that it has NaN in the watch index. You can see why this is the case by looking at the dictionary we created at the beginning. We clearly see that the dictionary has no item for Alice labeled watches. So whenever a DataFrame is created, if a particular column doesn't have values for a particular row index, Pandas will put a NaN value there.
If we were to feed this data into a machine learning algorithm we will have to remove these NaN values first. In a later lesson, we will learn how to deal with NaN values and clean our data. For now, we will leave these values in our DataFrame.


> Just as we can add rows and columns we can also delete them. To delete rows and columns from our DataFrame we will use the .pop() and .drop() methods. The .pop() method only allows us to delete columns, while the .drop() method can be used to delete both rows and columns by use of the axis keyword. Let's see some examples


# Eliminating NaN Values
Now that we learned how to know if our dataset has any NaN values in it, the next step is to decide what to do with them. In general, we have two options, we can either delete or replace the NaN values. In the following examples, we will show you how to do both.

We will start by learning how to eliminate rows or columns from our DataFrame that contain any NaN values. The .dropna(axis) method eliminates any rows with NaN values when axis = 0 is used and will eliminate any columns with NaN values when axis = 1 is used.

Tip: Remember, you learned that you can read axis = 0 as "down" and axis = 1 as "across" the given Numpy ndarray or Pandas dataframe object.

Function/Method	Description
pandas.read_csv(relative_path_to_file) = 	Reads a comma-separated values (csv) file present at relative_path_to_file and loads it as a DataFrame

pandas.DataFrame(data)	= Returns a 2-D heterogeneous tabular data. Note: There are other optional arguments as well that you can use to create a dataframe.

pandas.Series(data, index)	= Returns 1-D ndarray with axis labels


pandas.DataFrame.shape = 	Returns a tuple representing the dimensions
pandas.Series.ndim
pandas.DataFrame.ndim	= Returns the number of the dimensions (rank). It will return 1 in case of a Series

pandas.Series.size
pandas.DataFrame.size	Returns the number of elements

pandas.Series.values	Returns the data available in the Series

pandas.Series.index	Returns the indexes available in the Series

pandas.DataFrame.isnull()	Returns a same sized object having True for NaN elements and False otherwise.

pandas.DataFrame.count(axis)	Returns the count of non-NaN values along the given axis. If axis=0, it will count down the dataframe, meaning column-wise count of non-NaN values.

pandas.DataFrame.head([n])	Return the first n rows from the dataframe. By default, n=5.

pandas.DataFrame.tail([n])	Return the last n rows from the dataframe. By default, n=5. Supports negative indexing as well.

pandas.DataFrame.describe()	Generate the descriptive statistics, such as, count, mean, std deviation, min, and max.

pandas.DataFrame.min()	Returns the minimum of the values along the given axis.

pandas.DataFrame.max()	Returns the maximum of the values along the given axis.

pandas.DataFrame. mean()	Returns the mean of the values along the given axis.

pandas.DataFrame.corr()	Compute pairwise correlation of columns, excluding NA/null values.

pandas.DataFrame.rolling(windows)	Provide rolling window calculation, such as pandas.DataFrame.rolling(15).mean() for rolling mean over window size of 15.

pandas.DataFrame.loc[label]	Access a group of rows and columns by label(s)

pandas.DataFrame.groupby(mapping_function)	Groups the dataframe using a given mapper function or or by a Series of columns.

# Category: Manipulation
Function/Method	Description
pandas.Series.drop(index)	Drops the element positioned at the given index(es)

pandas.DataFrame.drop(labels)	Drop specified labels (entire columns or rows) from the dataframe.

pandas.DataFrame.pop(item)	Return the item and drop it from the frame. If not found, then raise a KeyError.

pandas.DataFrame.insert(location, column, values)	Insert column having given values into DataFrame at specified location.

pandas.DataFrame.rename(dictionary-like)	Rename label(s) (columns or row-indexes) as mentioned in the dictionary-like

pandas.DataFrame.set_index(keys)	Set the DataFrame's row-indexes using existing column-values.

pandas.DataFrame.dropna(axis)	Remove rows (if axis=0) or columns (if axis=1) that contain missing values.

pandas.DataFrame.fillna(value, method, axis)	Replace NaN values with the specified value along the given axis, and using the given method (‘backfill’, ‘bfill’, ‘pad’, ‘ffill’, None)

pandas.DataFrame.interpolate(method, axis)	Replace the NaN values with the estimated value calculated using the given method along the given axis.