# How to convert Python code into Binary format (.so)
This tutorial will guide you on how to create a binary file from Python code

## Step 0:
Save a copy of all .py code as .pyx with first line being 

```
STUFF = 'Hi'  ## This hack is required for importing .so object in target code
```

## Step 1: 
Go to the Folder where all the Python code resides and create a file called "setup" which contains below lines

./setup File should contain
```
from distutils.core import setup
from Cython.Build import cythonize

setup(
    ext_modules=cythonize("*.pyx"),
     )
```

## Step 2:
Run the below command to generate .pyx and .so files 

```
python setup build_ext --inplace
```

e.g it will create Utilities.so 

## Step 3:
Now copy .so files to any folder where you want to use it. Below is the usage information from user's code. 

```
import Utilities
```


Reference:
http://cython.readthedocs.io/en/latest/src/tutorial/cython_tutorial.html
