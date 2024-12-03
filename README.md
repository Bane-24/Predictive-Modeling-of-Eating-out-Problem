# Predictive Modelling of Eating-Out Problem


---

## Project Overview

This project leverages a dataset of over 10,000 records from Zomato to analyze Sydney's restaurant landscape in 2018. The analysis covers restaurant attributes such as ratings, costs, locations, cuisines, and more, aiming to understand patterns and predict restaurant ratings using machine learning models. Visualizations, feature engineering, and predictive modeling techniques were utilized to address the business problem.

---

## Business Problem

To analyze and predict restaurant ratings based on features such as cost, votes, cuisine, and business type, enabling better insights into the relationship between price, location, and customer feedback.

---

## Machine Learning Goal

1. **Exploratory Analysis**:
   - Understand the distribution of restaurant costs, ratings, and locations.
   - Identify trends such as the correlation between cost and ratings.
2. **Predictive Modeling**:
   - Use regression to predict restaurant ratings.
   - Classify restaurants into high or low-rated categories using classification models.

---

## Methodology

### Data Preprocessing and Feature Engineering
1. **Handling Missing Values**:
   - Imputed missing values in numerical features (`cost`, `votes`) with the median.
   - Dropped rows with missing target variables (`rating_number`, `rating_text`).
   - Handled categorical features like `type` with placeholder values.

2. **Label Encoding**:
   - Ordinal encoding for `rating_text` from "Excellent" to "Poor".
   - Binary encoding for `groupon`.

3. **Log Transformation**:
   - Log transformation applied to skewed features like `cost` and `votes` to normalize the data.

4. **Feature Selection**:
   - Selected relevant features (`log_cost`, `log_votes`, `rating_text_encoded`) for modeling.

---

## Toolkits Used

- **Libraries**:
  - Data Manipulation: `numpy`, `pandas`
  - Visualization: `matplotlib`, `seaborn`, `plotly`, `geopandas`
  - Machine Learning: `scikit-learn`
  - Geospatial Analysis: `geopandas`, `plotly`
- **Frameworks**:
  - Linear and Logistic Regression
  - Random Forest, K-Nearest Neighbors, Support Vector Machines
  - Neural Networks and Stochastic Gradient Descent

---

## Results

### Exploratory Data Analysis (EDA)
1. **Top Locations**:
   - CBD, Surry Hills, and Parramatta had the highest number of restaurants.
2. **Cost Distribution**:
   - Majority of restaurants fall within the $0-$100 range.
   - "Excellent" rated restaurants tended to be more expensive.
3. **Cuisine Insights**:
   - Most common cuisines: Modern Australian and Café.
4. **Correlation Analysis**:
   - Higher costs and votes correlated with better ratings.

### Regression Results
1. **Linear Regression**:
   - Without Log Transformation: R² = 0.778, MSE = 0.047
   - With Log Transformation: R² = 0.822, MSE = 0.038
2. **Gradient Descent**:
   - R² = 0.822, MSE = 0.038

### Classification Results
1. Binary classification into "Class 1" (low-rated) and "Class 2" (high-rated).
2. Models Evaluated:
   - **Logistic Regression**: Accuracy = 100%
   - **Random Forest**: Accuracy = 100%
   - **SVM**: Accuracy = 100%
   - **KNN**: Accuracy = 100%
   - **Neural Network**: Accuracy = 100%

### Visualizations
1. Heatmaps and pair plots highlighted relationships between key features.
2. Geographic density maps showcased cuisine distributions in Sydney.

---

## Key Insights

1. **Cost and Rating**:
   - Higher costs generally indicate better ratings, as confirmed by statistical tests and regression analysis.
2. **Location Trends**:
   - Central areas like CBD have a higher density of restaurants.
3. **Cuisine Preferences**:
   - Certain cuisines dominate in popularity, such as Café and Modern Australian.

---

## Future Work

1. **Addressing Imbalanced Datasets**:
   - Use advanced techniques like SMOTE or class weighting to handle dataset imbalances.
2. **Feature Enhancements**:
   - Include temporal data or customer demographics to enrich the analysis.
3. **Hyperparameter Optimization**:
   - Optimize models using grid search or Bayesian optimization.
4. **Interactive Tools**:
   - Extend geographic visualizations to interactive dashboards for better business insights.

---

## Conclusion

This project demonstrated the effectiveness of combining data preprocessing, exploratory analysis, and predictive modeling to derive actionable insights from restaurant data. While regression models predicted ratings effectively, classification models showed perfect accuracy for binary classification tasks. Future enhancements can further refine predictions and insights for real-world applications.
