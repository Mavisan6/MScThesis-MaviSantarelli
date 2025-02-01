# MSc Thesis: Assessing Amphibian Habitat Connectivity and BGI Opportunities in Scotland

## Repository Overview

This repository contains the code, data, and documentation for my MSc thesis on assessing amphibian habitat connectivity and evaluating opportunities for Blue-Green Infrastructure (BGI) development in Scotland. The project employs GIS techniques and multidimensional trait analysis to enhance amphibian conservation.

## Proposed Methodology

This project follows the Integrated Modelling Framework proposed by [Donati et al. (2022)](https://www.sciencedirect.com/science/article/pii/S0301479722008271?via%3Dihub) to assess amphibian habitat connectivity and evaluate Blue-Green Infrastructure (BGI) opportunities. The methodology involves:

1. **Data Assembly**: Gathering amphibian species data and environmental predictors across Scotland.
2. **Habitat Suitability Modelling**: Using species distribution models (SDMs) to identify biodiversity hotspots and their overlap with urban blue-green spaces.
3. **Ecological Network Modelling**: Employing resistance maps and Circuitscape analysis to model landscape connectivity and identify ecological corridors and barriers.
4. **Strategic BGI Planning**: Integrating results to propose targeted BGI interventions for enhancing amphibian connectivity.

JupyterLab notebooks will be used to display and document the research process, including detailed methodology, data analysis, and visualizations. These notebooks are designed to ensure transparency and reproducibility, allowing users to review and understand the steps and results of the research.

![Integrated Modelling Framework](docs/Integrated%20Modelling%20Framework.png) <!-- Replace with the path to your methodology image -->

*Figure 1. Overview of the integrated assessment framework used for identifying BGI opportunities to support amphibian connectivity in human-dominated landscapes (from Donati et al., 2022). This framework combines species distribution models and circuit theory to evaluate habitat suitability, ecological networks, and potential BGI interventions.*

## Repository Structure

The repository is organized into the following main directories and files:

### `/data`
- **`raw/`**: Contains raw, unprocessed data files used for the research.
- **`processed/`**: Includes cleaned and processed data files, ready for analysis.
- **`external/`**: Stores additional datasets and external data sources not originally part of the primary data.

### `/notebooks`
- **Jupyter Notebooks**: Contains notebooks for interactive data analysis, visualization, and documentation.
  - `data_analysis_notebook.ipynb`: Notebook for analyzing and visualizing data.
  - `model_evaluation_notebook.ipynb`: Notebook for evaluating and interpreting model results.

### `/scripts`
- **Python Scripts**: Scripts for data processing, model training, and results analysis.
  - `data_preprocessing.py`: Script for cleaning and preparing data.
  - `model_training.py`: Script for training models.
  - `results_analysis.py`: Script for analyzing and interpreting results.

### `/results`
- **`figures/`**: Includes plots and figures generated from the analysis.
- **`models/`**: Contains trained models and related files.
- **`outputs/`**: Stores any additional output files generated during the research.

### `/docs`
- **Documentation**: Provides detailed descriptions of the methodology, results, and other relevant information.
  - `methodology.md`: Description of the research methodology.
  - `results_summary.md`: Summary of the research results.

### Additional Files
- **`environment.yml`**: Conda environment file for managing project dependencies and ensuring a consistent setup.
- **`README.md`**: Project overview, setup instructions, and additional information.
- **`.gitignore`**: Specifies files and directories to be ignored by Git.

## Getting Started

1. Clone this repository to your local machine using GitHub Desktop or the command line.
2. Install the required Python packages listed in `requirements.txt`.
3. Open Jupyter Notebook to explore and run the notebooks.

## Environment Setup

This repository uses an `environment.yml` file to manage the dependencies required for the research project. This file ensures that all necessary libraries are installed and that the environment is consistent across different systems.

### Description of Libraries

- **python=3.9**: Specifies the Python version used in this environment.
- **numpy**: Essential for numerical operations and data manipulation.
- **pandas**: Provides data structures and data analysis tools.
- **matplotlib**: A plotting library for creating visualizations.
- **seaborn**: Provides a high-level interface for drawing attractive statistical graphics.
- **scikit-learn**: A machine learning library including tools for model fitting, classification, regression, and clustering.
- **jupyter**: Enables running Jupyter Notebooks for interactive data analysis and documentation.
- **geopandas**: Extends pandas to allow spatial operations on geometric types.
- **rasterio**: Reads and writes geospatial raster data.
- **fiona**: Provides a simple API for reading and writing vector data.
- **pyproj**: Interfaces with the PROJ library for cartographic transformations.
- **scikit-image**: Image processing library for Python.
- **shapely**: For manipulation and analysis of planar geometric objects.
- **joblib**: Provides tools for lightweight pipelining and caching results of expensive function calls.
- **xgboost**: Gradient boosting framework optimized for performance and speed.
- **statsmodels**: Provides classes and functions for statistical modeling and hypothesis testing.
- **pysal**: Python library for spatial analysis.

### Setting Up the Environment

To replicate the environment and ensure you have all the necessary dependencies, follow these steps:

1. **Install Anaconda**:
   If you don't have Anaconda installed, download and install it from [Anaconda's official website](https://www.anaconda.com/products/distribution).

2. **Download the Repository**:
   Clone the repository to your local machine using Git:
   ```bash
   git clone <repository-url>

3. **Navigate to the Repository**:
   Open a terminal (or Anaconda Prompt) and navigate to the cloned repository directory:
    ```bash
    cd path/to/repository

 4. **Create the Conda Environment**:
     Use the `environment.yml` file to create the environment. Run the following command:
    ```bash
    conda env create -f environment.yml

5. **Activate the Environment**:
   After the environment is created, activate it with:
   ```bash
   conda activate MScThesis-MaviSantarelli
   
6. **Install Circuiscape**:
   `Circuitscape`  is available from the conda-forge channel. If it is not installed automatically, you can manually install it with:
   ```bash
   conda install -c conda-forge circuitscape

8. **Install MaxEnt Separately**: `Maxent` is not included in the conda environment and needs to be installed manually. Download it from the [MaxEnt website](https://biodiversityinformatics.amnh.org/open_source/maxent/) and follow the provided instructions for setup. Integrate it manually with your Python scripts if needed.

9. Verify Installation: Ensure that all packages are installed correctly by running a few commands in a Python interpreter:
   ```Bash
   import numpy
   import pandas
   import matplotlib
   import seaborn
   import scikit_learn
   import geopandas
   import rasterio
   import fiona
   import pyproj
   import scikit_image
   import shapely
   import joblib
   import xgboost
   import statsmodels
   import pysal

---

## Guide: Running R within Python for MaxEnt Modelling

### Introduction

Species distribution modelling (SDM) often requires combining different statistical and machine learning approaches to achieve robust predictions. While many models (e.g., Generalized Linear Models [GLM], Generalized Additive Models [GAM], Random Forest [RF], and XGBoost) have Python-based implementations, MaxEnt (Maximum Entropy Modelling) is traditionally implemented in R or Java-based software.

This guide outlines a step-by-step process to integrate R within Python using `rpy2`, allowing users to:

✅ Run MaxEnt modelling within Python while keeping a unified workflow.  
✅ Leverage R packages (e.g., `dismo`, `rJava`) without switching environments.  
✅ Maintain compatibility with Python-based SDM models for ensemble modelling.  

### Step 1: Install R

**Why?**  
Python does not natively support MaxEnt, but R’s `dismo` package provides an interface to the MaxEnt software.  
Installing R ensures Python can communicate with it.

**Instructions:**  
1. Download and install **R (latest stable version)** from [CRAN](https://cran.r-project.org/).  
Example: Download **R-4.4.2 for Windows (64-bit)**.

2. Verify the installation by running in **Command Prompt** (Windows Terminal/Anaconda Prompt):

```sh
R --version
```

Expected output (example):
```sh
R version 4.4.2 (2024-10-31 ucrt) -- "Pile of Leaves"
```

### Step 2: Add R to System PATH

**Why?**
Adding R’s path ensures Python can locate and execute R commands using `rpy2`.

**Instructions:**
1. Open **System Environment Variables**:
- **Windows**: Search `"Environment Variables"` in the Start Menu → Edit System Environment Variables.
2. Locate the **PATH** variable and add the following directories (modify based on your R version):
```sh
C:\Program Files\R\R-4.4.2\bin
C:\Program Files\R\R-4.4.2\bin\x64
```
3. Verify by restarting Command Prompt and running:
```sh
R --version
```

### Step 3: Install Required R Packages

**Why?**
- `dismo`: Provides an interface for MaxEnt.
- `rJava`: Required for Java-based computations in MaxEnt.
- `raster & sp`: Handle spatial data.

**Instructions:**
1. Open **Anaconda Prompt** (or Command Prompt if R is available).
2. Start an **R session** by running:
```sh
R
```
3. Inside R, install the required packages:
```R
install.packages("dismo")
install.packages("rJava")
install.packages("raster")
install.packages("sp")
```
4. When prompted, select a CRAN mirror (e.g., UK).

### Step 4: Install Java and Set Up rJava

**Why?**
- `MaxEnt` requires Java to run models.
- `rJava` connects R with Java, allowing R to execute Java-based computations.

**Instructions:**
1. Download and install the **Java Development Kit (JDK)** from [Oracle](https://www.oracle.com/java/technologies/downloads/?er=221886).
- Recommended: **Windows x64 Installer** (`jdk-23_windows-x64_bin.exe`).
2. Set `JAVA_HOME` environment variable:
- In **Windows Environment Variables**, add:
```sh
JAVA_HOME = C:\Program Files\Java\jdk-23
```
3. Verify the installation:
```sh
java -version
```
Expected output (example):
```sh
java version "23.0.2" 2025-01-21
```
4. Open R again and test Java-R integration:
```R
library(rJava)
.jinit()
```

### Step 5: Download and Set Up MaxEnt

**Why?**
- MaxEnt runs as a Java-based standalone application (`maxent.jar`).
- R’s `dismo` package needs to locate maxent.jar to run MaxEnt models.

**Instructions:**
1. Download MaxEnt software from the [MaxEnt Website](https://biodiversityinformatics.amnh.org/open_source/maxent/).
2. Extract the `maxent.jar` file into a new directory:
```sh
C:\maxent\maxent.jar
```
3. Verify in R that the file is found:
```R
jar <- "C:/maxent/maxent.jar"
if (file.exists(jar)) {
    print("MaxEnt.jar found!")
} else {
    print("Error: MaxEnt.jar not found!")
}
```
Expected output:
```R
[1] "MaxEnt.jar found!"
```

### Step 6: Install and Configure `rpy2` in Python

**Why?**
- `rpy2` allows Python to **call R functions** directly within Jupyter Notebook.
- This maintains a **single workflow** instead of switching between Python and R.

**Instructions:**
1. Install rpy2 in the Anaconda environment:
```sh
pip install rpy2
```
2. Verify installation in Python:
```python
import rpy2.robjects as ro
print(ro.r("R.version"))
```
Expected output:
```sh
R version 4.4.2 (2024-10-31 ucrt)
```

### Final Verification & Running R in Jupyter Notebook

1. **Restart the system** to apply changes.
2. Open a **Jupyter Notebook** and verify R execution:
```python
import rpy2.robjects as ro
print(ro.r("R.version"))
```
3. Check if **MaxEnt** is recognized:
```python
ro.r('library(dismo)')
ro.r('jar <- "C:/maxent/maxent.jar"')
ro.r('print(file.exists(jar))')
```
Expected output:
```R
[1] TRUE
```

## Contributions and Issues

Feel free to open issues for any bugs or questions. Contributions to improve the analysis or documentation are welcome.

## License

This project is licensed under the MIT License.
