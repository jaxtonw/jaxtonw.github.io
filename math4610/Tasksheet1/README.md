**[Tasksheet 1 Repository](https://github.com/jaxtonw/math4610/tree/master/Tasksheet1)**

+ **Task 1:**
  - If you're Dr. Koebbe, you'll know the results of these tasks. I have emailed you regarding this task.
+ **Task 2:**
  - If you're Dr. Koebbe, you'll know the results of these tasks. I have emailed you regarding this task.
+ **Task 3:**
  - If you're Dr. Koebbe, you'll know the results of these tasks. I have emailed you regarding this task.
+ **Task 4:**
  - Checkout [my HelloWorld.py](https://github.com/jaxtonw/math4610/tree/master/Tasksheet1/Task4) program in my Math 4610 repo.
+ **Task 5:**
  - If you're Dr. Koebbe, you'll know the results of this task.
+ **Task 6:**
  - Checkout [Difference Quotient](https://github.com/jaxtonw/math4610/tree/master/Tasksheet1/DifferenceQuotient) in my Math 4610 Repo.
+ **Task 7:**
  - Checkout [Error Approx](https://github.com/jaxtonw/math4610/tree/master/Tasksheet1/Errors) in my Math 4610 Repo. I also included a routine that returns the percent representation of a relative error.
+ **Task 8:**
  - [Here is a link to the software manual table of contents](../softwareManual/README.md). Alternatively, you can directly navigate to the 4 subroutines below.

  - [maceps32bit](../softwareManual/maceps32bit.md) -- [Source Code](https://github.com/jaxtonw/math4610/blob/master/math4610lib/jaxtonwMLIB/tasksheet1/maceps32bit.py)

  import numpy as np
  def maceps32bit():
      x, xStar = np.float32(1), np.float32(1)
      epsilon = np.float32(1)
      iterationCount = 0

      while abs((xStar + epsilon) - x) != 0:
          print(f"iteration {iterationCount}: " + str((xStar + epsilon) - x))
          epsilon = np.float32(epsilon * .5)
          iterationCount += 1

      print("finish")

  - [maceps64bit](../softwareManual/maceps64bit.md) -- [Source Code](https://github.com/jaxtonw/math4610/blob/master/math4610lib/jaxtonwMLIB//tasksheet1/maceps64bit.py)

  def maceps64bit():
      x, xStar = float(1), float(1)
      epsilon = float(1)
      iterationCount = 0

      while abs((xStar + epsilon) - x) != 0:
          print(f"iteration {iterationCount}: " + str((xStar + epsilon) - x))
          epsilon = float(.5 * epsilon)
          iterationCount += 1

      print("finish")

  - [absErr](../softwareManual/absErr.md) -- [Source Code](https://github.com/jaxtonw/math4610/blob/master/math4610lib/jaxtonwMLIB/tasksheet1/absoluteError.py)

  def absErr(value, valueApprox):
      return abs(valueApprox - value)

  - [relErr](../softwareManual/relErr.md) -- [Source Code](https://github.com/jaxtonw/math4610/blob/master/math4610lib/jaxtonwMLIB//tasksheet1/relativeError.py)

  def relErr(value, valueApprox, percent=False):
      if value == 0: return
      if percent:
          return abs((value - valueApprox) / value) * 100
      return abs((value - valueApprox) / value)

+ **Task 9:**
  - To run the program that computes the derivative of e^x about \pi you need to ensure that the math4610lib is installed to your distribution of python. Click [this link](../softwareManual/installation.md) to see installation and update instructions of Jaxton Winder's math4610lib library.
  - After the library is installed, checkout [my DifferenceQuotientAboutPi.py](https://github.com/jaxtonw/math4610/blob/master/Tasksheet1/DifferenceQuotient/DifferenceQuotientAboutPi.py) program for the results of Task 9.
+ **Task 10:**
  - Absolute and Relative errors are computationally similar, but produce very different results and are used in different contexts. An absolute error function will produce the absolute value of the difference between two values, x and estimatedX. This is useful when you want to know the actual quantity of your error between x and estimatedX. The relative error will produce the absolute value of the difference between the two values x and estimatedX, divided by the target value x. This produces a value which represents the magnitude of the error in relation to the actual quantity of x.
  - [This wikipedia article was used in understanding relative vs. absolute errors.](https://en.wikipedia.org/wiki/Approximation_error#Formal_Definition)
