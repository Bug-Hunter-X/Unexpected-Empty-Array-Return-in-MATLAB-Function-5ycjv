# Unexpected Empty Array Return in MATLAB Function

This repository demonstrates a common but subtle error in MATLAB: returning an empty array (`[]`) when a function encounters an unexpected condition instead of handling it more gracefully with `NaN` or by throwing an error.  This can mask problems and lead to difficult-to-find bugs.

## Bug Description
The `myFunction` in `bug.m` returns an empty array when a specific condition is not met. This can cause downstream calculations to fail silently, producing unexpected results, or breaking code that isn't designed to handle empty arrays in that context.

## Solution
The solution, in `bugSolution.m`, addresses this by returning `NaN` when the unexpected condition arises.  This makes the error explicit and simplifies debugging by allowing for better error handling in calling functions.  Alternatives such as throwing an error might be more suitable depending on the application and the seriousness of the condition.

## How to Use
1. Clone the repository.
2. Open `bug.m` to see the code with the issue.
3. Open `bugSolution.m` to see the improved code.