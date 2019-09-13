
**Routine Name:** `maceps32bit`

**Author:** Jaxton Winder

**Language:** Python 3.7.4.

This routine is dependent on numpy, a mathematical library that comes with many distributions of Python. Use pip installer to run ``pip install numpy`` if numpy is not present in your Python distribution.

**Description/Purpose:** This routine tests the machine precision of a 32-bit single floating point value. This routine will start epsilon to be a double precision float of 1. It then iterates epsilon to be smaller and smaller to compute the smallest possible value a double precision type can hold and perform meaningful computations with. It prints the result of each iteration to the screen.

**Input:** No input is required.

**Output:** Any call to the function will print to the console each iteration on a new line until it reaches the last iteration with a meaningful calculation.

**Usage/Example:**

There are two ways to call the function, either by directly running the python file or by calling the function from the shared library.

Method 1:

    python maceps32bit.py

Method 2 (after math4610lib has been installed with pip installer):

    import math4610lib
    maceps32bit()

Output from the lines above:

    iteration 0: 1.0
    iteration 1: 0.5
    iteration 2: 0.25
    ...
    iteration 22: 2.3841858e-07
    iteration 23: 1.1920929e-07
    finish

**Implementation/Code:** The following is the code for `AbsoluteError(value, valueApprox)`

    def maceps32bit():
        import numpy as np

        x, xStar = np.float32(1), np.float32(1)
        epsilon = np.float32(1)
        iterationCount = 0

        while abs((xStar + epsilon) - x) != 0:
            print(f"iteration {iterationCount}: " + str((xStar + epsilon) - x))
            epsilon = np.float32(epsilon * .5)
            iterationCount += 1

    print("finish")

**Last Modified:** September/2019
