## Project Objective
The insurance company "Secure Tomorrow" aims to address several machine learning tasks to enhance their operations. The project focuses on:
- Finding similar clients for marketing purposes.
- Predicting whether a new client will receive an insurance payout.
- Predicting the number of insurance payouts a new client might receive using linear regression.
- Protecting client personal data while maintaining the integrity of machine learning models.


## Project Structure and Steps
**1. Load the Data:** The dataset insurance_us.csv was loaded to begin preprocessing and analysis.

**2. Preprocessing and Data Exploration:**
- Verified data quality: checked for missing values, outliers, and data types.
- Renamed columns for consistency and clarity.

**3. Specific Tasks:**
- Task 1 - Finding Similar Clients:
  - Used K-Nearest Neighbors (KNN) to find clients with similar profiles for targeted marketing strategies.
- Task 2 - Classification Model for Payout Prediction:
  - Developed a classification model to predict the likelihood of a client receiving an insurance payout, comparing model performance to a dummy classifier.
- Task 3 - Regression Model for Predicting Payouts:
  - Created a regression model to predict the number of insurance payouts a client is likely to receive.
- Task 4 - Data Masking:
  - Applied data obfuscation techniques to protect client information while ensuring the machine learning model's performance remains unaffected.


## Tools and Techniques Utilized

- **Data Preprocessing:** Pandas, NumPy
- Exploratory Data Analysis (EDA): Descriptive statistics, data visualization using Seaborn
- **Machine Learning Models:**
  - Classification: Scikit-learn's K-Nearest Neighbors, Decision Trees, and Logistic Regression
  - Regression: Linear Regression
- **Data Transformation:** Applied feature scaling and categorical encoding.
- **Data Privacy:** Data obfuscation techniques to ensure privacy without compromising model accuracy.

## Specific Results and Outcomes

**1. Data Overview and Quality Check**
- The dataset was thoroughly examined and contained the following features: Gender, Age, Salary, and Number of family members.
- Target Variable: Number of insurance payouts a client received over the past five years.
- The data was clean, with no missing values, duplicates, or significant anomalies. Each feature was validated for its type, range, and relevance for modeling.

**2. Task: Finding Similar Clients**
- **Objective**: Help marketing efforts by identifying clients with similar profiles.
- **Method**: Implemented K-Nearest Neighbors (KNN) to find clusters of clients with similar characteristics.
- **Results:**
  - Successfully identified clusters of clients with similar profiles based on age, salary, gender, and family size.
  - This similarity analysis allowed for better-targeted marketing strategies, helping to personalize offers and promotions.

**3. Task: Predicting Insurance Payout Probability**(Classification)
- **Objective**: Predict whether a client is likely to receive an insurance payout.
- **Models Tested:**
  - **Decision Tree Classifier**: Provided a basic understanding of the feature interactions and was used as an interpretable model.
  - **Logistic Regression**: Offered a probabilistic perspective on payout likelihood and served as a baseline for performance.
  - **K-Nearest Neighbors (KNN)**: Evaluated for its ability to identify similar patterns from historical data.
- Model Performance:
  - **F1-Score**: Each model's F1-score was evaluated to measure the balance between precision and recall.
    - **Decision Tree**: Achieved an F1-score of around 0.62.
    - **Logistic Regression**: Slightly lower F1-score of 0.58, indicating moderate performance in predicting payouts.
    - **KNN:** F1-score was around 0.60, showing balanced performance between false positives and false negatives.
  - **Baseline Comparison**: All models significantly outperformed the dummy classifier, which had an F1-score near 0.5 (random guessing).
- **Outcome:** The Decision Tree emerged as the most effective model for classifying clients likely to receive insurance payouts.

**4. Task: Predicting the Number of Insurance Payouts **(Regression)
- **Objective**: Predict the exact number of insurance payouts a client might receive.
- **Model Used:** Linear Regression was employed to predict the continuous target variable, focusing on the relationship between client features and payout amounts.
- **Performance Metrics:**
  - **Mean Absolute Error (MAE)**: Around 1.5 payouts, indicating the average error between predicted and actual payout numbers.
  - **R-Squared Value (R²)**: Approximately 0.55, suggesting that over half of the variance in the number of payouts could be explained by the client features in the model.
- **Outcome**: The linear regression model effectively provided estimates for the number of insurance payouts, allowing for better risk assessment and financial planning for the insurance company.

**5. Task: Data Masking and Privacy Preservation**
- **Objective**: Protect sensitive client information without compromising model performance.
- **Approach**:
  - Applied a data obfuscation algorithm that transformed personal data while preserving the underlying relationships between features.
  - Ensured that masked data remained useful for machine learning model training.
- **Validation**:
  - Trained the regression model using the obfuscated data and compared its performance to the model trained on the original data.
  - **Result**: The F1-score and regression metrics were nearly identical before and after obfuscation, confirming that data privacy was successfully achieved without degrading model accuracy.

6. Key Insights and Observations
- **Marketing Segmentation:** KNN clustering provided actionable insights into client segments, aiding targeted marketing strategies.
- **Classification Accuracy:** Decision Tree classifiers showed the best performance for predicting the likelihood of payouts, providing actionable predictive power for the insurance company.
- **Accurate Regression Estimates:** Linear regression was effective in predicting the number of payouts, with performance metrics indicating a reasonably high degree of accuracy.
- **Privacy Without Compromise:** Data obfuscation did not reduce the model's predictive capabilities, proving that privacy-preserving transformations can be effectively applied to sensitive data.


## What I Learned from This Project

- **Machine Learning Pipeline**: Enhanced skills in developing end-to-end machine learning pipelines, from data preprocessing to model evaluation.
- **Feature Engineering and Selection**: Gained experience in selecting important features and handling different data types for modeling.
- **Classification and Regression Analysis**: Improved understanding of applying classification for binary outcomes and regression for continuous predictions.
- **Data Privacy and Security:** Developed and applied data masking techniques that protect client information while ensuring model utility.
- **Model Evaluation and Validation:** Learned to evaluate models effectively using metrics like F1-score and comparing models against baselines.