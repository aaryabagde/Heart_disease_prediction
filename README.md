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

## Dataset
The dataset is taken from Kaggle and contains 15000 rows and 
