### Description:

- **Data Cleaning:**
  - Cleaned the "education" column to standardize values.
  - Dropped unnecessary columns that didn't directly relate to an individual's salary, such as "relationship" and "marital-status".
  
- **Exploratory Data Analysis (EDA) and Feature Selection:**
  - Visualized correlations and observed that "race" and "sex" had low positive correlation with income, so "race" was dropped.
  - Planned to work on the "sex" column during feature importance analysis to determine its relevance.

- **Encoding Categorical Variables:**
  - Applied label encoding on categorical columns to prepare data for modeling.

- **Handling Class Imbalance:**
  - The target variable was biased towards class 0 (low-income group). Oversampled the minority class to balance the dataset.

- **Feature Importance Analysis:**
  - Identified top important features as "age", "education", "capital-gain", "hours-per-week", and "occupation".
  
- **Scaling:**
  - Standard scaled the independent variables to ensure consistent feature magnitude.

- **Initial Model Creation:**
  - Trained a **Random Forest model**.
  - Achieved **Accuracy: 0.8428**.

- **Sex-based Income Distribution Check:**
  - Conducted a separate income distribution check for males and females:
    - **Male Count:** 4387, **Female Count:** 2126.
    - **Male Accuracy:** 0.7948, **Female Accuracy:** 0.8960.
  - Observed bias towards males as there were fewer female workers.

- **Final Model:**
  - Addressed bias in the income data using resampling techniques and applied stratification for the "sex" column.
  - Performed standard scaling again, excluding the binary "sex" column.
  - Trained a final **Random Forest model** with **Accuracy: 0.8412**.
  - Balanced the target variable: **Income 0 count:** 7382, **Income 1 count:** 7450.

- **Model Saving and Testing:**
  - Saved the scaler and classifier using **joblib** for future use.
  - Tested the model on new random data and obtained accurate predictions.
