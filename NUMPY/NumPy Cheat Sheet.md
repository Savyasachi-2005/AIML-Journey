
# NumPy Cheat Sheet

Welcome to your quick reference for **NumPy**! This guide covers the essentials for array creation, manipulation, and mathematical operations—perfect for data analysis, machine learning, and deep learning projects.

***

## 1. Creating Arrays

| Function | Description | Example |
| :-- | :-- | :-- |
| `np.array()` | Create 1D or 2D array | `arr1d = np.array([1,2,3])` |
| `np.zeros((rows,cols))` | Array of zeros | `np.zeros((2,3))` |
| `np.ones((n,))` | Array of ones | `np.ones((3,))` |
| `np.arange(start, stop, step)` | Range of numbers | `np.arange(0,10,2)` |
| `np.linspace(start, stop, num)` | Equally spaced numbers | `np.linspace(0,1,5)` |
| `np.random.rand(rows,cols)` | Random numbers | `np.random.rand(2,2)` |


***

## 2. Array Properties

| Property | Description |
| :-- | :-- |
| `arr.shape` | Dimensions of the array |
| `arr.size` | Total number of elements |
| `arr.dtype` | Data type of elements |


***

## 3. Indexing \& Slicing

| Operation | Example |
| :-- | :-- |
| Access element | `arr[1,0]` |
| Slice rows | `arr[1:4]` |
| Slice columns | `arr[:,0]` |


***

## 4. Array Operations

- **Element-wise:** `+`, `-`, `*`, `/`
- **NumPy functions:** `np.add(a,b)`, `np.subtract(a,b)`, `np.multiply(a,b)`, `np.divide(a,b)`
- **Matrix multiplication:** `np.dot(a,b)`
- **Transpose:** `arr.T`
- **Reshape:** `arr.reshape((rows,cols))`

***

## 5. Useful Functions

| Function | Description |
| :-- | :-- |
| `np.mean(arr)` | Mean of elements |
| `np.sum(arr)` | Sum of elements |
| `np.min(arr)` / `np.max(arr)` | Minimum / Maximum |
| `np.std(arr)` / `np.var(arr)` | Standard deviation / Variance |
| `np.cumsum(arr)` | Cumulative sum |
| `np.cumprod(arr)` | Cumulative product |
| `np.sqrt(arr)` | Square root |
| `np.exp(arr)` | Exponential |
| `np.log(arr)` | Natural logarithm |
| `np.abs(arr)` | Absolute value |
| `np.median(arr)` | Median value |
| `np.percentile(arr, p)` | p-th percentile |
| `np.corrcoef(a,b)` | Correlation coefficient |
| `np.cov(a,b)` | Covariance matrix |


***

## 6. Broadcasting

Allows operations between arrays of different shapes.

- *Example:* Add a vector to each row of a matrix

***

## 7. Sorting \& Unique

- `np.sort(arr)` → Sorted array
- `np.unique(arr)` → Unique elements

***

## 8. Conditional Operations

- `arr[arr > 2]` → Elements satisfying condition
- `np.where(arr > 2)` → Indices of elements satisfying condition

***

## 9. Stacking Arrays

- **Vertical stack:** `np.vstack((a,b))`
- **Horizontal stack:** `np.hstack((a,b))`

***

## 10. Repeating \& Tiling

- **Repeat elements:** `np.repeat(a, 2)`
- **Tile array:** `np.tile(a, 3)`

***

## 11. Saving \& Loading

- **Save:** `np.save('file.npy', arr)`
- **Load:** `arr = np.load('file.npy')`

***

> **Tip:** Mastering these basics will make advanced Python data science much easier. For more, check out the [NumPy documentation](https://numpy.org/doc/).

