# Introduction to Python for Astronomy

<img src="Images/qarg_bw_dark.png" alt="QUT Astrophysics Research Group" width="500" />

A set of hands-on Python training notebooks for new students joining the QUT Astrophysics Research Group [(QARG)](https://research.qut.edu.au/qutastrophysics/). They're written for Honours, VRES and capstone students who haven't done SEB108, or did it a while ago and need a refresher.

The group works on galaxy evolution and cosmology, so the examples use what you'll meet in your project: redshifts, magnitudes, fluxes, sky coordinates and galaxy catalogues from surveys like ZFOURGE and SDSS. No astrophysics background is assumed.

**Group leads:** Dr Michael Cowley and Dr Rossana Ruggeri  
**Author:** Michael Cowley

## Notebooks

Work through them in order. Each one is self-contained, so you can start any notebook without running the previous ones, and all the code is in the notebook itself.

| Part | Notebook | Topic | Time |
|------|----------|-------|------|
| 1 | [Python Basics](01-Python-Basics.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/01-Python-Basics.ipynb) | Variables, data types, strings, lists, dictionaries, conditions, loops, functions and errors | ~3 h |
| 2 | [NumPy and Astropy](02-NumPy-and-Astropy.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/02-NumPy-and-Astropy.ipynb) | Arrays, masks, missing data, 2D images, units, constants and cosmology | ~2.5 h |
| 3 | [Catalogues and Data](03-Catalogues-and-Data.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/03-Catalogues-and-Data.ipynb) | pandas, missing data and flags, CSV, text and FITS files, merging, FITS images and WCS, astroquery and cross-matching, using real ZFOURGE data | ~3 h |
| 4 | [Plotting for Astronomy](04-Plotting-for-Astronomy.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/04-Plotting-for-Astronomy.ipynb) | Matplotlib figures and axes, log axes, histograms, crowded scatter plots, error bars, multi-panel UVJ diagrams, images with WCS, and making good figures | ~3 h |
| 5 | [Statistics and Fitting](05-Statistics-and-Fitting.ipynb) <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjcowley/Python_Intro/blob/main/05-Statistics-and-Fitting.ipynb) | Robust statistics and photo-z quality, error propagation, weighted means and tension, curve fitting and χ², measuring H₀ and dark energy with Pantheon+ supernovae, KS tests and the bootstrap | ~3 h |
| 6 | Putting It Together *(coming soon)* | Short galaxy evolution examples | ~2 h |

Altogether it's about a day and a half to two days of full-time work.

From Part 3 onwards the notebooks use real survey data, which they download automatically. See the [data README](data/README.md) for where it comes from.

Every notebook pairs worked examples with exercises. Most exercises have a check cell so you can confirm your answer, and every exercise has a hidden solution you can open once you've had a go.

## Running the Notebooks

### Google Colab (recommended to start)

Click an **Open in Colab** button above. Colab runs in your browser with nothing to install, and you just need a Google account.

Before you start, go to *File → Save a copy in Drive*, otherwise your work won't be saved.

### On your own computer

Once your project starts you'll want Python set up locally. We recommend [Miniforge](https://github.com/conda-forge/miniforge), a free, lightweight installer for Python and the `conda` package manager.

1. Install Miniforge by following the instructions on its page.
2. Open a terminal (on Windows, use *Miniforge Prompt* from the Start menu) and create an environment for your work:

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

- Read the error message, then search it. Section 10 of Part 1 covers how.
- Ask others in the group. Everyone has been stuck on the same things.
- Talk to your supervisor, and check the [QARG Canvas site](https://canvas.qut.edu.au/courses/13966) for group resources.

## Next Steps

Once you've finished, have a look at [Astro_Code](https://github.com/mjcowley/Astro_Code) for the group's research notebooks (ZFOURGE, EAZY, UVJ diagrams, SDSS luminosity functions and SED fitting), and [Astro_Demos](https://mjcowley.github.io/astro_demos/) for interactive astrophysics demonstrations.
