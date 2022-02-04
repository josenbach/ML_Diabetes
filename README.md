# Machine Learning Diabetes

## Selected Topic

Using data from over 70,000 hospitalized diabetic patients, we are utilizing classification methods to predict whether HbA1c levels are within a normal range, or an abnormal (high) range, based on other health-related factors.

## Reason for topic selection

Most of the data are numeric and are suitable for the machine learning model to answer our question.

## Description of datasource

We are using data from the UCI Machine Learning Repository. This dataset spans diabetic hospital encounters between 1999 and 2008 (the dataset from the UCI Machine Learning Repository can be found [here](https://archive.ics.uci.edu/ml/machine-learning-databases/00296/)).

## Question we hope to answer

Using a machine learning classification model, can demographics, diagnoses, medications, and other related indicators be used to predict whether someone admitted to the hospital with diabetes will have a normal or abnormal (high) HbA1c level. 

## Communication protocols

We will meet asynchronously via Slack and Zoom together when needed.

## List of Medicines for Reference
Unspecified Type
- chlorpropamide
- tolbutamide
- acarbose
- miglitol 
- tolazamide 
- insulin    

Type II
- metformin
- glyburide
- Repaglinide
- nateglinide
- glimepiride
- glipizide
- Pioglitazone
- rosiglitazone  
- glyburide-metformin
- glipizide-metformin

## Notes of columns
- **Readmitted** Days to inpatient readmission. Values: “<30” if the patient was readmitted in less than 30 days, “>30” if the patient was readmitted in more than 30 days, and “No” for no record of readmission
- **Admission Type**: Integer identifier corresponding to 9 distinct values, for example, emergency, urgent,
elective, newborn, and not available 
- **Dischard Disposition** Integer identifier corresponding to 29 distinct values, for example, discharged to
home, expired, and not available
- **admission_source_id**: Integer identifier corresponding to 21 distinct values, for example, physician referral,
emergency room, and transfer from a hospital 
- **time_in_hospital**: Integer number of days between admission and discharge 
## Technologies that will be used:
## Hosting platform
Github will be the code hosting platform.
## Data Reprocessing and Analysis
Pandas will be used to explore, clean, and perform an analysis. 
## Database
PostgreSQL will be uses for database storage and it will be integrated with **Tableau** to display the data. SQLite will be used for our analysis in our Python notebook.
## Machine Learning
SciKitLearn and TensorFlow are the ML libraries we'll be using to create a classifier. Our training and testing setup is using an 70/30 train-test split ratio. The training set will then be fit into a Neural Network model and a Random Forest model to compare which method has the greatest accuracy.
## Dashboard
Tableau will be used to create the dashboard.
