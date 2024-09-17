# MSc Thesis: Strategic Planning for Blue-Green Infrastructure: A GIS Approach to Amphibian Conservation in Urban and Peri-Urban Areas of Central Scotland

## Repository Overview

This repository contains the following components:

- **Jupyter Notebooks**: Detailed analysis and visualizations of amphibian habitat connectivity using species distribution models (SDMs), habitat suitability models, and ecological connectivity modeling.
- **Python Scripts**: Implementation of methodologies including Scikit-learn for machine learning, MaxEnt for SDMs, and Circuitscape for ecological connectivity modeling.
- **Data**: Datasets used for the analysis, including species trait information and environmental variables.
- **Documentation**: Descriptions of the methodology, results, and interpretations.

## Key Features

- **Multidimensional Trait Analysis**: Analysis of six amphibian species (Common Toad, Palmate Newt, Smooth Newt, Common Frog, Great Crested Newt, and Alpine Newt) to evaluate habitat connectivity.
- **Blue-Green Infrastructure Evaluation**: Identification of BGI opportunities to enhance amphibian corridors and connectivity.
- **Transparency and Reproducibility**: All code and data are available for review and replication, following best practices for reproducible research.

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
