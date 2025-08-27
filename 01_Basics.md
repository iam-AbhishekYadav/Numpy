# Numpy


# # What is Numpy ?

- NumPy(Numerical Python) is a fundamental library for Python numerical computing.
- NumPy aims to provide an array object that is up to 50x faster than traditional Python lists.


# # Installation of Numpy

**Installation through UV.**

## UV

- UV is a Python package and project manager.
- It is used for fast dependency installation.
- It can build and publish Python packages.
- It automatically handles virtual environments.

### Steps

**(i)** Open integrated terminal  
**(ii)** pip install uv  
**(iii)** uv venv  
**(iv)** Write --> `.venv\Scripts\activate`  
**(v)** uv pip install numpy  
**(vi)** uv pip install ipykernel  
**(vii)** python -m ipykernel install --user --name=.venv --display-name "Python (.venv)"  
**(viii)** Then create a fime `Name.ipynb` and Select kernel  
**(ix)** Run `import numpy as np`  

# # Creating Array

- The object in Numpy is call ndarray
- We can also pass a list, tuple, or any array like obect with array() method and it will be coverted to ndarray.

``` py
import numpy as np

arr = np.array([1,2,3,4,5])
print(arr)                                                      # Output : [1 2 3 4 5]

arr2 =np.array([[1,2,3,4],[5,6,7,8]])
print(arr2)                                                     # Output : [[1 2 3 4]
                                                                #           [5 6 7 8]]

print(type(arr))                                                # Output : <class 'numpy.ndarray'>
print(type(arr2))                                               # Output : <class 'numpy.ndarray'>
```

### Chaeck How many dimensions the array have 

- We can check array dimensions by **`ndim attribute`**

``` py
import numpy as np

a = np.array(42)
b = np.array([1,2,3,4,5])
c = np.array([[1,2,3,4],[5,6,7,8]])
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(a.ndim, "Dimensional array")                          # Output : 0 Dimensional array
print(b.ndim, "Dimensional array")                          # Output : 1 Dimensional array
print(c.ndim, "Dimensional array")                          # Output : 2 Dimensional array
print(d.ndim, "Dimensional array")                          # Output : 3 Dimensional array
```

# # Array from Scratch

### numpy.zeros

- It will create an array filled with 0 values with the specified shape.
- The default dtype is float64

``` py
imort numpy as np

zeros = np.zeros((3,4))
print("Zeros array : ", zeros)                         # Output : Zeros array : [[0. 0. 0. 0.]
                                                       #                         [0. 0. 0. 0.]
                                                       #                         [0. 0. 0. 0.]]
```

### numpy.ones

- It will create an array filled with 1 values.


``` py
imort numpy as np

ones = np.ones((2,3))
print("Ones array : \n", ones)                         # Output : Ones array : [[1. 1. 1.]
                                                       #                        [1. 1. 1.]]
```

### numpy.full

- It will return a new array with the same shape and type as a given array filled with a fill_value.


``` py
imort numpy as np

full = np.full((2,2), 7)
print("Full array :\n", full)                         # Output : Full array : [[7 7]
                                                      #                        [7 7]]
```

### numpy.random

- It  will create an array filled with random values between 0 and 1.
- It is included with the numpy.random library.

``` py
import numpy as np

random = np.random.random((2,3))
print("Random array :\n", random)                         # Output : Random array : [[0.42986452 0.81999175 0.95778097]
                                                          #                          [0.15036669 0.56415203 0.36115213]]
```

### Sequence ---> numpy.arrange 

- It creates an array of evenly spaced values within a given interval.

``` py
import numpy as np

sequence = np.arange(0, 10, 2)
print("Sequence array :\n", sequence)                          # Output : Sequence array : [0 2 4 6 8]
``` 


# # Basics Array Properties

Here are some of the commonly used NumPy attributes:

**(i)** `ndim` ---> Returns number of dimension of the array  
**(ii)** `size` ---> Returns number of elements in the array  
**(iii)** `dtype` ---> Returns data type of elements in the array  
**(iv)** `shape` ---> Returns the size of the array in each dimension  

``` py
import numpy as np

arr3 = np.array([[1,2,3],
                 [4,5,6]])

print("Dimension", arr3.ndim)                                    # Output : Dimension of array : 2
print("No. of elements", arr3.size)                              # Output : No. of elements : 6
print("Data type of elements", arr3.dtype)                       # Output : Data type of elements : int64
print("Shape of array", arr3.shape)                              # Output : Shape of array : (2, 3)
```

# # Array Reshaping

**(i)** `reshape` ---> Gives a new shape to an array without changing its data.  
**(ii)** `flattened` ---> Return a copy of the array collapsed into one dimension.  
**(iii)** `ravel` --->  Return a view of the array collapsed into one dimension.  
**(iv)** `transpose` ---> Swaps the axes of the given array.  

``` py
import numpy as np

arr = np.arange(12)
print("Original array", arr)                           # Output : Original array : [ 0  1  2  3  4  5  6  7  8  9 10 11]

reshaped = arr.reshape((3,4))
print("Reshaped array :",reshaped)                     # Output : Reshaped array : [[ 0  1  2  3]
                                                       #                            [ 4  5  6  7]
                                                       #                            [ 8  9 10 11]]
flattened = reshaped.flatten()
print("Flattened array :", flattened)                  # Output : Flattened array : [ 0  1  2  3  4  5  6  7  8  9 10 11]

raveled = reshaped.ravel()
print("Raveled array :", raveled)                      # Output : Raveled array : [ 0  1  2  3  4  5  6  7  8  9 10 11]

transpose = reshaped.transpose()
print("Transpose array :", transpose)                  # Output : Transpose array : [[ 0  4  8]
                                                       #                             [ 1  5  9]
                                                       #                             [ 2  6 10]
                                                       #                             [ 3  7 11]]
```













