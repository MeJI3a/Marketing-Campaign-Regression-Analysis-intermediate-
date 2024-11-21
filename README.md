# Project 3: Marketing Campaign Regression Analysis

## Overview

This project explores marketing campaign data to understand and predict revenue based on various campaign performance metrics. By using regression techniques, we aim to identify key drivers of revenue and evaluate the effectiveness of marketing efforts. The project is divided into four stages: data cleaning, simple regression, multiple regression, and visualization of model performance.

---

## Project Structure

### **File 1: Data Cleaning**
- **Objective**: Prepare the marketing dataset for analysis.
- **Key Tasks**:
  - Handled missing values and removed duplicates to ensure data quality.
  - Converted the `c_date` column to datetime format for temporal analysis.
  - Verified column data types and saved the cleaned dataset as `cleaned_marketing.csv`.
- **Outcome**: A clean dataset containing **308 rows** and **11 columns** ready for regression analysis.

---

### **File 2: Simple Linear Regression**
- **Objective**: Establish a baseline model to predict revenue based solely on marketing spend (`mark_spent`).
- **Key Results**:
  - **R-squared**: 0.576 – The model explains 57.6% of the variance in revenue.
  - **RMSE**: $223,586.20 – Average prediction error for revenue.
  - **MAE**: $92,960.24 – Average absolute error between actual and predicted revenue.
- **Insights**:
  - A moderate relationship exists between marketing spend and revenue.
  - The model’s performance can be improved by incorporating additional predictors.

---

### **File 3: Multiple Linear Regression**
- **Objective**: Enhance the model by including additional predictors (`impressions`, `clicks`, and `leads`) to better explain revenue.
- **Key Results**:
  - **R-squared**: 0.603 – The model now explains 60.3% of the variance in revenue.
  - **RMSE**: $216,439.42 – Reduced prediction error compared to the simple regression model.
  - **MAE**: $89,750.88 – Improved absolute error.
- **Insights**:
  - Variables like `clicks` and `leads` significantly improve the model’s ability to predict revenue.
  - While the improvement is incremental, it highlights the importance of multiple marketing factors.

---

### **File 4: Visualizing Model Performance**
- **Objective**: Evaluate the regression model’s performance and visualize relationships between marketing variables and revenue.
- **Key Visualizations**:
  1. **Predicted vs. Actual Revenue**:
     - Most predicted values are close to the actual values, but some large outliers exist.
     - Suggests reasonable model accuracy with room for improvement.
  2. **Residual Analysis**:
     - Residuals are mostly random and close to zero, but higher errors occur at extreme revenue values.
     - Indicates a good fit for most data but struggles with higher revenue predictions.
  3. **Impact of Marketing Variables**:
     - **Positive Correlations**:
       - `mark_spent`, `clicks`, and `leads` show strong positive relationships with revenue.
       - Campaigns with higher clicks or leads tend to generate more revenue.
     - **Weak Correlation**:
       - `impressions` have a weaker impact, suggesting ad volume alone doesn’t drive revenue.
- **Insights**:
  - Variables like `clicks` and `leads` are critical drivers of revenue.
  - Future strategies should focus on optimizing these metrics for better ROI.

---

## Key Takeaways

1. **Drivers of Revenue**:
   - **Strongest Predictors**: Marketing spend, clicks, and leads.
   - **Weaker Predictor**: Impressions alone do not significantly impact revenue.
2. **Model Performance**:
   - The multiple regression model explains 60.3% of revenue variance, an improvement over the simple regression model.
   - Visualizations highlight areas for improvement, particularly for higher revenue predictions.
3. **Business Implications**:
   - Marketing efforts should prioritize optimizing spend to increase clicks and leads, as these are the most impactful factors.
   - Focusing on ad engagement rather than sheer volume (impressions) is likely to yield better results.

---

## Tools and Libraries

- **Python**: Data analysis and modeling.
- **Libraries**:
  - `Pandas` and `NumPy`: Data cleaning and manipulation.
  - `scikit-learn`: Regression modeling and evaluation.
  - `Matplotlib` and `Seaborn`: Data visualization.

---

## Future Work

1. **Feature Engineering**:
   - Explore additional features like campaign category or temporal patterns.
2. **Outlier Management**:
   - Investigate and handle outliers in revenue to improve model accuracy.
3. **Advanced Models**:
   - Experiment with non-linear models (e.g., decision trees, XGBoost) or regularization techniques.
4. **Optimization Insights**:
   - Use findings to build actionable recommendations for campaign strategies.

---

## Conclusion

This project demonstrates the application of regression techniques to marketing data, providing valuable insights into revenue drivers. By integrating predictive modeling with visual analytics, it offers actionable recommendations to optimize marketing strategies for better performance.
