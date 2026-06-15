# Introduction to Python

<img src="../Images/qarg_bw_dark.png" alt="QUT Logo" width="500" />

A self-contained introductory Python workbook for physics students with no prior programming experience. Covers data types, data acquisition and cleaning, descriptive and inferential statistics, and data visualisation across four guided practicals.

## Key Features

- **No installation required**: Designed to run in Google Colab out of the box; local environments also supported
- **Worked examples and exercises**: Each section pairs demonstration code with hands-on exercises using real datasets
- **Real datasets**: Uses Queensland air quality monitoring data and global temperature anomaly records throughout
- **Progressive structure**: Each part builds on the previous; completable in a day or two

## Contents

- `Python-Intro.ipynb` - Main workbook (four parts)

## Data Files

The following files must be in the same directory as the notebook:

| File | Description |
|------|-------------|
| `quantum_mechanics.grades` | Exam score dataset used in Parts 1 and 2 |
| `carbonmonoxide-qld-2022.csv` | Hourly CO measurements across Queensland (2022), used in Parts 2, 3, and 4 |
| `global_temp_anomalies.csv` | Annual global temperature anomalies relative to the 1951–1980 baseline ([NASA GISS](https://data.giss.nasa.gov/gistemp/)), used in Part 4 |

## Structure

| Part | Topic |
|------|-------|
| 1 | Introduction to Python: variables, data types, errors, and NumPy basics |
| 2 | Data Acquisition and Preparation: importing, cleaning, and formatting data with pandas |
| 3 | Data Analysis: descriptive statistics, t-tests, and confidence intervals |
| 4 | Data Visualisation: pie charts, bar charts, line charts, scatter plots, histograms, and uncertainty visualisation |

## Requirements

- Python 3.10+
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scipy`

All packages are available by default in Google Colab. For local use, install via:

```bash
pip install numpy pandas matplotlib seaborn scipy
```

## Running the Notebook

The recommended option for students new to Python is **Google Colab** as no local installation required. Upload the notebook and data files to Google Drive, open the notebook in Colab, and run cells in order.

For local use, ensure you have Python 3.10 or later and Jupyter installed before opening the notebook. [Anaconda](https://www.anaconda.com/) is the easiest way to get everything in one install.