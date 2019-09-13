
**Routine Name:** `absErr`

**Author:** Jaxton Winder

**Language:** Python 3.7.4.

**Description/Purpose:** This routine will return the absolute error between two values, value and valueApprox. The absolute error is the absolute value of the difference between value and valueApprox.

**Input:** There are two inputs required to use this function, value and valueApprox. Value is the value you are testing, and valueApprox is the approximation.

**Output:** This routine returns a double precision float that is the absolute value of the difference between value and valueApprox.

**Usage/Example:**

The routine has two arguments, value and valueApprox. After importing the math4610lib, the routine can be used as follows:

    import math4610lib
    error = math4610lib.absErr(5, 5.5)
    print("error is: " + str(error))

Output from the lines above:

      error is: .5

**Implementation/Code:** The following is the code for `absErr(value, valueApprox)`

    def absErr(value, valueApprox):
        return abs(valueApprox - value)

**Last Modified:** September/2019
