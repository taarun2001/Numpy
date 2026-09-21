# Numpy
NumPy Fundamentals & Practical GuideA concise reference and tutorial covering core NumPy concepts, array initialization, vectorization, indexing, and array manipulations for data science and machine learning workflows.Table of ContentsOverviewKey FeaturesInstallationCore Concepts & Code Examples1. Array Creation & Type Casting2. Multi-dimensional Arrays & Special Initializers3. Element-wise Operations (Vectorization)4. Slicing & Boolean Indexing5. Reshaping & Structural OperationsEcosystem IntegrationOverviewNumPy (Numerical Python) is the foundational library for scientific computing in Python. It provides high-performance N-dimensional array objects (ndarray) and comprehensive mathematical routines for array operations, linear algebra, and data manipulation.Compared to native Python lists, NumPy arrays offer optimized performance, memory efficiency, and concise vectorized syntax.Key FeaturesHigh Performance: Implemented in C for fast array computation and vectorized operations.N-Dimensional Arrays (ndarray): Efficient storage and manipulation of homogeneous numerical data.Broadcasting & Vectorization: Execute mathematical operations on whole arrays without explicit for loops.Ecosystem Compatibility: Seamless integration with data analysis and machine learning tools, including Pandas, Matplotlib, SciPy, and Scikit-Learn.InstallationInstall NumPy using pip:pip install numpy
Core Concepts & Code Examples1. Array Creation & Type CastingImport NumPy and create basic arrays. When mixed types are passed, NumPy automatically upcasts elements to maintain data homogeneity (e.g., converting integers to strings):import numpy as np

# Creating an array (upcasted to string type due to mixed types)
narray = np.array([1, 2, 3, "hello"])

print(narray)         # Output: array(['1', '2', '3', 'hello'], dtype='<U21')
print(type(narray))   # Output: <class 'numpy.ndarray'>
print(narray.shape)   # Output: (4,)
2. Multi-dimensional Arrays & Special InitializersInitialize multi-dimensional structures or arrays with specific initial values:# Creating a 2D array from nested lists
n2 = [[1, 2], [3, 4]]
arr_2d = np.array(n2)

# Initializing a 3x4 array of zeros
zeros_arr = np.zeros((3, 4))
print(zeros_arr)
3. Element-wise Operations (Vectorization)NumPy allows element-wise arithmetic without looping:n1 = np.array([3, 4, 5])
n2 = np.array([6, 7, 8])

# Element-wise multiplication
result = n1 * n2
print(result)  # Output: [18, 28, 40]
4. Slicing & Boolean IndexingExtract sub-regions or filter elements based on conditions:arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])

# Basic slicing
print(arr[0:4])  # Output: [1, 2, 3, 4]

# Boolean filtering (masking)
filtered_arr = arr[arr > 3]
print(filtered_arr)  # Output: [4, 5, 6, 7, 8, 9]
5. Reshaping & Structural OperationsChange array dimensions without altering data content:# Generate a 1D sequence of numbers
arr = np.arange(10)
print(len(arr))  # Output: 10

# Reshape 1D array (10 elements) to 2D matrix (2x5)
reshaped_arr = arr.reshape(2, 5)
print(reshaped_arr)
# Output:
# [[0 1 2 3 4]
#  [5 6 7 8 9]]
Ecosystem IntegrationNumPy serves as the fundamental building block across the scientific Python ecosystem:LibraryPrimary Use CasePandasHigh-level data analysis and tabular data manipulation built on NumPy arrays.Matplotlib / SeabornData visualization and plotting using NumPy inputs.Scikit-LearnMachine learning model training, evaluation, and data preprocessing pipelines.
