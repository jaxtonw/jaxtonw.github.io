
**Routine Name:** `relErr`

**Author:** Jaxton Winder

**Language:** Python 3.7.4.

**Description/Purpose:** This routine will return the relative error between two values, value and valueApprox. The relative error is the absolute value of the difference between value and valueApprox, divided by value.

**Input:** There are two inputs required to use this function, value and valueApprox. Value is the value you are testing, and valueApprox is the approximation. It has an optional boolean input for percent. By default, percent is set as false. When percent is set to be true, the value returned will be represented as a percent error.

**Output:** This routine returns a double precision float that is the absolute value of the difference between value and valueApprox, divided by value.

**Usage/Example:**

The routine has two arguments, value and valueApprox.  It has an optional boolean input for percent. By default, percent is set as false. When percent is set to be true, the value returned will be represented as a percent error. After importing the math4610lib, the routine can be used as follows:

    import math4610lib
    error = math4610lib.relErr(5, 5.5)
    print("error is: " + str(error))

Output from the lines above:

      error is: .1

Use the percent argument as follows:

    import math4610lib
    error = math4610lib.relErr(5, 5.5, percent=True)
    print("error is: " + str(error))

Ouput from the lines above:

    error is: 10

**Implementation/Code:** The following is the code for `relErr(value, valueApprox, percent=False)`

    def relErr(value, valueApprox, percent=False):
        if value == 0: return
        if percent:
            return abs((value - valueApprox) / value) * 100
        return abs((value - valueApprox) / value)


**Last Modified:** September/2019
