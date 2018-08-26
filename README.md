# Python Libraries of Interest to Particle Physics

Python libraries of interest to particle physicists.  This is meant to be a living document.  Therefore, if you have suggestions, click the edit button then make a pull request with your proposed change.

## New to Python

If you are new to Python, the following contains general information on using Python in Science.

| Name         | Use             | 
| ------------ | --------------- |
| [Software Carpentry Python Lesson ](http://swcarpentry.github.io/python-novice-inflammation/) | Lesson aimed at people who have never used Python before.  |

## Getting Python

| Name         | Use             | 
| ------------ | --------------- |
| [Anaconda Package Manager](https://conda.io/docs/user-guide/getting-started.html) | Anaconda packages most scientific Python libraries while also living purely in user space.  Therefore, you don't need special permissions to setup. |


## Scientific Python Stack

The packages that are used in Physics and/or data science within Python grew somewhat organically before forming the current ecosystem.  Detailed information on what exists can be found [here](https://scipy.org/about.html), but we will summarize here.

| Name         | Use             | 
| ------------ | --------------- |
| [numpy](http://www.numpy.org) | Array and matrix operations (including math operations) at C speeds. | 
| [pandas](https://pandas.pydata.org) | A very elegant way to work with tabular data (i.e. ntuples) with in memory calculations.  Especially good at time series. |
| [scipy](https://www.scipy.org) | Various scientific routines like minimization. |
| [matplotlib](https://matplotlib.org) | Main Python plotting library.  Start from [matplotlib gallery](https://matplotlib.org/gallery.html) then adapt to your application. |
| [scikit-learn](http://scikit-learn.org/stable/index.html) | Very easy to use machine learning routines with great examples. |

Notable mentions:

| Name         | Use             | 
| ------------ | --------------- |
| [seaborn](https://seaborn.pydata.org) | Easier to use plotting library with some statistical routines, builds on matplotlib, but annoying to customize. |
| [tensorflow](http://scikit-learn.org/stable/index.html) | For deep neural networks. |

## Tutorials

*Who has good tutorials to add?*

## ROOT

For many particle physics experiments, a lot of data is stored within ROOT files.  This means at very least one must have the ability to read ROOT files.  ROOT also serves as a tool suite designed to solve many computational problems encountered in HEP, which means that one may want to access some of this tool suite.  The following packages below are worth knowing for these situations:

| Package name | Use | Pro | Con | Further information |
| ------------ | --- | --- | --- | ------------------- |
| [uproot](https://github.com/scikit-hep/uproot) | Native Python ROOT I/O | Easy to install, fast, no dependencies | Purely for reading ROOT files to exit ROOT ecosystem | | 
| [ROOT conda](https://nlesc.gitbooks.io/cern-root-conda-recipes/content/installing_root_via_anaconda.html) | Using ROOT within Anaconda | Easy to get ROOT installed with PyROOT support | Not all features of ROOT | [Recipes](https://github.com/NLeSC/root-conda-recipes) | 
| [PyROOT](https://root.cern.ch/pyroot) | Official ROOT Python bindings | Good support and many examples | Raw C++ wrapping results in weird Python code |  | 
| [rootpy](http://www.rootpy.org) | Pythonic ROOT access | More logical for people who know Python | Smaller user based than PyROOT | [Repository](https://github.com/rootpy/rootpy/) | 


## Speeding up code

Often, it is not needed anymore to write C++/C routines that get wrapped since there are other ways to speed up your Python code.  Namely:

| Name         | Use             | 
| ------------ | --------------- |
| [numba](https://numba.pydata.org) | Tight loops are often the slow part of Python code, where this compiles them! |
| [numpy](http://www.numpy.org) | Expressing your code as array options means you get native-C speeds. | 

## Binding C/C++ to Python

*Before you read this, realize that this is for existing C++ code.  If you want to write new C/C++ code for speed, see section above.*

Python entered into the particle physics ecosystem since it was useful as a 'glue lanaguage'.  This means that you can get multiple softwares in different languages to work with one another.  Given the large ecosystem of Python packages in the last decade, this is less common now.  However, the situation still does arise that you want to call some existing C/C++ code from Python.

Please be aware that wrapping C code is signficantly easier than wrapping C++ code due to details of how function names get garbled in libraries within C++.

At present, the best summary of how to bind code in HEP applications comes from Henry Schreiner in a [2018 PyHEP talk](https://indico.cern.ch/event/694818/contributions/2985778/attachments/1682465/2703470/PyHEPTalk.pdf)

| Package name  | Use | Pro | Con | Further information |
| ------------- | --- | --- | --- | ------------------- |
| pybind11  | Wrapping existing C++ codes  | Small elegant package | Have to code up binding | Henry's slides |
| Cython  | ...  | | | |
| swig | ...  | | | |
| Boost | ... | | | |
