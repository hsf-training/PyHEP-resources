# Python Libraries of Interest to Particle Physics

[![Join the chat at https://gitter.im/HSF/PyHEP](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/HSF/PyHEP?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Python libraries of interest to particle physicists.  This is meant to be a living document.  Therefore, if you have suggestions, click the edit button then make a pull request with your proposed change.

## New to Python

If you are new to Python, the following contains general information on using Python in Science.  

| Name         | Use             | 
| ------------ | --------------- |
| [Software Carpentry Python Lesson ](http://swcarpentry.github.io/python-novice-inflammation/) | Lesson aimed at people who have never used Python before.  |
| [Scipy tutorials](https://scipy2017.scipy.org/ehome/220975/493423/) | You'll want the beginner courses, the intermediate/advanced courses are actually quite advanced. Setup instructions are linked on the page, videos are [here](https://www.youtube.com/playlist?list=PLYx7XA2nY5GfdAFycPLBdUDOUtdQIVoMf) |
| [Dive into Python 3](http://www.diveintopython3.net/index.html) | Very useful for learning python, though it's a bit old and doesn't cover any of the scientific python stuff you really need. | 
| [Code academy](https://www.codecademy.com/learn/python) | |
| Many EdX and Coursera courses | Often introductory CS courses which can teach other useful skills (algorithms and datastructures) |
| (The python docs)[https://docs.python.org/3/] | |

Otherwise, just google python + description of problem, usually answer is on stackoverflow.

Youtube channels with talks / tutorials:

Pycon, e.g.:
  * https://www.youtube.com/channel/UCrJhliKNQ8g0qoE_zvL8eVg (2017)
  * https://www.youtube.com/channel/UCwTD5zJbsQGJN75MwbykYNw (2016)
  * https://www.youtube.com/channel/UCgxzjK6GuOHVKR_08TT4hJQ (2015)

Some more advanced talks of interested:
  * Ned Batchelder, "Facts and Myths about Python names and values" https://www.youtube.com/watch?v=_AEJHKGk9ns
  * David Baumgold, "Advanced Git" https://www.youtube.com/watch?v=4EOZvow1mk4
  * David Beazley, "Discovering python" https://www.youtube.com/watch?v=RZ4Sn-Y7AP8.
  * Thomas Ballinger, "Finding closure with closures" https://www.youtube.com/watch?v=E9wS6LdXM8Y

## Getting Python

| Name         | Use             | 
| ------------ | --------------- |
| [Anaconda Package Manager](https://conda.io/docs/user-guide/getting-started.html) | Anaconda packages most scientific Python libraries while also living purely in user space.  Therefore, you don't need special permissions to setup. |
| [pipenv](https://pipenv.readthedocs.io/en/latest/) | Official Python way |
| [ripa](https://github.com/tunnell/ripa) | ripa solves the packaging issue by letting you install packages (or requirements.txt) where priority given to conda channels, otherwise fetches from PyPI. (Works but rough) |


## Scientific Python Stack

The packages that are used in Physics and/or data science within Python grew somewhat organically before forming the current ecosystem.  Detailed information on what exists can be found [here](https://scipy.org/about.html), but we will summarize here.

| Name         | Use             | 
| ------------ | --------------- |
| [jupyter notebook](https://jupyter.org) | Main one way of doing interactive and/or exploratory analysis. |
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
| PyTorch / keras | Higher level neural network interfaces |

General information through talks tthat maybe  useful on PyData (various conferences each year):
  * https://www.youtube.com/user/PyDataTV and other per-conference channels
  * Scipy conferences, e.g. https://www.youtube.com/playlist?list=PLYx7XA2nY5Gf37zYZMw6OqGFRPjB1jCy6
  * Enthought: https://www.youtube.com/user/EnthoughtMedia
  * Continuum Analytics: https://www.youtube.com/channel/UCND4vKhJssAtK8p1Blfj14Q

## Tutorials

*Who has good tutorials to add?*

## ROOT

For many particle physics experiments, a lot of data is stored within ROOT files.  This means at very least one must have the ability to read ROOT files.  ROOT also serves as a tool suite designed to solve many computational problems encountered in HEP, which means that one may want to access some of this tool suite.  The following packages below are worth knowing for these situations:

| Package name | Use | Pro | Con | Further information |
| ------------ | --- | --- | --- | ------------------- |
| [uproot](https://github.com/scikit-hep/uproot) | Native Python ROOT I/O | Easy to install, fast, no dependencies | Purely for reading ROOT files to exit ROOT ecosystem | | 
| root_numpy, root_pandas | ROOT to/from Numpy and Pandas, like uproot | full ROOT functionality, like TFormula | slower than uproot, binary incompatibilities with different versions of ROOT | |
| [ROOT conda](https://nlesc.gitbooks.io/cern-root-conda-recipes/content/installing_root_via_anaconda.html) | Using ROOT within Anaconda | Easy to get ROOT installed with PyROOT support | Not all features of ROOT and getting dated (6.04 Py2.7/3.4 since XENON1T uses that) | [Recipes](https://github.com/NLeSC/root-conda-recipes) | 
| [PyROOT](https://root.cern.ch/pyroot) | Official ROOT Python bindings | Good support and many examples | Raw C++ wrapping results in weird Python code |  | 
| [rootpy](http://www.rootpy.org) | Pythonic ROOT access | More logical for people who know Python | Smaller user base than PyROOT, abandoned? | [Repository](https://github.com/rootpy/rootpy/) | 
| [alphatwirl](https://github.com/alphatwirl/alphatwirl) | Summerizing ROOT data into categorical data as Pandas' data frames | Small output size. Easy one-function interface with [qtwirl](https://github.com/alphatwirl/qtwirl) | Not for data type conversion | [Repository](https://github.com/alphatwirl/alphatwirl) | 


## Speeding up code

Often, it is not needed anymore to write C++/C routines that get wrapped since there are other ways to speed up your Python code.  Namely:

| Name         | Use             | 
| ------------ | --------------- |
| [numba](https://numba.pydata.org) | Tight loops are often the slow part of Python code, where this compiles them! |
| Pythran | whole scripts |
| [numpy](http://www.numpy.org) | Expressing your code as array options means you get native-C speeds. | 
| NumExpr | single pass "mapper" operations (one input → one output |

## Binding C/C++ to Python

*Before you read this, realize that this is for existing C++ code.  If you want to write new C/C++ code for speed, see section above.*

Python entered into the particle physics ecosystem since it was useful as a 'glue lanaguage'.  This means that you can get multiple softwares in different languages to work with one another.  Given the large ecosystem of Python packages in the last decade, this is less common now.  However, the situation still does arise that you want to call some existing C/C++ code from Python.

Please be aware that wrapping C code is signficantly easier than wrapping C++ code due to details of how function names get garbled in libraries within C++.

At present, the best summary of how to bind code in HEP applications comes from Henry Schreiner in a [2018 PyHEP talk](https://indico.cern.ch/event/694818/contributions/2985778/attachments/1682465/2703470/PyHEPTalk.pdf)

(TODO: improve table.  Most non-pybind11 have given me hundreds of hours of pain so I can't comment objectively)

| Package name  | Use | Pro | Con | Further information |
| ------------- | --- | --- | --- | ------------------- |
| pybind11  | Wrapping existing C++ codes  | Small elegant package | Young but quickly widely used. | Henry's slides |
| Cython  | Wrapping C++ code  | Widely used, freely mixing Python and C++. | Weird syntax, incomplete coverage of C++ | |
| swig | Wrapping C++ code  | Widely used. | Have to write wrapper file and feels dated. | |
| Boost | Wrapping C++ code | Widely used.  | Giant dependency since Boost does many other things.| |

## Experimental codes

Stealing code from other physicists is its own sign of flattery.  Codes that are abandoned more than two years will get struck through.:

|  Name | Collaboration | Use | Further information | Date added to list |
| ----- | ---------- | --- | ------------------- | --------------------- |

