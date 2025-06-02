# Environmental Carcinogenesis Decoded: Tracing Cancer's Roots with Advanced Machine Learning

By: Danielle Grunwald, Gabriel Orbe, Badr Abushaar

This repository contains the code, data, and documentation for our research, which investigates the relationship between environmental pollution and cancer incidence rates for bladder and lung cancers.

## Table of Contents

- [Abstract](#abstract)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Data Sources](#data-sources)
- [Methodology Overview](#methodology-overview)
- [Results](#results)

## Abstract

This research investigates the relationship between environmental pollution and cancer incidence rates for bladder and lung cancers. Advanced machine learning techniques were employed to analyze the impact of air and water pollutants on bladder and lung cancer incidence rates by utilizing a multitude of government datasets, such as those from the Environmental Protection Agency (EPA), the Centers for Disease Control and Prevention (CDC), and the National Health Institute (NCI). The core problems examined through this research involved working with high-dimensional data from multiple sources, addressing challenges in preprocessing, feature engineering, and building predictive models to uncover meaningful patterns with the use of government data that could contain redactions or gaps within spatial-temporal data. By working with high-dimensional data, Mutual Information was discovered to be a great basis for reducing the dimensions and strengthening the model. In order to capture temporal dependencies in the time series data, attention-enhanced LSTM models were implemented with different adjustable configurations being identified for the bladder and lung cancer predictions. Feature selection techniques using mutual information were also applied to mitigate overfitting. Findings reveal the strong correlations between environmental pollutants and cancer incidence rates across different geographical regions in the United States. The ultra ensemble model, which is the final model used, achieved an R² score of .6584 for bladder cancer and .5304 for lung cancer, demonstrating strong predictive accuracy for environmental cancer risk factors with correlations of 0.8245 and 0.7333 respectively. This research contributes to the understanding of how environmental factors could influence cancer incidence rates and provides a methodological framework for analyzing complex, multi-source, high dimensional, environmental health data. The results have potential implications on handling high dimensional, multi-source time series and geographical data and may impact public health policy, environmental regulation, and targeted cancer prevention strategies in high-risk areas.

## Repository Structure

```bash
healthcare-capstone/
├── data/                                   # Preprocessed data
├── data_pulls/                             # Raw data sources
├── MLPmodel.ipynb                          # Multilayer Perceptron model
|── README.md                               # Project documentation
├── StatAnalysis.ipynb                      # Statistical analysis
├── decisionTreeModel.ipynb                 # Decision Tree model
├── feature_engineering.ipynb               # Feature engineering steps
├── linRegAndSVRmodels.ipynb                # Linear Regression and SVR models
├── model.ipynb                             # Additional modeling approaches
├── Lung_Model.ipynb                        # Final Model for Lung Cancer Prediction
├── Bladder_Model.ipynb                     # Final Model for Bladder Cancer Prediction
├── spatial-temporal gnn.ipynb              # Spatial-temporal gnn model
└── modelcomparison_transformer.ipynb       # Model comparison using transformers


```

## Getting Started

1. **Clone the Repository**

   ```bash
   git clone https://github.com/gorbe2002/healthcare-capstone.git
   cd healthcare-capstone
   ```

2. **Set Up Your Environment**

   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

## Data Sources

Cancer Incidence:

- National Health Institute: "Surveillance, Epidemiology, and End Results (SEER) Program"
- Centers for Disease Control and Prevention: "Wonder Incidence"

Air Pollution:

- United States Environmental Protection Agency: "Air Quality System (AQS)"

Bladder Pollution:

- United States Environmental Protection Agency: "Toxics Release Inventory (TRI)"
- United States Environmental Protection Agency: "Assessment, Total Maximum Daily Load (TMDL) Tracking and Implementation System (ATTAINS)"

## Methodology Overview

## Results
Bladder Cancer Model Results:

|   Model   |   Mean Squared Error (MSE) |   R<sup>2</sup> Score  |
| --------- | -------------------------- | ---------------------- |
| Emsemble LSTM | 0.00000012 | 0.5628289 |
| Two-Stage | 0.00000018 | 0.3753374 |
| Trend | 0.00000017 | 0.4119355 |
| Ultra Emsemble | 0.00000010 | 0.6583507 |

Lung Cancer Model Results:

|   Model   |   Mean Squared Error (MSE) |   R<sup>2</sup> Score  |
| --------- | -------------------------- | ---------------------- |
| Emsemble LSTM | 0.00000130 | 0.3011947 |
| Two-Stage | 0.00000128 | 0.3120608 |
| Trend | 0.00000135 | 0.2721805 |
| Ultra Emsemble | 0.00000093 | 0.5001329 |
