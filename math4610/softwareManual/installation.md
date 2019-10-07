# Math 4610 Shared Library Installation Guide

After cloning [this repository](https://github.com/jaxtonw/math4610), make sure your current working directory is within the repository. In your current working directory should be the file `math4610lib-0.0.1-py3-none-any.whl`. This is the wheel file that will be used to install the `math4610lib` shared library.

Once the wheel file has been found, run `python -m pip install math4610lib-0.0.1-py3-none-any.whl`. This will then install the wheel file and will then place math4610lib as a shared library for python.

# Updating The Library

When installing an updated version of the math4610 library, run `python -m pip install --upgrade math4610lib-0.0.1-py3-none-any.whl` to directly replace the old version of the math4610lib file.
