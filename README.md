# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# involving mutable variables and function parameters. The `swap` function attempts to swap the values of two mutable variables, but it fails to modify the original variables because of how function parameters are handled in F#.

## Bug Description

The `bug.fs` file contains a function `swap` that aims to swap the values of two mutable variables `x` and `y`. However, the function does not correctly swap the values.  The issue is because the function takes copies of the variables as input, and any changes inside the function do not affect the original variables outside the function.

## Solution

The `bugSolution.fs` file provides a corrected version of the `swap` function that uses the `&` operator to pass the mutable variables by reference. This ensures that changes made inside the function directly affect the original variables.

## How to reproduce

1. Clone this repo.
2. Open the `bug.fs` file in a F# editor or IDE.
3. Compile and run the code. Observe that the values of `x` and `y` are not swapped.
4. Open the `bugSolution.fs` file. Compile and run the code. Observe that the values are correctly swapped. 