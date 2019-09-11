
**Routine Name:** `AbsoluteError`

**Author:** Jaxton Winder

**Language:** Python 3.7.4. This routine is dependent on numpy, a mathematical library that comes with many distributions of Python. Use pip installer to run ``pip install numpy`` if numpy is not present in your Python distribution.

    python absoluteError.py

**Description/Purpose:** This routine will return the absolute error between two values, x and estimatedX. The absolute error is the absolute value of the difference between x and estimatedX.

**Input:** There are two inputs required to use this function, value and valueApprox. Value is the value you are testing, and valueApprox is the approximation.

**Output:** This routine returns a double precision float that is the absolute value of the difference between value and valueApprox.

**Usage/Example:**

The routine has two arguments needed to return the values of the precision in terms of the smallest number that can be
represented. Since the code is written in terms of a Fortran subroutine, the values of the machine machine epsilon and
the power of two that gives the machine epsilon. Due to implicit Fortran typing, the first argument is a single precision
value and the second is an integer.

      error = AbsoluteError(5, 5.5)
      print("error is: " + str(error))

Output from the lines above:

      error is: .5

**Implementation/Code:** The following is the code for `AbsoluteError(value, valueApprox)`

    def AbsoluteError(value, valueApprox):
        return abs(valueApprox - value)

**Last Modified:** September/2019
