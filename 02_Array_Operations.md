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

unsorted = np.array([3,1,4,1,5,9,2,6])
print("Sorted Array", np.sort(unsorted))                                               # Output : Sorted Array : [1 1 2 3 4 5 6 9]

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












































