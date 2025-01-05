# Dangling Pointer Due to Deleting Stack Variable

This repository demonstrates a common C++ error: attempting to delete a pointer to a variable allocated on the stack.  Deleting stack-allocated memory leads to undefined behavior and potential crashes.

The `bug.cpp` file shows the erroneous code, while `bugSolution.cpp` provides a corrected version.

## How to Reproduce
1. Clone this repository.
2. Compile `bug.cpp` using a C++ compiler (e.g., g++).
3. Run the executable.  The behavior may vary depending on your system, but it's likely to be unpredictable or crash.

## Solution
The solution in `bugSolution.cpp` avoids the issue entirely by not attempting to deallocate stack memory. Stack memory is managed automatically by the system.