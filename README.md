# Machine Learning Diabetes

## Selected Topic

Diabetes is a leading cause of disability and mortality in the US. One of the ways healthcare providers monitor blood sugar levels in patients is by taking a blood test to measure HbA1c percentage. HbA1c is a measure of glycated haemoglobin, or glucose(sugar) that is in the red blood cells of the body. Red blood cells have a 2-3 month life span, meaning that HbA1c is an indicator of blood glucose levels over 2-3 months. High HbA1c levels mean that the patient has had 2-3 months of high levels of blood sugar, which is correlated with higher instances of Diabetic complications. Using data from over 70,000 hospitalized diabetic patients nationwide, we are utilizing classification methods to predict whether HbA1c levels are within a normal range, or an abnormal (high) range, based on other health-related factors.

## Reason for topic selection

Most of the data are numeric and sufficient enough for the machine learning model to answer our question.

## Description of datasource

We are using data from the UCI Machine Learning Repository. This dataset spans diabetic hospital encounters nationwide between 1999 and 2008 (the dataset from the UCI Machine Learning Repository can be found [here](https://archive.ics.uci.edu/ml/machine-learning-databases/00296/)).

## Question we hope to answer

Using a machine learning classification model, can demographics, diagnoses, medications, and other related indicators be used to predict whether someone admitted to the hospital with diabetes will have a normal or abnormal (high) HbA1c level. 

## Communication protocols

We will meet asynchronously via Slack and Zoom together when needed.


## Notes of columns
- **Readmitted** Days to inpatient readmission. Values: “<30” if the patient was readmitted in less than 30 days, “>30” if the patient was readmitted in more than 30 days, and “No” for no record of readmission
- **Admission Type**: Integer identifier corresponding to 9 distinct values, for example, emergency, urgent,
elective, newborn, and not available 
- **Discharge Disposition** Integer identifier corresponding to 29 distinct values, for example, discharged to
home, expired, and not available
- **admission_source_id**: Integer identifier corresponding to 21 distinct values, for example, physician referral,
emergency room, and transfer from a hospital 
- **time_in_hospital**: Integer number of days between admission and discharge 


## Technologies that will be used:
### Hosting platform
```GitHub``` will be the code hosting platform.
### Data Reprocessing and Analysis
```Pandas``` will be used to explore, clean, and perform an analysis. 
### Database
```SQLAlchemy``` and ```SQLite``` are used for our database in our analysis.
### Machine Learning
```SciKitLearn``` and ```TensorFlow``` are the ML libraries we'll be using to create a classifier. Our training and testing setup is using an 70/30 train-test split ratio. The training set will then be fit into a Neural Network model and a Random Forest model to compare which method has the greatest accuracy.
### Dashboard
```Tableau``` will be used to create the dashboard to display our findings. 
- [Tableau-Intisar](https://public.tableau.com/app/profile/intisar3500/viz/ML-DiabetesClassification/Dashboard1?publish=yes).
- [Tableau-Minnie Raw data from UCI](https://public.tableau.com/views/ML-DiabetesClassification_16447097191460/Raw_Visualizations?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link).
- [Tableau-Minnie](https://public.tableau.com/views/ML-Diabetes_A1MEtformin/Dashboard3?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link).

## Machine Learning Analysis

**Description of preliminary data preprocessing**
- Removed the following columns
  - Non-beneficial ID column – would not add value to analysis (patient_nbr)
  - Columns with missing values greater than 50% were converted into “NA” before being dropped because there’s not enough data to contribute to significant analysis (weight, payer_code, max_glu_serum, medical_specialty).
  - Columns with outliers are checked and dropped, because outliers can spoil the and mislead the training process resulting in longer training times, less accurate models and ultimately poorer results. 
  - Columns with only 1 value – 7 diabetic medications were noted as not given to any of the patients in our database, so keeping these columns would not provide additional insight (acetohexamide, troglitazone, examide, citoglipton, glimepiride-pioglitazone, metformin-rosiglitazone, metformin-pioglitazone)

**Description of feature engineering and the feature selection, including their decision-making process**
- Target variable
  - HgA1c level (A1Cresult) was converted from 4 values (none, normal, >7, >8) to 2 values (≤ 7 or > 7)*
  - HgA1c level–normal (less than or equal to 7%) or high (greater than 7%)

- Feature variables: 
  - utilized Random Forest Model to rank feature importance in order and selected the top 8 features:
    - num_lab_procedures
    - num_medications	
    - time_in_hospital	
    - num_procedures	
    - number_diagnoses	
    - discharge_disposition_id	
    - admission_type_id	
    - admission_source_id

**Description of how data was split into training and testing sets**
- Training set at 70%, testing set at 30%

**Explanation of model choice, including limitations and benefits**
- Classification predictive modeling utilizing neural network and random forest models (supervised machine learning) for comparison
  - Neural Network Model: 3 hidden layers, activation function–relu (input), sigmoid (output)
    - Benefits: with a complex dataset with almost 50 feature variables, this model has a greater tolerance for messy data and detect complex, nonlinear relationships
    - Limitations: prone to overfitting and may not generalize well

**Description of how model is trained thus far, and any additional training that will take place**
- Generated Random Forest Model to rank feature importance
- Utilized PCA with marginally improved accuracy score

**Description of current accuracy score**


## Slides
Our slides were created using [Google Slides](https://docs.google.com/presentation/d/1W2DfvjoKXET1t2AdzyoIjnP3BIkupiBVizmdS_L6_j0/edit?usp=sharing).
