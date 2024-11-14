# EEG Data Analysis and Classification Project

## Overview
This project involves the analysis and classification of EEG data collected using the EMOTIV Insight EEG device. The dataset contains power spectral density (PSD) values for five electrode channels (AF3, AF4, T7, T8, Pz) across different frequency bands (Theta, Alpha, Beta Low, Beta High, Gamma). The goal is to explore, preprocess, and build a machine learning model to classify mental states corresponding to:

- **0:** Movements of the left hand
- **1:** Movements of the right hand
- **2:** No hand movements

## Dataset Description
### Source
This dataset was obtained from Kaggle and can be accessed [here]([https://www.kaggle.com/](https://www.kaggle.com/datasets/fabriciotorquato/brain-wave-data-from-hands-movement-of-eeg/data)). It provides preprocessed EEG data specifically for machine learning applications.

### Equipment
- **Device:** EMOTIV Insight EEG
- **Sampling Frequency:** 128 Hz
- **Electrodes:** AF3, AF4, T7, T8, Pz
- **Resolution:** 16-bit ADC

### Data Structure
The dataset is organized in CSV files, with one file per participant (e.g., `user_a.csv`, `user_b.csv`). Each file contains the following columns:

- **Values:** Target variable (0, 1, 2)
- **PSD Features:**
  - Power values for each electrode channel (AF3, AF4, T7, T8, Pz) across frequency bands:
    - Theta
    - Alpha
    - Beta Low (BetaL)
    - Beta High (BetaH)
    - Gamma

### Example Data Format
| Values | POW.AF3.Theta | POW.AF3.Alpha | POW.AF3.BetaL | POW.AF3.BetaH | POW.AF3.Gamma | ... |
|--------|---------------|---------------|---------------|---------------|---------------|-----|
| 0      | 177.54        | 44.20         | 52.90         | 111.84        | 118.63        | ... |
| 1      | 134.39        | 36.72         | 58.06         | 138.92        | 146.54        | ... |
| 2      | 101.18        | 32.58         | 76.66         | 157.98        | 169.94        | ... |

### Label Description
- **0:** Movements of the left hand
- **1:** Movements of the right hand
- **2:** No hand movements

## Goals
### Exploration
1. Understand the structure of the dataset.
2. Visualize patterns and correlations within the data.
3. Identify and interpret relationships between PSD features and the target variable.

### Preprocessing
1. Normalize PSD features to ensure consistent scaling.
2. Handle missing data (if any).
3. Balance the dataset across target labels.

### Machine Learning
1. Develop a classifier to predict the target variable (Values).
2. Evaluate the performance of the model using metrics like accuracy, precision, recall, and F1 score.

## Initial Steps
### 1. Exploratory Data Analysis (EDA)
- Compute summary statistics for each feature.
- Generate box plots, histograms, and pair plots to visualize feature distributions.
- Create heatmaps to identify correlations between features.

### 2. Preprocessing
- Normalize power values across all features.
- Ensure consistent dimensionality and formatting.
- Check for and handle missing or anomalous values.

### 3. Feature Selection
- Use feature correlation analysis to identify redundant or irrelevant features.
- Optionally, apply Principal Component Analysis (PCA) for dimensionality reduction.

## Example Questions to Explore
- How do PSD values vary across different mental states?
- Which frequency bands are most predictive of each mental state?
- How do electrode-specific features correlate with the target variable?

## Dependencies
- **Python Libraries:**
  - `numpy`: Numerical operations
  - `pandas`: Data manipulation
  - `matplotlib`: Data visualization
  - `seaborn`: Advanced visualizations
  - `scikit-learn`: Machine learning tools
  - `tensorflow` or `pytorch` (optional): Deep learning

## File Structure
```plaintext
brain_bci_project/
|-- extracted_data/
|   |-- eeg/
|   |   |-- user_a.csv
|   |   |-- user_b.csv
|   |   |-- ...
|-- scripts/
|   |-- eda.py
|   |-- preprocess.py
|   |-- train_model.py
|-- README.md
```

## Roadmap
1. Conduct EDA to gain insights into the dataset.
2. Preprocess the data for machine learning.
3. Train and evaluate classification models.
4. Optimize the model for deployment.

## Contribution
If you wish to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature.
3. Submit a pull request for review.

