# Python Libraries of Interest to Particle Physics

[![Join the chat at https://gitter.im/HSF/PyHEP](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/HSF/PyHEP?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1420444.svg)](https://doi.org/10.5281/zenodo.1420444)

Python libraries of interest to particle physicists.  This is meant to be a living document.  Therefore, if you have suggestions, click the edit button then make a pull request with your proposed change(s).

You are more than welcome to join the [HSF/PyHEP Gitter channel](https://gitter.im/HSF/PyHEP) and contribute to the informal discussions there.

## New to Python

If you are new to Python, the following contains general information on using Python in Science.  

| Name         | Use             |
| ------------ | --------------- |
| [Software Carpentry Python Lesson][] | Lesson aimed at people who have never used Python before.  |
| [Scipy tutorials][] | You'll want the beginner courses, the intermediate/advanced courses are actually quite advanced. Setup instructions are linked on the page, videos are [here][Scipy tutorial videos] |
| [Dive into Python 3][] | Very useful for learning python, though it's a bit old and doesn't cover any of the scientific python stuff you really need. |
| [Code academy][] | |
| Many EdX and Coursera courses | Often introductory CS courses which can teach other useful skills (algorithms and datastructures) |
| [The python docs][] | |

[Software Carpentry Python Lesson]: http://swcarpentry.github.io/python-novice-inflammation/
[Scipy tutorials]:                  https://scipy2017.scipy.org/ehome/220975/493423/
[Scipy tutorial videos]:            https://www.youtube.com/playlist?list=PLYx7XA2nY5GfdAFycPLBdUDOUtdQIVoMf
[Dive into Python 3]:               http://www.diveintopython3.net/index.html
[Code academy]:                     https://www.codecademy.com/learn/python
[The python docs]:                  https://docs.python.org/3/

Otherwise, just google python + description of problem, usually answer is on stackoverflow.

Youtube channels with talks / tutorials:

Pycon, e.g.:
  * <https://www.youtube.com/channel/UCrJhliKNQ8g0qoE_zvL8eVg> (2017)
  * <https://www.youtube.com/channel/UCwTD5zJbsQGJN75MwbykYNw> (2016)
  * <https://www.youtube.com/channel/UCgxzjK6GuOHVKR_08TT4hJQ> (2015)

Some more advanced talks of interested:
  * [Ned Batchelder, "Facts and Myths about Python names and values"](https://www.youtube.com/watch?v=_AEJHKGk9ns)
  * [David Baumgold, "Advanced Git"](https://www.youtube.com/watch?v=4EOZvow1mk4)
  * [David Beazley, "Discovering python"](https://www.youtube.com/watch?v=RZ4Sn-Y7AP8)
  * [Thomas Ballinger, "Finding closure with closures"](https://www.youtube.com/watch?v=E9wS6LdXM8Y)


## Getting Python

| Name         | Use             |
| ------------ | --------------- |
| [Conda][] | Anaconda packages most scientific Python libraries while also living purely in user space.  Therefore, you don't need special permissions to setup. Anaconda is a metapackage of 100 or so scientific Python packages for Conda. |
| [pipenv][] | Very slick all-in-one combination of virtual environments and package installation, can manage Python installs too. |
| [ripa][] | ripa solves the packaging issue by letting you install packages (or requirements.txt) where priority given to conda channels, otherwise fetches from PyPI. (Works but rough) |

[Conda]:  https://conda.io/docs/user-guide/getting-started.html
[pipenv]: https://pipenv.readthedocs.io/en/latest/
[ripa]:   https://github.com/tunnell/ripa

## Scientific Python Stack

The packages that are used in Physics and/or data science within Python grew somewhat organically before forming the current ecosystem.  Detailed information on what exists can be found [here](https://scipy.org/about.html), but we will summarize here.

| Name         | Use             |
| ------------ | --------------- |
| [jupyter notebook][] | Main one way of doing interactive and/or exploratory analysis. |
| [numpy][] | Array and matrix operations (including math operations) at C speeds. |
| [pandas][] | A very elegant way to work with tabular data (i.e. ntuples) with in memory calculations.  Especially good at time series. |
| [xarray][] | Extension of pandas to N-Dim structures. |
| [h5py][] | Simple numpy to HDF5 bindings (backend for Keras saved models). |
| [scipy][] | Various scientific routines like minimization. |
| [matplotlib][] | Main Python plotting library.  Start from [matplotlib gallery][] then adapt to your application. |
| [scikit-learn][] | Very easy to use machine learning routines with great examples. |

[jupyter notebook]:   https://jupyter.org
[numpy]:              http://www.numpy.org
[pandas]:             https://pandas.pydata.org
[xarray]:             http://xarray.pydata.org/en/stable/why-xarray.html#core-data-structures
[h5py]:               http://www.h5py.org/
[scipy]:              https://www.scipy.org
[matplotlib]:         https://matplotlib.org
[matplotlib gallery]: https://matplotlib.org/gallery.html
[scikit-learn]:       http://scikit-learn.org/stable/index.html) 


Visualisation:

| Name         | Use             |
| ------------ | --------------- |
| [matplotlib][] | Main Python plotting library.  Start from [matplotlib gallery][] then adapt to your application. |
| [seaborn][] | Easier to use plotting library with some statistical routines. Builds on matplotlib, but annoying to customize. |
| [vegascope][] | View Vega/Vega-Lite plots in your web browser from local or remote Python processes. |

[seaborn]: https://seaborn.pydata.org
[vegascope]: https://github.com/scikit-hep/vegascope

Machine learning:

| Name         | Use             |
| ------------ | --------------- |
| [scikit-learn][] | Popular package. |
| [tensorflow][] | By Google, for deep neural networks and more. |
| [pytorch][] | Deep learning framework for fast, flexible experimentation with dynamic computational graphs. |
| [keras][] | Higher level neural network interfaces. |

[scikit-learn]: http://scikit-learn.org/stable/index.html
[tensorflow]: http://tensorflow.org
[pytorch]: https://pytorch.org
[keras]: https://keras.io

General information through talks that may be useful on PyData (various conferences each year):
  * <https://www.youtube.com/user/PyDataTV> and other per-conference channels
  * [Scipy conferences](https://www.youtube.com/playlist?list=PLYx7XA2nY5Gf37zYZMw6OqGFRPjB1jCy6)
  * [Enthought](https://www.youtube.com/user/EnthoughtMedia)
  * [Continuum Analytics](https://www.youtube.com/channel/UCND4vKhJssAtK8p1Blfj14Q)




## Particle Physics packages
| Name         | Use             |
| ------------ | --------------- |
| [numpythia][] | Interface between FastJet and NumPy. |
| [pyjet][] | Interface between PYTHIA and NumPy. |

[numpythia]: https://github.com/scikit-hep/numpythia
[pyjet]:     https://github.com/scikit-hep/pyjet

## Tutorials

See tutorials here and other resources collected by [IML HEP-ML Resources](https://github.com/iml-wg/HEP-ML-Resources#tutorials).


## ROOT and interoperability with ROOT

For many particle physics experiments, a lot of data is stored within ROOT files.  This means at very least one must have the ability to read ROOT files.  ROOT also serves as a tool suite designed to solve many computational problems encountered in HEP, which means that one may want to access some of this tool suite.  The following packages below are worth knowing for these situations:

| Package name | Use | Pro | Con | Further information |
| ------------ | --- | --- | --- | ------------------- |
| [ostap](https://github.com/OstapHEP/ostap) | User-friendly &amp; more intuitive interface to(Py)ROOT | Many decorations to ROOT classes | Requires C++ code compilation |  |
| [uproot](https://github.com/scikit-hep/uproot) | Native Python ROOT I/O | Easy to install, fast, no dependence on C++ ROOT | Although it can read all ROOT files, can only write ROOT files with specific objects. | |
| [root_numpy][], [root_pandas][] | ROOT to/from Numpy and Pandas, like uproot | full ROOT functionality, like TFormula | slower than uproot, binary incompatibilities with different versions of ROOT, partially superceded by `AsMatrix` in ROOT 6.14+ | |
| [Conda-Forge ROOT](https://github.com/conda-forge/root-feedstock) | Using ROOT within Anaconda | Full-featured ROOT and PyROOT 6.16 on Linux | Not available on macOS yet |  |
| [NLeSC: ROOT on conda][] | Using ROOT within Anaconda | Easy to get ROOT installed with PyROOT support | Not all features of ROOT and getting dated (6.04 Py2.7/3.4 since XENON1T uses that) | [Recipes](https://github.com/NLeSC/root-conda-recipes) |
| [PyROOT](https://root.cern.ch/pyroot) | Official ROOT Python bindings | Good support and many examples | Raw C++ wrapping results in weird Python code |  |
| [rootpy](http://www.rootpy.org) | Pythonic ROOT access | More logical for people who know Python | Smaller user base than PyROOT, abandoned? | [Repository](https://github.com/rootpy/rootpy/) |
| [alphatwirl](https://github.com/alphatwirl/alphatwirl) | Summerizing ROOT data into categorical data as Pandas' data frames | Small output size. Easy one-function interface with [qtwirl](https://github.com/alphatwirl/qtwirl) | Not for data type conversion | |
| [pyhf](https://github.com/diana-hep/pyhf) | statistical analysis / fitting | pure python implementation of HistFactory specification with auto-diff enabled backends in tensorflow, pytorch, and MXNet | not yet interoperable with ROOT-based RooFit models | |


[root_numpy]: http://scikit-hep.org/root_numpy/
[root_pandas]: https://github.com/scikit-hep/root_pandas
[NLeSC: ROOT on conda]: https://nlesc.gitbooks.io/cern-root-conda-recipes/content/installing_root_via_anaconda.html

## Jupyter extensions

Jupyter has a wide ecosystem of extensions that can be used to extend the functionality. Some useful extensions for HEP data analysis are summarised here.

| Name         | Use             |
| ------------ | --------------- |
| [nbdime][]   | Simplifies diffing and merging of jupyter notebooks that are stored in version control. |
| [jupytext][] | Splits notebooks into a `.ipynb` and `.py` file for easier version control and to allow them to be run as scripts idependently of jupyter. |

[nbdime]:   https://github.com/jupyter/nbdime
[jupytext]: https://github.com/mwouts/jupytext

## Speeding up code

Often, it is not needed anymore to write C++/C routines that get wrapped since there are other ways to speed up your Python code.  Namely:

| Name         | Use             |
| ------------ | --------------- |
| [numba][] | Tight loops are often the slow part of Python code, where this JIT compiles them! |
| [Pythran][] | Whole scripts |
| [numpy][] | Expressing your code as array options means you get native-C speeds per sub-expression. |
| [NumExpr][] | Single pass "mapper" operations (one input &rarr; one output). |

[numba]:   https://numba.pydata.org
[Pythran]: https://pythran.readthedocs.io/en/latest/
[numpy]:   http://www.numpy.org
[NumExpr]: https://numexpr.readthedocs.io/en/latest/user_guide.html

## Binding C/C++ to Python

*Before you read this, realize that this is for existing C++ code.  If you want to write new C/C++ code for speed, see section above.*

Python entered into the particle physics ecosystem since it was useful as a 'glue lanaguage'.  This means that you can get multiple softwares in different languages to work with one another.  Given the large ecosystem of Python packages in the last decade, this is less common now.  However, the situation still does arise that you want to call some existing C/C++ code from Python.

Please be aware that wrapping C code is signficantly easier than wrapping C++ code due to details of how function names get garbled in libraries within C++; but the tools below can make wrapping C++ easy as well.

At present, the best summary of how to bind code in HEP applications comes from Henry Schreiner in a [2018 PyHEP talk][Binding Python].

| Package name  | Use | Pro | Con | Further information |
| ------------- | --- | --- | --- | ------------------- |
| [pybind11][]  | Wrapping existing C++ codes  | Small elegant package, simple build. | Young but gaining populatiry quickly. | [Henry's slides][Binding Python] |
| [Cython][]  | Wrapping C++ code  | Widely used, freely mixing Python and C++. | Mix of C and Python is a new language, incomplete coverage of C++. | |
| [SWIG][] | Wrapping C++ code  | Widely used, multiple languages. | Have to write wrapper file, harder to customize, and development is slow/dated. | |
| [Boost::Python][] | Wrapping C++ code | Widely used.  | Giant dependency since Boost does many other things, uses "jam" to build.| |

[pybind11]:       http://pybind11.readthedocs.io
[Binding Python]: https://indico.cern.ch/event/694818/contributions/2985778/attachments/1682465/2703470/PyHEPTalk.pdf
[Cython]:         https://cython.readthedocs.io/en/latest/
[SWIG]:           http://www.swig.org
[Boost::Python]:  https://www.boost.org/doc/libs/1_69_0/libs/python/doc/html/index.html

## Experimental codes

Stealing code from other physicists is its own sign of flattery.  Codes that are abandoned more than two years will get struck through.:

|  Name | Collaboration | Use | Further information | Date added to list |
| ----- | ---------- | --- | ------------------- | --------------------- |
