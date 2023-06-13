# Disjoint Set Implementation

This repository contains a Python implementation of the Disjoint Set data structure using an array-based approach. The Disjoint Set, also known as the Union-Find data structure, is used to efficiently manage a partitioning of a set into disjoint subsets.

## Usage

To use the Disjoint Set implementation in your Python project, follow these steps:

1. Clone or download the repository to your local machine.
2. Import the `ArrayDisjointSet` class from the `disjoint_set.py` file into your Python script.
3. Create an instance of the `ArrayDisjointSet` class by providing the desired size of the set.
4. Use the available methods to perform operations on the Disjoint Set:
   - `make_set(x)`: Creates a new set with a single element `x`.
   - `find(x)`: Returns the representative element of the set that `x` belongs to.
   - `union(x, y)`: Merges the sets that contain elements `x` and `y`.
   - `is_same_set(x, y)`: Checks if elements `x` and `y` belong to the same set.

Here's an example of how to use the Disjoint Set implementation:

```python
from disjoint_set import ArrayDisjointSet

# Create a Disjoint Set with a size of 10
set = ArrayDisjointSet(10)

# Make sets with individual elements
for i in range(10):
    set.make_set(i)

# Merge sets
set.union(0, 1)
set.union(2, 3)
set.union(4, 5)
set.union(6, 7)
set.union(8, 9)

# Check if elements belong to the same set
print(set.is_same_set(0, 1))  # True
print(set.is_same_set(1, 3))  # False

# Find the representative element of an element's set
print(set.find(4))  # 4
print(set.find(9))  # 8
```
