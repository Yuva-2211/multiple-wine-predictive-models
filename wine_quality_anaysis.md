

# Wine Quality Prediction - Machine Learning Analysis

## Overview

This project involves the analysis and prediction of wine quality based on a dataset containing various chemical properties of red wine. The primary goal is to predict the quality of the wine based on these features using machine learning models.

## Dataset

The dataset used in this project is the **Wine Quality** dataset (red wine) from the UCI Machine Learning Repository. It contains several chemical properties of red wine and a quality score based on expert ratings.

### Key Features:
- **Fixed acidity**: Amount of acid in wine.
- **Volatile acidity**: Acidity that can evaporate.
- **Citric acid**: A weak organic acid.
- **Residual sugar**: Sugar remaining after fermentation.
- **Chlorides**: Salt content.
- **Free sulfur dioxide**: Free form of sulfur dioxide (SO2) in wine.
- **Total sulfur dioxide**: Total amount of sulfur dioxide.
- **Density**: Wine density.
- **pH**: Acidity.
- **Sulphates**: Amount of sulphate.
- **Alcohol**: Alcohol content.
- **Quality**: Target variable (score from 0 to 10, where higher values represent better quality).

## Data Preprocessing

The following steps were carried out to prepare the dataset for modeling:
1. **Handling Missing Values**: No missing values were found.
2. **Feature Correlation**: A correlation matrix was generated to examine the relationships between the features and the target variable.
3. **Feature Engineering**: A new binary feature `good_quality` was created, which classifies wines with a quality score of 7 or higher as `1` (good quality) and others as `0` (low quality).

### Key Insights:
- **Alcohol** showed the strongest positive correlation with wine quality.
- **Volatile acidity** and other factors like **density** and **chlorides** were negatively correlated with quality.
- **Sulphates** and **citric acid** had moderate positive correlations.

## Exploratory Data Analysis (EDA)

The following visualizations were generated:
- Correlation heatmap to visualize the relationships between features.
- Line plots of alcohol content vs. quality and density vs. quality.
- Boxplots and histograms to visualize the distribution of wine quality and key features.

## Model Building

Multiple machine learning models were trained and evaluated to predict the quality of wine:
1. **Decision Tree Classifier**
2. **Random Forest Classifier**
3. **XGBoost Classifier**
4. **Logistic Regression** (used for comparison after feature scaling)

The data was split into a **training** and **testing** set, with an 80%/20% ratio.

## Model Evaluation

The models were evaluated using the following metrics:
- **Accuracy**
- **Precision**, **Recall**, and **F1-Score** for both classes (Good quality vs Low quality)
- **Macro and Weighted Average Precision**, **Recall**, and **F1-Score**
- **AUC Score** for the Logistic Regression model

### Model Comparison

The table below summarizes the performance of each model:

| Model              | Accuracy | Precision (Class 0) | Recall (Class 0) | F1-Score (Class 0) | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) | Macro Avg Precision | Macro Avg Recall | Macro Avg F1-Score | Weighted Avg Precision | Weighted Avg Recall | Weighted Avg F1-Score |
|--------------------|----------|---------------------|------------------|--------------------|---------------------|------------------|--------------------|---------------------|-------------------|---------------------|------------------------|---------------------|-----------------------|
| Decision Tree      | 0.85     | 0.91                | 0.91             | 0.91               | 0.37                | 0.37             | 0.37               | 0.64                | 0.64              | 0.64                | 0.85                   | 0.85                | 0.85                  |
| Random Forest      | 0.9125   | 0.92                | 0.99             | 0.95               | 0.81                | 0.34             | 0.48               | 0.87                | 0.67              | 0.72                | 0.91                   | 0.91                | 0.90                  |
| XGBoost            | 0.909375 | 0.93                | 0.98             | 0.95               | 0.70                | 0.42             | 0.52               | 0.81                | 0.70              | 0.74                | 0.90                   | 0.91                | 0.90                  |
| Logistic Regression| 0.88     | 0.91                | 0.96             | 0.93               | 0.45                | 0.26             | 0.33               | 0.68                | 0.61              | 0.63                | 0.85                   | 0.88                | 0.86                  |

- The **Random Forest** model achieved the highest accuracy (91.25%), while **Decision Tree** and **XGBoost** performed similarly well.
- **Precision and Recall** for class 1 (Good quality) showed a trade-off between models, with **Random Forest** offering a good balance between precision and recall.

## Conclusion

- **Random Forest** and **XGBoost** are the most effective models for predicting wine quality based on the dataset, with **Random Forest** slightly outperforming others in terms of accuracy.
- Further improvements can be made by fine-tuning hyperparameters or exploring other models and techniques.

## Next Steps

- **Hyperparameter Tuning**: Perform hyperparameter tuning for the top models.
- **Model Deployment**: Develop a pipeline to predict wine quality on new data.
- **Feature Engineering**: Explore the potential of additional features or advanced techniques for improving performance.

---
## Author 
   [Yuva Shankar Narayana](https://www.linkedin.com/in/yuva-shankar-narayana/)