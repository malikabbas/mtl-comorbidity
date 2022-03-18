# Comorbidity prediction of depressive and cardiometabolic disorders using multitask learning

## features_to_use.json
This file contains all considered exposome features mapped as values against their codes in UK Biobank dataset

## Data preprocessing.ipynb:
This file contains code for loading the dataset from csv file to its final stages. Main steps performed include:
1. Load the dataset from csv file and select only specified columns
2. Filter the columns that contain ICD9 and ICD10 codes for diabetes, depression and CVDs
3. Create 3 target features/columns named diabetes, depression and CVD and populate them by consolidating data from other columns
4. Remove the columns that are no more required
5. Replace -3 (Prefer not to answer) and -1 (do not know) with nan values
6. Split the dataset into Dataset A and Dataset B, because for 23 columns we have only limited data
7. Impute missing values
8. Encode categorical features as a one-hot numeric arrays
9. Save the dataframes as csv files

## model.ipynb
This file contains the code for MTL model devlopment and obtaining model performance evaluation metrics. Main steps performed include:
1. Loading dataset A and B
2. Feature selection using SKlearn's SelectKBest function
3. Obtain and plot score of selected best features
4. Develop and train the model
5. Plot the ROC and PR curves of predictions
