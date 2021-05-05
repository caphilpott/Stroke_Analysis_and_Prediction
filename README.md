# Stroke_Analysis_and_Prediction
### Use of Machine Learning and Tableau Dashboards to Help Predict Strokes and Understand Contributing Factors


### Select Stroke folder to review project files and access Heroku link 

## Executive Summary
Cerebrovascular accidents (strokes) in 2020 were the 5th leading cause of death in the United States. 
The objective of this activity was to develop a model which can reliably predict the likelihood of a stroke using patient input information.

## Hypothesis
A reliable predictive model can be developed if the data and stroke key attributes are correctly identified and prepared for the machine learning process.  The importance of features generated by the model selected will be compared against the stroke risk factors identified by the American Stroke Association.  If the attributes are correctly identified by the model, the hypothesis will be considered validated.

## Data Selection 
A dataset from Kaggle was selected for the machine learning process.  The data was reviewed to identify trends and cleanup requirements.  The primary data cleanup activities identified were to address “N/A” values associated with body mass index and “Unknown” smoker status.  The “N/A” values represented 3.9% of the dataset and were addressed by using the mean body mass index and assigning that to the “N/A” values.  The “Unknown” smoker status represented 30.4% of the dataset.  Literature review verified that “Unknown” values were considered an accepted data point and therefore the “Unknown” values were left as presented in the raw data. 

## Data Preparation
Review of the data identified most of the Yes/No type answers for personal health questions, including if the person had a stroke, were heavily biased to the “No” side.  To ensure an effective model learning process, Synthetic Minority Oversampling Technique (SMOTE) was used to synthetically balance the Yes/No results for stroke.  SMOTE selects samples in the minority class that are close and then draws lines between them. New sample points are located on these lines. Other data preparation steps included One-Hot Encoding. 

## Model Selection and Machine Learning 
Linear and Tree models were evaluated.  The criteria used to select the model was one that did not overfit the data and had the best overall performance for f1-scores and recall for the likelihood of a stroke.   After the evaluation process was completed, a Linear Model, LogisticRegression was selected.  The results were saved and tested against live data after the model selection and machine learning process was completed.

##  Hypothesis Validation
The live testing of data verified that a reliable predictive model could be created if the data and stroke key attributes are correctly identified and prepared for the machine learning process.  

