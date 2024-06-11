# Real-Estate-Price-Prediction-Using-Machine-Learning

<div align="justify">
The real estate market is a complex and dynamic sector influenced by various factors. Predicting property prices is crucial for buyers, sellers, and investors to make informed decisions. As data enthusiast with a passion for real estate, I embarked on a project to predict property prices using machine learning. This project uses a Random Forest model to forecast house prices based on key features like the number of bedrooms, bathrooms, lot size, house size, and zip code. I used a comprehensive real estate dataset from [Kaggle](https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset/data), which includes information about various properties across the US.
</div>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/1de3ce5b-b507-4111-a314-32a66a311d3d">
</p>

**Problem Statement**:

The goal of this project is to develop a predictive model for real estate prices in the US. Specifically, it aims to:
1. Identify key factors that influence property prices.
2. Build and evaluate a machine learning model to predict property prices based on these factors.
3. Provide actionable insights for potential buyers, sellers, and real estate professionals.

# Data Preprocessing

<div align="justify">

Preprocessing Steps:
1.	**Handling Missing Values:** Missing values were imputed using appropriate methods to ensure data integrity.
2.	**Outlier Transformation:** Outliers were identified and handled to prevent skewing the model.
3.	**Feature Engineering:** New features like 'price_per_sqft' were created for high-level visualizations.
</div>
<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/0018022c-7500-488c-ba6f-6213dc502742">
</p>

# Exploratory Data Analysis

<div align="justify">

EDA provided insights into the distribution and relationships of key variables in the dataset. Visualizations such as boxplots, histograms, and scatter plots were used to explore the data. Key findings included:

•	**Distribution of Prices:** The distribution of property prices showed significant variation, with a few high-value properties skewing the mean.<br/>
•	**Correlation Analysis:** A correlation matrix highlighted that house size and the number of bedrooms were strongly correlated with price, while other features like zip code also had a notable impact.

</div>
<br/>
A sample of the most notable graphs includes:
<br/>
<br/>

<div align="center">

**1.	Average Price per Square Foot vs. State**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/0f00e60e-124a-4899-bb78-55c3075af47a">
</p>

<div align="center">

**2.	Top 20 States by Average House Size**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/e5160cf0-f719-44bc-a94e-8f107b4b33d4">
</p>

<div align="center">

**3.	Top 20 States by Highest Average Price**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/4f580d6a-9a5e-462e-87ca-4e2f8ae00c92">
</p>

<div align="center">

**4.	Average Price per House Size**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/fc049a0d-27d8-4ff1-b59e-a1f8b3725e9e">
</p>

<div align="center">

**5.	Price Distribution by Top 20 States**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/0a291eed-b2ca-4b68-8b67-8de04935883b">
</p>

<div align="center">

**6.	Comparison of Major States House Sizes vs Price**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/c43bedb6-ae41-43c7-b388-88496b60c4ee">
</p>

<div align="center">

**7.	Price Densities by States**
</div>
<br/>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/b36df2d7-49c2-4a1f-8052-3b9b51ec1594">
</p>

# Model Building and Evaluation

<div align="justify">

**Linear Regression Model**
<br/>
<br/>
Linear Regression, a simple yet interpretable model, was used as a baseline. The model's performance was evaluated using RMSE (Root Mean Squared Error), resulting in an RMSE of 197570.33. The coefficients provided insights into the linear relationships between features and property prices.
<br/>

**Random Forest Model**
<br/>
<br/>
The Random Forest model, known for its versatility and accuracy, was then employed. This model handles non-linear relationships and interactions between features more effectively than linear regression. The Random Forest model achieved a significantly lower RMSE of 99881.67, indicating better predictive performance.
</div>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/5b090f4c-2228-4eb7-a228-65a1f74fd3bd">
</p>

# Feature Importance

<div align="justify">

Understanding which features contribute the most to the model's predictions is crucial. The feature importance from the Random Forest model revealed that:

•	**Zip Code:** Had the highest importance, indicating the significant impact of location on property prices.<br/>
•	**House Size:** Followed, highlighting the importance of property size.<br/>
•	**Number of Bathrooms:** Also contributed notably to the model's predictions.

</div>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/d01bd7ea-446f-4cf5-885c-138a818da025">
</p>

# Model Interpretation and Visualization

<div align="justify">
  
**Predictions**
<br/>
To validate the model's predictions, I tested it on individual and batch input data. The predictions for individual properties were compared, showcasing the model's practical application.
<br/>

**Residual Analysis**
<br/>
Residual plots for both models were analyzed to diagnose potential biases. The Random Forest model showed a better alignment with actual prices, though some high-value properties still presented challenges.
<br/>

**Visualizing Predictions**
<br/>
Scatter plots of actual vs. predicted prices and residual plots provided a clear visual comparison of model performance. The Random Forest model demonstrated a closer fit to the actual values, especially for mid-range properties.
</div>
<br/>

<p align="center" width="100%">
    <img width="33%" src="https://github.com/dmousouroulis/Real-Estate-Price-Prediction-Using-Machine-Learning/assets/156945591/ad1bef9e-53cd-46c8-9673-d348adb13a6a">
</p>

# Conclusion and Future Work

<div align="justify">
Through strategic data preprocessing, exploratory analysis, and the application of machine learning models, this project successfully predicted real estate prices. The Random Forest model outperformed the Linear Regression model, providing more accurate predictions.
</div>
<br/>

**Future Work:**
1.	**Hyperparameter Tuning:** Further optimize the Random Forest model to improve performance.
2.	**Advanced Models:** Experiment with more sophisticated models like Gradient Boosting Machines (GBM), XGBoost, or Neural Networks.
3.	**Geospatial Analysis:** Incorporate geospatial data to better capture location effects.
4.	**Time Series Analysis:** Analyze historical data to identify trends and seasonality in property prices.

<br/>

By enhancing the model with additional features and advanced techniques, future iterations of this project can achieve even greater accuracy and insight into the real estate market.
