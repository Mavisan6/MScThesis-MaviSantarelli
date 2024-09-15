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

This repository uses an `environment.yml` file to manage dependencies required for the research. The environment file ensures that all necessary libraries are installed and that the environment is consistent.

### Description of Libraries

- **`python=3.9`**: Specifies the Python version used in this environment.
- **`numpy`**: Essential for numerical operations and data manipulation.
- **`pandas`**: Provides data structures and data analysis tools.
- **`matplotlib`**: A plotting library for creating visualizations.
- **`seaborn`**: Provides a high-level interface for drawing attractive statistical graphics.
- **`scikit-learn`**: A machine learning library including tools for model fitting, classification, regression, and clustering.
- **`jupyter`**: Enables running Jupyter Notebooks for interactive data analysis and documentation.
- **`geopandas`**: Extends pandas to allow spatial operations on geometric types.
- **`rasterio`**: Reads and writes geospatial raster data.
- **`fiona`**: Provides a simple API for reading and writing vector data.
- **`pyproj`**: Interfaces with the PROJ library for cartographic transformations.
- **`scikit-image`**: Image processing library for Python.
- **`maxent`**: Implementation of the Maximum Entropy model for species distribution modeling.
- **`circuitscape`**: Tool for modeling ecological connectivity and landscape resistance.
- **`shapely`**: For manipulation and analysis of planar geometric objects.
- **`joblib`**: Provides tools for lightweight pipelining and caching results of expensive function calls.
- **`xgboost`**: Gradient boosting framework optimized for performance and speed.
- **`statsmodels`**: Provides classes and functions for statistical modeling and hypothesis testing.
- **`pysal`**: Python library for spatial analysis.

## Contributions and Issues

Feel free to open issues for any bugs or questions. Contributions to improve the analysis or documentation are welcome.

## License

This project is licensed under the MIT License.
