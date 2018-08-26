# pyhep_python_libraries

Python libraries of interest to particle physicists.  This is meant to be a living document.  Therefore, if you have suggestions, click the edit button then make a pull request with your proposed change.

## New to Python

If you are new to Python, the following contains general information on using Python in Science.

## Getting Python

## Scientific Python Stack

## Tutorials

## ROOT

For many particle physics experiments, a lot of data is stored within ROOT files.  This means at very least one must have the ability to read ROOT files.  ROOT also serves as a tool suite designed to solve many computational problems encountered in HEP, which means that one may want to access some of this tool suite.  The following packages below are worth knowing for these situations:

| Package name | Use | Pro | Con | Further information |
| ------------ | --- | --- | --- | ------------------- |
| [uproot](https://github.com/scikit-hep/uproot) | Native Python ROOT I/O | Easy to install, fast, no dependencies | Purely for reading ROOT files to exit ROOT ecosystem | | 
| [ROOT conda](https://nlesc.gitbooks.io/cern-root-conda-recipes/content/installing_root_via_anaconda.html) | Using ROOT within Anaconda | Easy to get ROOT installed with PyROOT support | Not all features of ROOT | [Recipes](https://github.com/NLeSC/root-conda-recipes) | 
| [PyROOT](https://root.cern.ch/pyroot) | Official ROOT Python bindings | Good support and many examples | Raw C++ wrapping results in weird Python code |  | 
| [rootpy](http://www.rootpy.org) | Pythonic ROOT access | More logical for people who know Python | Smaller user based than PyROOT | [Repository](https://github.com/rootpy/rootpy/) | 



## Binding C/C++ to Python

Python entered into the particle physics ecosystem since it was useful as a 'glue lanaguage'.  This means that you can get multiple softwares in different languages to work with one another.  Given the large ecosystem of Python packages in the last decade, this is less common now.  However, the situation still does arise that you want to call some existing C/C++ code from Python.

Please be aware that wrapping C code is signficantly easier than wrapping C++ code due to details of how function names get garbled in libraries within C++.

At present, the best summary of how to bind code in HEP applications comes from Henry Schreiner in a [2018 PyHEP talk](https://indico.cern.ch/event/694818/contributions/2985778/attachments/1682465/2703470/PyHEPTalk.pdf)

| Package name  | Use | Pro | Con | Further information |
| ------------- | --- | --- | --- | ------------------- |
| pybind11  | Wrapping existing C++ codes  | Small elegant package | Have to code up binding | Henry's slides |
| Cython  | ...  | | | |
| swig | ...  | | | |
| Boost | ... | | | |
