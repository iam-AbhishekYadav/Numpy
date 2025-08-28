# Numpy Array Operations

# # Sclicing Array

- Slicing in python means taking elements from one given index to another given index.
- We pass slice instead of index like this: **[ start : end ]** or **[ start : end : step ]**

### Basic Sclicing

``` py
import numpy as np

arr = np.array([1,2,3,4,6,7,8,9,10])

print("Basic Sclicing :", arr[2:7])                 # Output : Basic Sclicing : [3 4 6 7 8]
print("With Step :", arr[1:8:2])                    # Output : With Step : [2 4 7 9]
print("Negative Indexting :", arr[-3])              # Output : Negative Indexting : 8
```

### 2d Array

``` py
import numpy as np

arr_2d = np.array([[1,2,3],
                   [4,5,6],
                   [7,8,9]])

print("Specific element :", arr_2d[1,2])                 # Output : Specific element : 6
print("Entire row :", arr_2d[1])                         # Output : Entire row : [4 5 6]
print("Entire column :", arr_2d[:,1])                    # Output : Entire row : [2 5 8]
```


# # Sorting 

- Sorting means putting elements in an ordered sequence.

``` py
import numpy as np

# Basic Array Sorting

unsorted = np.array([3,1,4,1,5,9,2,6])
print("Sorted Array", np.sort(unsorted))                                               # Output : Sorted Array : [1 1 2 3 4 5 6 9]



# 2D Array Sorting

arr_2d = np.array([[3,1],
                   [1,2],
                   [2,3]])

print("Sorted 2D Array by Column :", np.sort(arr_2d, axis=0))                          # Output : Sorted 2D Array by Column : [[1 1]
                                                                                       #                                       [2 2]
                                                                                       #                                       [3 3]]

print("Sorted 2D Array by Row :", np.sort(arr_2d, axis=))                              # Output : Sorted 2D Array by Column : [[1 3]
                                                                                       #                                       [1 2]
                                                                                       #                                       [2 3]] 
``` 

# # Filtering

- Filtering means taking the elements which satisfy the condition given by us.

``` py
import numpy as np

numbers = np.array([1,2,3,4,5,6,7,8,9,10])
even_number = numbers[numbers % 2 == 0]

print("Even Number :", even_number)                    # Output : Even Number : [ 2  4  6  8 10]
```
## Filter with Mask

**`Mask`**---> It is a expression which evaluate.

``` py
import numpy as np

numbers = np.array([1,2,3,4,5,6,7,8,9,10])
mask = numbers > 5

print("Number greater than 5 :", numbers[mask])                    # Output : Number greater than 5 : [ 6  7  8  9 10]
```

# # Fancy Indexing

- It is also known as Advanced Indexing
- It allows us access elements of an array by using another array or list of indices.


``` py
import numpy as np
arr = np.array([10, 20, 30, 40, 50])
indices = [0, 2, 4]

print(arr[indices])                            # Output : [10 30 50]
```


# # Where()

- It is used for conditional operations on arrays.
- It functions similarly to an if-else statement but is vectorized, meaning it operates efficiently across entire arrays rather than element by element.

### Syntax - 1

``` py
import numpy as np

numbers = np.array([1,2,3,4,5,6,7,8,9,10])
where_result = np.where(numbers > 5)

print(where_result)                                      # Output : Stores the indexing of array --> (array([5, 6, 7, 8, 9]),)
print("NP Where", numbers[where_result])                 # Output : NP Where : [ 6  7  8  9 10]
```

### Syntax - 2 

``` py
import numpy as np

numbers = np.array([1,2,3,4,5,6,7,8,9,10])
condition_array = np.where(numbers > 5, numbers * 5, numbers)

# This works like if - else

# if(numbers > 5){  
#     numbers * 4  
# } else {  
#     numbers  
# }

print("Conditional Array :",condition_array)                 # Output : Conditional Array : [ 1  2  3  4  5 30 35 40 45 50]
```

# # Merging of Array

- We acan combines multiple arrays into a single array along a specified axis by **`numpy.concatenate()`** function.
- Join a sequence of arrays along an existing axis.


### What not to do 

This will add the arrays 

``` py
import numpy as np

arr1 = np.array([1,2,3])
arr2 = np.array([4,5,6])

combine = arr1 + arr2  
print("Combined Array :",combine)                  # Output : Combined Array : [5 7 9]
```


### What to do

``` py
import numpy as np

arr1 = np.array([1,2,3])
arr2 = np.array([4,5,6])

combine = np.concatenate((arr1, arr2))
print("combined Array :",combine)                  # Output : Combined Array : [1 2 3 4 5 6]
```


# # Array Compatibility

- It checks the shape/Dimensions of the array are some or not

``` py
import numpy as np

a = np.array([1,2,3])
b = np.array([4,5,6])
c = np.array([7,8,9,10])

print("Compatibility Shape :",a.shape == b.shape)                  # Output : Compatibility Shape : True
print("Compatibility Shape :",a.shape == c.shape)                  # Output : Compatibility Shape : False
```











































































