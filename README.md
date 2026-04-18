# E-Cigarette and Healthy Habits Study
Team Members: Elizabeth Greenan, Nicholas Perry, & Kevin Wilson

## Project Details

### Background
This project uses data from the 2024 BRFSS Survey conducted by the CDC to evaluate whether an individual is more likely to use an e-cigarette based on their lifestyle choices.

### Question
Are those with healthier lifestyles less likely to use e-cigarettes than those who may have less healthy lifestyles?

### Hypothesis
We hypothesize a predictive model for e-cigarette usage can be built using health and lifestyle data because unhealthy habits frequently co-occur.

### Prediction
We predict that those with healthier living habits may be less likely to use e-cigarettes due to their desire to live the healthiest lifestyle.

## Dataset Details

### Data and Download
Due to the size of the file, the original dataset is not located in the repository, but the source data used can be downloaded here: https://www.cdc.gov/brfss/annual_data/annual_2024.html

The codebook from the CDC is located in the Documentation folder of the repository.

The data downloaded as a XPT (SAS Transport) file and imported into R using the haven package. Then, it was written as a .csv file. The code for this can be found in the Scripts folder of the repository.

### Response Variable
The response variable in this dataset is E_Cig_User (renamed from _CURECI3 in the BRFSS dataset). This is a binary response variable, where 0 represents a non e-cigarette user and 1 represents a current e-cigarette user. All missing data was removed from this variable.

### Predictor Variables
There are several predictor variables used for this analysis. They are categorized as demographic, mental health, physical health, lifestyle, and social determinant variables. A complete list can be found in the Data Dictionary, which is in the Reports folder of the repository. Note that several of the predictor variables have been renamed for improved readability.

### Analysis Plan

## Imputation
Multivariate Imputation by Chained Equations (MICE) was the imputation method chosen.

## Models
Elastic Net Logistic Regression with Ridge (unsupervised), Elastic Net Logisitc Regression with Lasso (supervised), and Random Forest will be the models used for this analysis. They will be trained on the cleaned, imputed, one-hot encoded, and scaled training dataset.

## Model Performance
When testing model performance, the imputed test set will be used and metrics such as precision, recall, F1-Score, and ROC curves will be used to analyze results and model performance.

