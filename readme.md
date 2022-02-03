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
