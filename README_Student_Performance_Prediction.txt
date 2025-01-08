
# Student Performance Prediction

This project aims to predict student performance (Exam Score) using various machine learning models based on the dataset provided. Below are the detailed steps followed in the analysis, the performance comparison of models, and the final selected model.



## Steps Followed:

1. Data Loading:
Make sure to upload the StudentPerformanceFactors.csv in the Google Colab files before running the code.
   - Loaded the dataset `/content/StudentPerformanceFactors.csv` using pandas.
   - Previewed the dataset to understand its structure.

2. Data Preprocessing:
   - Handled missing values (if any) by imputing or dropping as necessary.
   - Encoded categorical features using one-hot encoding for multi-class variables and label encoding for binary variables.
   - Normalized numerical features to ensure uniform scaling for machine learning models.

3. Feature Engineering:
   - Extracted and prepared independent features (`X`) and the target variable (`y` - Exam Score).

4. Train-Test Split:
   - Split the dataset into training (70%) and testing (30%) subsets for model evaluation.

5. Model Selection:
   - Trained the following models:
     - Linear Regression
     - Random Forest
     - Decision Tree
     - XGBoost
     - LightGBM
     - Support Vector Regression (SVR)
   - Evaluated each model based on the following metrics:
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - Root Mean Squared Error (RMSE)
     - R² Score

6. Model Performance Comparison:
   - Metrics from the trained models:
     ```
               Model       MAE        MSE      RMSE  R2 Score
     1                SVR  0.681716   3.457887  1.859540  0.748334
     2           LightGBM  0.862872   3.763675  1.940019  0.726078
     3  Linear Regression  1.020321   4.277985  2.068329  0.688647
     4      Random Forest  1.166309   4.688166  2.165217  0.658794
     5            XGBoost  1.030270   4.854658  2.203329  0.646676
     6      Decision Tree  1.874433  13.141200  3.625079  0.043579
     ```

7. Model Selection:
   - Based on the metrics, SVR (Support Vector Regression) was selected as the final model because:
     - It had the lowest MAE, MSE, and RMSE.
     - It achieved the highest R² score (0.7483), indicating it explains ~75% of the variance in Exam Scores.

8. Final Output:
   - The SVR model is recommended for predicting student performance as it demonstrated superior accuracy and lower error rates compared to the other models.

---

## Recommendations:
- Use SVR for predicting student performance in this dataset.
- Explore hyperparameter tuning for SVR and other top-performing models (LightGBM) to further optimize their performance.
- Analyze feature importance using SVR or other methods (e.g., SHAP) to understand the most impactful predictors of Exam Scores.

---

## Prerequisites:
- Python 3.7 or above
- Libraries: pandas, numpy, scikit-learn, xgboost, lightgbm, matplotlib

---

## Usage:
1. Clone or download this repository.
2. Upload the dataset (`StudentPerformanceFactors.csv`) to your working directory.
3. Execute the script in Google Colab or a Jupyter Notebook to reproduce the analysis.

---

