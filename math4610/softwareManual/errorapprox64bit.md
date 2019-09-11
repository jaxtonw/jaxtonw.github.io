
**Routine Name:** `errorapprox64bit`

**Author:** Jaxton Winder

**Language:** Python 3.7.4. This routine is dependent on numpy, a mathematical library that comes with many distributions of Python. Use pip installer to run ``pip install numpy`` if numpy is not present in your Python distribution.

    python errorapprox64bit.py

**Description/Purpose:** This routine tests the machine precision of a 64-bit double floating point value. This routine will start epsilon to be a double precision float of 1. It then iterates epsilon to be smaller and smaller to compute the smallest possible value a double precision type can hold and perform meaningful computations with.

**Input:** There are no inputs required.

**Output:** Any call to the function will print to the console each iteration on a new line until it reaches the last iteration with a meaningful calculation.

**Usage/Example:**

The routine has no inputs.

      errorapprox64bit()

Output from the lines above:

      error is: .5

**Implementation/Code:** The following is the code for `AbsoluteError(value, valueApprox)`

    def AbsoluteError(value, valueApprox):
        return abs(valueApprox - value)

**Last Modified:** September/2019
