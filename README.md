# E-Commerce Customer Segmentation

 I worked on this project using a proprietary dataset from a retail company, provided as part of my fully online "Advanced Analytics" coursework at university. Here, I made an initial dive into numerous stages of the machine learning modeling pipeline, including in-depth data preprocessing, feature engineering, a variety of ML models, hyperparameter tuning, and many more. Additionally, I researched and incorporated various use cases demonstrating how businesses can benefit from implementing this Customer Segmentation Model. Overall, this experience not only taught me substantial technical skills but also demonstrated my ability to independently learn and implement complex concepts in a virtual setting, all within just 8 weeks!

Here is the link to **full detailed report** of this project: https://naga-chaitanya-paladugu.github.io/Ecommerce-Classification-Model/. 

 Below is a **quick summary** of project's main details. 
## Overview
This project focuses on analyzing the purchasing behavior of 9,506 online clients for a major American retailer, Vanguard, over the past 12 months. The goal is to build a robust classification model to segment customers into ‘Core’ (regular tier) and ‘Up’ (premium tier) categories, with a priority on making as many predictions on ‘Up’ customers as possible due to their higher revenue generation and importance to the business. This segmentation can help in strategic decision-making for marketing and sales.
## Dataset
- **Source**: Proprietary dataset of a retail company shared by SLU.
- **Size**: 9,504 observations, 16 variables
- **Key Variables**:
  - **Demographic Details**: Gender, marital status, age
  - **Purchasing Behavior**: Cumulative sales, frequency, average ticket, recency, consistency
  - **Customer Segmentation**: Segment 1 (Core or Up), loyalty group, price group, segment 2
  - **Other**: Most used platform

## Methodology
1. **Data Preprocessing**:
   - Handled missing values
   - Dropped redundant columns (Client ID, Birth Date)
   - Renamed columns for clarity
   - Used Median Imputation in more than 10% of missing values in the Age column.
   - Removed outliers from numerical column.

2. **Exploratory Data Analysis (EDA)**:
   - Analyzed distributions and relationships of key variables
   - Visualized data using histograms, box plots, and bar plots
   - Identified and handled outliers
   - Identified multi-collinearity among features.

3. **Feature Engineering**:
   - One-hot encoded categorical variables
   - Scaled numerical features using standardization

4. **Model Building**:
   - Parametric Models
      1. Logistic Regression - Baseline model with L1 regularization (Lasso). Tuned using cross-validation to find the optimal regularization parameter.
   - Non-Parametric Models
     1. Random Forest - Tuned for the number of trees and maximum depth.
     2. Gradient Boosting - Tuned for the number of boosting stages and maximum depth.
     3. Support Vector Machine (SVM) - Evaluated with different kernels and tuned for the best C value.
     4. Neural Networks - Tuned for the number of layers and neurons using a subset of the data.
5. **Model Evaluation**:
   - Performed 10-fold cross-validation
   - Compared models using accuracy, precision, recall, F1 score, and confusion matrices

## Results
- **Gradient Boosting:** Achieved the highest recall (98.10%) and F1-score (76.03%), making it the best model for identifying ‘Up’ customers.
- **Random Forest:** Balanced performance with good precision (63.00%) and recall (94.07%).
- **SVM:** Moderate performance with a recall of 93.74% and F1-score of 75.06%.
- **Lasso Regression:** Simpler model with a recall of 92.84% and F1-score of 73.61%.
- **Neural Networks:** Lower performance with a recall of 71.48% and F1-score of 67.09%.

## Conclusions
- **Best Model:** Gradient Boosting is the top-performing model, effectively capturing the complex, non-linear relationships in the data due to its high recall and F1-score. However, Random Forest is the best choice for time-sensitive applications due to its faster training and prediction times, while still offering similar performance.
- **Feature Importance:** Key predictors include cumulative sales, loyalty group, average ticket, and consistency. Features like marital status and price group were less important and can be dropped to simplify the model, making it more interpretable without losing significant predictive power.
- **Business Impact:** The model identifies high-value ‘Up’ customers, enabling targeted marketing and personalized offers to maximize revenue. Leveraging top features like cumulative sales and loyalty group can enhance customer engagement and retention through strategic marketing initiatives.
## Future Work
- Conduct PCA and cluster analysis for dimensionality reduction and improved interpretability.
- Fine-tune classification thresholds to balance true positives and true negatives.
- Perform comprehensive hyperparameter tuning, explore additional features and interactions to enhance model performance.

