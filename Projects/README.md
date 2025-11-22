## Crop Yield Estimation using Machine Learning

A machine learning project focused on predicting crop yield using various agricultural factors including soil type, weather conditions, and farming practices.

### Project Overview  
This project compares multiple machine learning algorithms to predict crop yield based on soil type, weather conditions, and farming practices using a synthetic agricultural dataset.
Dataset: 1 million samples from Kaggle (Samuel Ott Attakorah)
Task: Supervised Regression
Target: Crop Yield (tons/hectare)

### Machine Learning Models
Four regression models were implemented and evaluated:

1. Dummy Regressor (Baseline)
2. Ridge Regression
3. Random Forest Regressor
4. Histogram-based Gradient Boosting

### Methodology
Preprocessing:  
Removed 231 outliers (negative yields)  
Normalized numerical features  
OneHot encoding for categorical features  

Evaluation:  
80/20 train-test split (stratified by region)  
Stratified cross-validation for hyperparameter tuning  
Metrics: RMSE and MAE  

### Project Timeline
- **Milestone 1:** October 8, 2025 - Dataset exploration and initial analysis
- **Milestone 2:** November 19, 2025 - Model implementation and evaluation

### Limitations and Future Work
Current Limitations:
- Dataset is synthetic and may not fully reflect real-world variability
- Limited environmental and measurement variability 

Future Improvements:
- Add realistic noise to simulate environmental variability and test model generalization on real-world agricultural data
- Incorporate additional features (pest data, advanced soil metrics)
- Test on multi-crop and multi-region real datasets

### License

This project is available for educational and research purposes.

