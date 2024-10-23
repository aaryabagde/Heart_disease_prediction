# Heart Disease Prediction

## Introduction

Heart disease remains a leading cause of mortality globally. Early prediction can significantly enhance treatment outcomes. This notebook aims to predict whether a patient has heart disease based on various health metrics.

## Dependencies

The following libraries are required to run this notebook:

- `numpy`: For numerical computations and array manipulations.
- `pandas`: For data manipulation and analysis.
- `scikit-learn`: For machine learning algorithms and evaluation metrics.

```python
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score
```

## DataPreProcessing and EDA
The dataset is downloaded from Kaggle. It has 13 features and  a target variable indicating if a person has a heart disease or not. The features are as follows:
| Feature     | Description                                                                                       |
|-------------|---------------------------------------------------------------------------------------------------|
| `Age`       | The age of the patient in years. Age is a significant risk factor for heart disease, with older individuals generally at higher risk.                             |
| `Sex`       | The sex of the patient, where 1 indicates male and 0 indicates female. This feature helps capture gender-related risk factors associated with heart disease.    |
| `cp`        | Chest pain type, with values ranging from 0 to 3. This feature categorizes the type of chest pain experienced, which can indicate the severity of heart conditions.    |
| `trestbps`  | Resting blood pressure (in mm Hg) measured when the patient is at rest. High blood pressure is a known risk factor for heart disease.                              |
| `chol`      | Serum cholesterol level (in mg/dl). High cholesterol levels can lead to the buildup of plaques in the arteries, increasing the risk of heart disease.              |
| `fbs`       | Fasting blood sugar level, where 1 indicates a blood sugar level greater than 120 mg/dl and 0 indicates less. High fasting blood sugar levels can indicate diabetes, which is a risk factor for heart disease. |
| `restecg`   | Resting electrocardiographic results, with values representing different heart conditions. This feature helps assess the electrical activity of the heart.       |
| `thalach`   | Maximum heart rate achieved during exercise. A higher maximum heart rate can indicate better cardiovascular fitness, whereas a lower maximum can signal potential issues.         |
| `exang`     | Exercise induced angina, where 1 indicates the presence of angina during exercise and 0 indicates its absence. This feature helps evaluate the heart's response to physical activity. |
| `oldpeak`   | ST depression induced by exercise relative to rest. This feature measures changes in the ST segment of the electrocardiogram, indicating potential ischemia.      |
| `slope`     | Slope of the peak exercise ST segment, indicating the type of response the heart has during exertion. Different slopes can indicate varying degrees of heart health.  |
| `ca`        | Number of major vessels (0-3) colored by fluoroscopy. This feature reflects the severity of coronary artery disease, with more vessels affected indicating higher risk.  |
| `thal`      | Thalassemia (a blood disorder), represented in categories (e.g., 1 = normal; 0, 2, 3 indicating various degrees of thalassemia). This can influence heart disease risk and overall health. |


Following EDA was conducted:
- **Dataset Structure**: A concise summary of the DataFrame is provided, including the number of entries, data types of each column, and non-null counts. This information helps identify any columns that may need further cleaning or processing.

- **Statistical Measures**: Descriptive statistics are generated for each numerical feature, including count, mean, standard deviation, minimum, maximum, and quartiles. This summary gives insights into the distribution and central tendency of the data.

- **Checking for Missing Values**: The presence of missing values across the dataset is checked, as this is crucial for ensuring data quality. Missing values can lead to inaccuracies in model predictions.

- **Target Variable Distribution**: Analyzing the distribution of the target variable (`target`) is essential to understand the balance between the two classes (heart disease present vs. absent). This analysis helps assess whether the data is imbalanced.

- **Visualizations**: Additional visualizations can be beneficial for EDA. Utilizing libraries like Matplotlib and Seaborn, histograms, box plots, and pair plots can be created to visualize distributions and relationships between features. For example, plotting the distribution of age among patients with and without heart disease can reveal trends.

- **Correlation Analysis**: Understanding how features relate to one another and to the target variable can provide insights for feature selection. A correlation matrix can help identify strong correlations, which can inform the choice of features for the predictive model.

## Model Training
The dataset is split into training and testing sets. The logistic regression model is trained on the training data.

## Results
The model achieves a training accuracy of approximately 85.12% and a testing accuracy of approximately 81.97%. Further improvements can be made by exploring different models and hyperparameter tuning.
