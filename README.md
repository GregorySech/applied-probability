# Master Degree Notes
These are my notes from the Master's Degree Programme course that I was able to attend.

# Technologies

## [Anaconda][anaconda-individual]
Personally I install most of my Python packages with [Anaconda][anaconda-individual] which I also use to manage development environments.

## [Jupyter Notebooks](https://jupyter.org/)
Jupyter is an open source platform to create interactive software, usually in the form of notebooks, in a wide variety of programming languages.

### Installing Jupyter
```bash
conda install -c conda-forge jupyter
```

## [JupyterBook](https://jupyterbook.org/)
This is a neat conversion and pagination tool for Jupyter and Markdown books (and notes).

### Installing JupyterBook
At the time of writing JupyterBook is not installable through Anaconda but only through [PyPI](https://pypi.org/).

```bash 
pip install jupyter-book
```

### Building a course's notes
```bash 
jupyter-book build <course folder path> --builder pdflatex
```

### Cleaning the build outputs
```bash
jupyter-book clean <course folder path>
```

## [xeus-cling](https://github.com/jupyter-xeus/xeus-cling)
This is a Jupyter kernel to create notebooks with C++ based on the `cling` interpreter.

### Installation

```bash
conda install xeus-cling -c conda-forge
```

## [IRKernel](https://github.com/IRkernel/IRkernel)
This is a native R kernel for Jupyter. It is part of the `r-essentials` package in Anaconda.

### Setting up R with Anaconda
```bash
conda install -c r-essentials r-base
```

[anaconda-individual]: https://www.anaconda.com/products/individual