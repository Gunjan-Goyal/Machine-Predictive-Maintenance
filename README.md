# Predictive Maintenance using Machine Learning

## Overview
This project applies machine learning techniques for predictive maintenance, helping to identify potential failures before they occur. The dataset used in this project includes sensor data from industrial machines, and the analysis involves unsupervised learning techniques to detect anomalies and predict maintenance needs.

## Features
- **Data Preprocessing**: Cleaning and preparing sensor data for analysis.
- **Exploratory Data Analysis (EDA)**: Visualizing trends and distributions.
- **Unsupervised Learning Models**: Clustering techniques for anomaly detection.
- **Model Evaluation**: Assessing model performance using relevant metrics.

## Installation
To run this project, install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/predictive-maintenance.git
   cd predictive-maintenance
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `project_predicitve_maintenance.ipynb` and execute the cells step by step.

## Dataset
The dataset used in this project is the **Machine Predictive Maintenance Classification Dataset**. Since real predictive maintenance datasets are often difficult to obtain and publish, this synthetic dataset has been designed to reflect real-world predictive maintenance scenarios as closely as possible.

### Dataset Details
- **Size**: 10,000 data points with 14 features.
- **Columns**:
  - `UID`: Unique identifier ranging from 1 to 10,000.
  - `productID`: Product quality variant categorized as **L** (Low, 50%), **M** (Medium, 30%), and **H** (High, 20%), along with a variant-specific serial number.
  - `air temperature [K]`: Generated using a random walk process, normalized to a standard deviation of 2K around 300K.
  - `process temperature [K]`: Generated using a random walk process, normalized to a standard deviation of 1K, added to air temperature plus 10K.
  - `rotational speed [rpm]`: Computed from power of 2860W, with normally distributed noise.
  - `torque [Nm]`: Normally distributed around 40Nm with a standard deviation of 10Nm, with no negative values.
  - `tool wear [min]`: The quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process.
  - `machine failure`: Indicates whether the machine failed at a given data point due to any of the following failure types:
    - **Target**: Failure or Not.
    - **Failure Type**: Specifies the type of failures are :
        - Heat Dissipation Failure
        - Power Failure
        - Overstrain Failure
        - Tool Wear Failure

⚠ **Important**: There are two target variables. Do not mistakenly use one of them as a feature, as this will lead to data leakage.

## Results
- Anomaly detection insights.
- Visualizations of machine sensor readings.
- Predictive maintenance alerts based on model predictions.

## Acknowledgements
Dataset sourced from **UCI Machine Learning Repository**: [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset)
