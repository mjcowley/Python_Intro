# Introduction to Python for Astronomy

<img src="Images/qarg_bw_dark.png" alt="QUT Astrophysics Research Group" width="500" />

A set of hands-on Python training notebooks for new students joining the QUT Astrophysics Research Group [(QARG)](https://research.qut.edu.au/qutastrophysics/). They're written for research students who are either new to or need a refresher in Python. The group works on galaxy evolution and cosmology, so the examples use what you'll meet in your project (e.g., redshifts, magnitudes, fluxes, sky coordinates and galaxy catalogues from surveys like ZFOURGE and SDSS).

## New to Python? Start Here

Before you open Part 1, read the **[Getting Started guide](GETTING_STARTED.md)** (also available as a [printable PDF](Getting-Started.pdf)). It takes about 15 minutes and covers:

- What notebooks, cells, and the other terms you'll come across actually mean
- Opening your first notebook in Google Colab and saving your work
- Running cells, useful shortcuts, and tips to overcome confusion
- How to get complete exercises and check your answers
- What to do when something goes wrong, and how to ask for help
- Step-by-step setup of Python on your own computer
- A one-page Python cheat sheet

## Notebooks

Each notebook is self-contained, so you can start any without running the previous ones. That said, it's recommended you complete in the order provided below. 

| Part | Notebook | Topic | Time |
|------|----------|-------|------|
| 1 | [Python Basics](01-Python-Basics.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/01-Python-Basics.ipynb) | Variables, data types, strings, lists, dictionaries, conditions, loops, functions and errors | ~3 h |
| 2 | [NumPy and Astropy](02-NumPy-and-Astropy.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/02-NumPy-and-Astropy.ipynb) | Arrays, masks, missing data, 2D images, units, constants and cosmology | ~3 h |
| 3 | [Catalogues and Data](03-Catalogues-and-Data.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/03-Catalogues-and-Data.ipynb) | pandas, missing data and flags, CSV, text and FITS files, merging, FITS images and WCS, astroquery and cross-matching, using real ZFOURGE data | ~3 h |
| 4 | [Plotting for Astronomy](04-Plotting-for-Astronomy.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/04-Plotting-for-Astronomy.ipynb) | Matplotlib figures and axes, log axes, histograms, crowded scatter plots, error bars, multi-panel UVJ diagrams, images with WCS, and making good figures | ~3 h |
| 5 | [Statistics and Fitting](05-Statistics-and-Fitting.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/05-Statistics-and-Fitting.ipynb) | Robust statistics and photo-z quality, error propagation, weighted means and tension, curve fitting and χ², measuring H₀ and dark energy with Pantheon+ supernovae, KS tests and the bootstrap | ~3 h |
| 6 | [Putting It Together](06-Putting-It-Together.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/06-Putting-It-Together.ipynb) | Three short projects (the stellar mass function, large-scale structure in CDFS, and the ages of galaxies) plus tips on working in the group | ~2 h |

From Part 3 onwards the notebooks use real survey data, which they download automatically. See the [data README](data/README.md) for where this comes from. Every notebook pairs worked examples with exercises, which have hidden solutions so you can check your working as you go.

## Running the Notebooks

### Google Colab

If this is all new to you, it's recommended you start here by clicking an "Open in Colab" button above, which runs in your browser with nothing to install (requires a Google account).

Before you start, go to *File → Save a copy in Drive*, otherwise your work won't be saved. That said, it's highly encouraged you soon move to a local environment as below.

### On your own computer

For Honours, MPhil or PhD, you're encouraged to set up Python locally. We recommend [Miniforge](https://github.com/conda-forge/miniforge), a free, lightweight installer for Python and the `conda` package manager.

1. Install Miniforge. Step-by-step instructions for Windows, macOS and Linux are in [Section 7 of the Getting Started guide](GETTING_STARTED.md#7-setting-up-python-on-your-own-computer).
2. On Linux or macOS, open a terminal (on Windows, open *Miniforge Prompt* from the Start menu) and create an environment for your work:

   ```bash
   conda create -n qarg python=3.12
   conda activate qarg
   ```

3. Download this repository, either with *Code → Download ZIP* on GitHub or with git:

   ```bash
   git clone https://github.com/mjcowley/Python_Intro.git
   cd Python_Intro
   ```

4. Install the packages and start JupyterLab:

   ```bash
   pip install -r requirements.txt
   jupyter lab
   ```

Each time you come back, open a terminal and run `conda activate qarg` before `jupyter lab`.

If you'd rather use an editor, [VS Code](https://code.visualstudio.com/) and [VSCodium](https://vscodium.com/) both run notebooks well. Point them at the `qarg` environment when they ask which Python to use.

### Supercomputers (HPC)

Some projects need more computing power than a laptop. The group has access to QUT's eResearch HPC and to Swinburne's [OzSTAR](https://supercomputing.swin.edu.au/) supercomputer. You'll find details on how to get access on the [QARG Canvas site](https://canvas.qut.edu.au/courses/13966). Talk to your supervisor first about whether your project needs it.

## Requirements

- Python 3.10 or later
- `numpy`, `scipy`, `pandas`, `matplotlib`, `astropy` and `astroquery`

Colab has most of these already, and any notebook that needs something extra installs it in its first cell. For local use, everything is listed in [`requirements.txt`](requirements.txt).

## Getting Help

- Read the error message, then ~~Google~~ DuckDuckGo search it. Section 10 of Part 1 covers this in more detail.
- Ask others in the group. Everyone else has likely been stuck on the same things!
- Talk to your supervisor, and check the [QARG Canvas site](https://canvas.qut.edu.au/courses/13966) for group resources.
