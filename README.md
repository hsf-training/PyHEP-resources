# pyhep_python_libraries
Python libraries of interest to particle physicists.

Domain-specific 

[[toc]]

## New to Python

If you are new to Python, the following contains general information on using Python in Science.

## Getting Python

## Scientific Python Stack

## Tutorials


## Binding C/C++ to Python

Python entered into the particle physics ecosystem since it was useful as a 'glue lanaguage'.  This means that you can get multiple softwares in different languages to work with one another.  Given the large ecosystem of Python packages in the last decade, this is less common now.  However, the situation still does arise that you want to call some existing C/C++ code from Python.

Please be aware that wrapping C code is signficantly easier than wrapping C++ code due to details of how function names get garbled in libraries within C++.

| Package name  | Use | Caveats |Further information |
| ------------- | ------------- |
| pybind11  | Wrapping existing C++ codes  | Small elegant package | Learning curve | Henry's slides |
| Cython  | ...  | | |
| swig | 
