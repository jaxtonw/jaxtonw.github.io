
**Routine Name:** `maceps64bit`

**Author:** Jaxton Winder

**Language:** Python 3.7.4.

**Description/Purpose:** This routine tests the machine precision of a 64-bit double floating point value. This routine will start epsilon to be a double precision float of 1. It then iterates epsilon to be smaller and smaller to compute the smallest possible value a double precision type can hold and perform meaningful computations with. It then prints the result of each iteration to the console.

**Input:** There are no inputs required.

**Output:** Any call to the function will print to the console each iteration on a new line until it reaches the last iteration with a meaningful calculation.

**Usage/Example:**

There are two ways to call the function, either by directly running the python file or by calling the function from the shared library.

Method 1:

    python maceps64bit.py

Method 2 (after math4610lib has been installed with pip installer):

    import math4610lib
    maceps64bit()

Output from the lines above:

    iteration 0: 1.0
    iteration 1: 0.5
    ...
    iteration 51: 4.440892098500626e-16
    iteration 52: 2.220446049250313e-16
    finish

**Implementation/Code:** The following is the code for `maceps64bit`

    def maceps64bit():
        x, xStar = float(1), float(1)
        epsilon = float(1)
        iterationCount = 0

        while abs((xStar + epsilon) - x) != 0:
            print(f"iteration {iterationCount}: " + str((xStar + epsilon) - x))
            epsilon = float(.5 * epsilon)
            iterationCount += 1

        print("finish")

**Last Modified:** September/2019
