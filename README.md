# E-Commerce Customer Segmentation

### I am working on this e-commerce project by applying the ML coursework that I am taking in this semester. Great Learning! This is still on building stage and many more changes and improvements need to be made as I learn more.
## Project Overview
This project aims to analyze the purchasing behavior of 9,506 online clients for a major American retailer, Vanguard, over the past 12 months. The goal is to develop a robust segmentation model to enhance strategic decisions for the retailer’s online presence.

## Dataset
- **Source**: Proprietary dataset from Vanguard
- **Size**: 9,504 observations, 16 variables
- **Key Variables**:
  - **Demographic Details**: Gender, marital status, age
  - **Purchasing Behavior**: Cumulative sales, frequency, average ticket, recency, consistency
  - **Customer Segmentation**: Segment 1, loyalty group, price group, segment 2
  - **Other**: Most used platform

## Objective
To develop a segmentation model with 'Segment 1' as the target variable, using demographic details and purchasing behavior data.

## Methodology
1. **Data Preprocessing**:
   - Handled missing values
   - Dropped redundant columns (Client ID, Birth Date)
   - Renamed columns for clarity
   - Imputed missing values in the Age column
   - Removed outliers from numerical columns

2. **Exploratory Data Analysis (EDA)**:
   - Analyzed distributions and relationships of key variables
   - Visualized data using histograms, box plots, and bar plots
   - Identified and handled outliers

3. **Feature Engineering**:
   - One-hot encoded categorical variables
   - Scaled numerical features using standardization

4. **Model Building**:
   - Implemented and evaluated multiple models:
     - **Logistic Regression**: Baseline and Lasso regularization
     - **Random Forest**: Baseline and optimized with hyperparameter tuning
     - **Gradient Boosting**: Baseline and optimized with hyperparameter tuning
     - **Support Vector Machine (SVM)**: Evaluated different kernels and optimized with hyperparameter tuning

5. **Model Evaluation**:
   - Performed 10-fold cross-validation
   - Compared models using accuracy, precision, recall, F1 score, and confusion matrices

## Key Findings
- **Significant Predictors**: Cumulative sales, average ticket, loyalty group, most used platform
- **Model Performance**:
  - **Logistic Regression (Lasso)**:
    - Accuracy: 61.6%
    - Precision: 62.1%
    - Recall: 92.1%
    - F1 Score: 74.2%
  - **Random Forest**:
    - Accuracy: 63.9%
    - Precision: 63.7%
    - Recall: 91.2%
    - F1 Score: 75.0%
  - **Gradient Boosting**:
    - Accuracy: 64.8%
    - Precision: 62.9%
    - Recall: 99.3%
    - F1 Score: 77.0%
  - **Support Vector Machine (SVM)**:
    - Accuracy: 62.0%
    - Precision: 62.4%
    - Recall: 90.3%
    - F1 Score: 73.8%

## Conclusions
- **Predictive Power**: Cumulative sales and average ticket are strong predictors of customer segments
- **Model Performance**: Gradient Boosting achieved the highest accuracy, but Random Forest provided a better balance of metrics
- **Implications**: The model can help Vanguard identify customer segments and tailor marketing strategies accordingly

## Future Work
- Explore additional features and interactions
- Implement more advanced hyperparameter tuning
- Investigate the impact of external factors on customer behavior

## References
- Graff, V. (2023). Dimension Reduction: Facing the Curse of Dimensionality. Medium.
- Johnson, Ott, & Dogucu (2021). Bayes Rules! An Introduction to Applied Bayesian Modeling.
- Mudigonda, S. (2024). Video lecture on Multivariate Normal Models. Saint Louis University.

