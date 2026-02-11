## Crop Yield Estimation using Machine Learning 
A  machine learning project predicting crop yield based on environmental and agricultural factors using a large-scale synthetic dataset.

### Overview 
This project implements and compares multiple regression algorithms to predict crop yield (tons/hectare) based on:
- Soil type
- Weather conditions
- Farming practices (fertilizer and irrigation use)
- Regional characteristics

**Learning Task:** Supervised Regression

### Dataset
**Source:** [Kaggle - Agriculture Crop Yield Dataset](https://www.kaggle.com/datasets/samuelotiattakorah/agriculture-crop-yield) by Samuel Ott Attakorah
**Size:** 1 million samples (after cleaning: 999,769 samples)

### Project Structure

```
Projects/
├── README.md                 
├── data.csv                  # Dataset (1M samples)
├── full_code.ipynb          # Complete implementation
├── milestone1_code.ipynb    # Initial EDA
├── presentation1.pdf        # Milestone 1 presentation
└── presentation2.pdf        # Milestone 2 presentation
```

### Features
**Categorical Variables:**
- `Region` - Geographic region (West, South, North, East)
- `Soil_Type` - Soil classification (Sandy, Clay, Loam, Silt, Peaty, Chalky)
- `Crop` - Crop type (Cotton, Rice, Barley, Soybean, Wheat, Maize)
- `Weather_Condition` - Predominant weather (Cloudy, Rainy, Sunny)
- `Fertilizer_Used` - Boolean indicating fertilizer application
- `Irrigation_Used` - Boolean indicating irrigation use
**Numerical Variables:**
- `Rainfall_mm` - Rainfall during growth period (100-1000mm)
- `Temperature_Celsius` - Average temperature (15-40°C)
- `Days_to_Harvest` - Days from planting to harvest (60-149 days)
**Target Variable:**
- `Yield_tons_per_hectare` - Crop yield in tons per hectare (continuous)

### Models
Four regression models were implemented and evaluated:

| Model | Type | Purpose |
|-------|------|---------|
| **Dummy Regressor** | Baseline | Mean prediction benchmark |
| **Ridge Regression** | Linear | L2 regularized linear model |
| **Random Forest** | Ensemble | Tree-based ensemble method |
| **Histogram Gradient Boosting** | Ensemble | Optimized gradient boosting |

### Methodology
1. Data Preprocessing
Outlier Removal
Feature Engineering  
2. Train-Test Split
- **Split Ratio:** 80% train / 20% test
- **Strategy:** Stratified by Region  
3. Model Training
- Hyperparameter tuning via RandomizedSearchCV
- Stratified cross-validation
- Grid search for optimal parameters
4. Evaluation Metrics
- **RMSE** (Root Mean Squared Error)
- **MAE** (Mean Absolute Error)
- **R² Score**

### Limitations
**Data Constraints:**
1. **Synthetic Data:** Dataset is artificially generated and may not fully reflect real-world agricultural complexity
2. **Limited Variability:** Reduced environmental and measurement noise compared to actual field data
3. **Feature Scope:** Missing potentially important factors:
   - Pest and disease data
   - Advanced soil metrics (pH, nutrients)
   - Historical yield trends
   - Market and economic factors

**Model Limitations:**
- Assumes linear/tree-based relationships
- May not capture complex temporal dependencies
- Generalization to real-world scenarios untested

### Project Timeline
- **Milestone 1:** October 8, 2025 - Dataset exploration and initial analysis
- **Milestone 2:** November 19, 2025 - Model implementation and evaluation

### Contributors
- **Angelica Moreno**
- **Arunima Sen**  
- **Ethel Ogallo**
