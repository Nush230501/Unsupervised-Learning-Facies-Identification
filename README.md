# Geological Facies Identification

## Overview
This project focuses on identifying geological facies using well log data through clustering techniques. We utilize K-means clustering and Principal Component Analysis (PCA) to categorize facies based on well log measurements such as Gamma Ray (GR), Density (RHOB), Neutron Porosity (NPHI), and Resistivity (RT).

## Contents
1. [Project Files](#project-files)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Data Description](#data-description)
5. [Analysis Steps](#analysis-steps)
6. [Results](#results)
7. [License](#license)

## Project Files
- `geological_facies_identification.ipynb`: Jupyter Notebook containing the analysis code.
- `well_log_data.las`: Example LAS file with well log data.
- `requirements.txt`: List of required Python packages.

## Installation
To run the analysis locally, you'll need to install the required Python packages. You can do this using pip:

```bash
pip install -r requirements.txt
```
## Usage

### Download the Data

- Ensure you have the LAS file with well log data available.

### Run the Analysis

1. Open the Jupyter Notebook: `geological_facies_identification.ipynb`.
2. Follow the instructions in the notebook to:
   - Load the data.
   - Preprocess it.
   - Perform PCA.
   - Apply K-means clustering.

### Inspect Results

- The notebook includes visualizations of the clustering results and facies distribution with depth.

## Data Description

### Well Log Data

- **Gamma Ray (GR):** Measures natural radioactivity.
- **Density (RHOB):** Measures formation density.
- **Neutron Porosity (NPHI):** Measures hydrogen content to infer porosity.
- **Resistivity (RT):** Indicates the presence of hydrocarbons.

### Example Files

- `well_log_data.las`: LAS file containing well log measurements.

## Analysis Steps

1. **Load the Data:**
   - Use `lasio` to read LAS files and convert them to a Pandas DataFrame.
2. **Preprocess the Data:**
   - Handle missing values.
   - Normalize the data.
3. **Dimensionality Reduction:**
   - Apply PCA to reduce the number of features for clustering.
4. **Clustering:**
   - Use K-means clustering to identify distinct facies.
5. **Visualization:**
   - Plot PCA components and facies distribution with depth.
6. **Interpretation:**
   - Analyze clusters to identify geological facies.

## Results

The clustering results categorize the well log data into distinct facies, interpreted as follows:

- **Facies 0 (Purple):** Likely Shale.
- **Facies 1 (Blue):** Likely Sandstone.
- **Facies 2 (Green):** Likely Dolomite.
- **Facies 3 (Yellow):** Likely Limestone.

These facies are characterized based on gamma-ray, density, neutron porosity, and resistivity measurements.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.
