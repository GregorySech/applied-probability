# Applied Probability for Computer Science Notes
These are my notes from the Master's Degree Programme course Applied Probability for Computer Science by [Prof. Antoniano Villalobos](https://www.unive.it/data/persone/20055797).

# Disclaimer
As these are my personal notes I might have misunderstood or came up to wrong 
conclusions during the lessons. For these mistakes I apologize in advance and 
incourage anyone in submitting either a GitHub issue on this repository so that 
I will fix the mistake as soon as possible or directly submit a pull request.

The course content is a selection from the textbook [Probability and Statistics for Computer Scientists](https://books.google.it/books/about/Probability_and_Statistics_for_Computer.html?id=fkDADwAAQBAJ&redir_esc=y) of
which I'm not the author.

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

## [IRKernel](https://github.com/IRkernel/IRkernel)
This is a native R kernel for Jupyter. It is part of the `r-essentials` package in Anaconda.

### Setting up R with Anaconda
```bash
conda install -c r-essentials r-base
```

[anaconda-individual]: https://www.anaconda.com/products/individual