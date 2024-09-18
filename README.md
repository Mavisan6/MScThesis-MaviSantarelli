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

## Contributions and Issues

Feel free to open issues for any bugs or questions. Contributions to improve the analysis or documentation are welcome.

## License

This project is licensed under the MIT License.
