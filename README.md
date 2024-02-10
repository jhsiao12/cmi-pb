

### Overview
This project is part of the 2nd CMI-PB Prediction Challenge (https://www.cmi-pb.org/blog/prediction-challenge-overview/)
It involves the analysis of pertussis vaccine immune response data, with a specific focus on predicting and ranking IgG-PT-D14-titer and IgG-PT-D14-titer fold change values. Analysis using various machine learning models.

#### Task 1.1: 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jhsiao12/cmi-pb/HEAD?labpath=CMI_Task1.ipynb)


#### Task 1.2: 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jhsiao12/cmi-pb/HEAD?labpath=Task1_peng_comment.ipynb)

### Project Structure
1. **Data Loading and Cleaning**
The project begins with loading data from data related to plasma antibody titers, specimens, and subject information for multiple years (2020, 2021).
The prediction data is from dataset of 2022.
The data is cleaned using specific functions (clean_df_subject, clean_df_specimen, clean_df_titer) to handle missing values and extract relevant information.
2. **Data Merging and Feature Engineering**
The cleaned data is merged based on common identifiers, creating a comprehensive dataset for training and prediction.
Feature engineering is applied to create new columns such as 'IgG-PT-D0-titer' and 'actual_boost_day_on_D14' for training data, and 'actual_boost_day_on_D14' for prediction data.
3. **Model Training**
Machine learning models including Random Forest, Linear Regression, Support Vector Regression, Gradient Boosting, Lasso Regression, Ridge Regression, ElasticNet, Decision Tree, and K-Nearest Neighbors are trained using the training dataset.
Randomized Search Cross-Validation is used to find the best hyperparameters for each model.
4. **Model Evaluation**
The trained models are evaluated on a test dataset using R-squared as the performance metric.
Feature importance is assessed using a Random Forest Regressor.
5. **Best Model Selection**
The model with the highest R-squared value is selected as the best model for making predictions on new data.
6. **Making Predictions on New Data**
The best model is used to make predictions on a new dataset for the 'IgG-PT-D14-titer' and 'IgG-PT-D14-titer-FC' values.
7. **Result Presentation**
The predicted 'IgG-PT-D14-FC' values are presented along with additional subject information.
The results are ranked based on the 'IgG-PT-D14-FC' values.
8. **Output**
The final results are saved to a TSV file for reporting.


### Getting Started
To run this project locally, follow these steps:
Install the required dependencies listed in the requirements.txt file using the following command:

```bash
pip install -r requirements.txt
```

When pushing commits format python code using 



### Dependencies
* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
