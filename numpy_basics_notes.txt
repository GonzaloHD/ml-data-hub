
# 🧠 NumPy Basics – Quick Notes

## 🔹 Importing NumPy
```
import numpy as np
```

## 🔹 Creating Arrays
```
a = np.array([1, 2, 3])               # 1D array
b = np.array([[1, 2], [3, 4]])        # 2D array

np.zeros((2, 3))                      # 2x3 array of zeros
np.ones((3, 3))                       # 3x3 array of ones
np.eye(3)                             # 3x3 identity matrix
np.full((2, 2), 7)                    # 2x2 array filled with 7
np.arange(0, 10, 2)                   # [0, 2, 4, 6, 8]
np.linspace(0, 1, 5)                  # 5 values from 0 to 1
```

## 🔹 Array Shape & Type
```
a.shape                               # Returns shape (rows, cols)
a.ndim                                # Number of dimensions
a.dtype                               # Data type
a.size                                # Total number of elements
```

## 🔹 Indexing & Slicing
```
a[0]                                  # First element
b[1, 0]                               # Row 1, Col 0

b[0:2, 1]                             # Slice rows 0-1, column 1
b[:, 0]                               # All rows, column 0
b[1, :]                               # Row 1, all columns
```

## 🔹 Array Operations
```
a + b                                 # Element-wise addition
a - b                                 # Element-wise subtraction
a * b                                 # Element-wise multiplication
a / b                                 # Element-wise division

np.dot(a, b)                          # Matrix multiplication
np.sum(a), np.mean(a), np.std(a)     # Aggregations
```

## 🔹 Reshaping & Stacking
```
a.reshape((3, 1))                     # Change shape
a.flatten()                           # Convert to 1D array

np.concatenate([a, b], axis=0)        # Stack vertically
np.concatenate([a, b], axis=1)        # Stack horizontally
```

## 🔹 Boolean Masking & Filtering
```
a = np.array([1, 2, 3, 4, 5])
a[a > 2]                              # [3, 4, 5]

np.where(a % 2 == 0)                  # Indices of even elements
```

## 🔹 Random Numbers
```
np.random.rand(2, 3)                  # Uniform dist [0, 1)
np.random.randn(3)                    # Standard normal dist
np.random.randint(0, 10, (2, 2))      # Random ints in range
```
