# Off-by-one error in C++ vector iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The error occurs because the loop condition `i <= vec.size()` attempts to access an element beyond the valid range of indices.  Vectors in C++ are zero-indexed, meaning the last valid index is `vec.size() - 1`.

The `bug.cpp` file contains the erroneous code, while `bugSolution.cpp` provides the corrected version.

**Understanding the Error**

The off-by-one error is a subtle but frequently encountered bug, especially when dealing with arrays and vectors.  It's important to carefully consider loop conditions to prevent accessing memory outside the allocated bounds.

**How to fix it**

The solution is to change the loop condition to `i < vec.size()`. This ensures that the loop iterates only over valid indices.