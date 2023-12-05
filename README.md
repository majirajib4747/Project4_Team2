Project 4 - UPenn Data Science Boot Camp - Alzheimer detection and comparison between different models
Early Detection of Alzheimer 
First we tried to find out whether any early detection is feasible for Alzheimer / Dimnetia. We had used a Dataset from Kaggle ( https://www.kaggle.com/code/ahmedghobashi/detecting-early-alzheimer-s/input ) to find out which feature can be used to detect early alzheimer. Definitely early detection is better so that , more clinical options can be tried on patients as well as Patient's family can be prepared early if they know patient might have Alzhimer in future. 
We had used Logistic regression Model to find out which patient might have early symptomops of Alzheimer. 
There are 3 features - Age , MMSE ( Mini Mental State Examination ) and CDR ( Clinical Dementia Rating ) - These 3 features have pretty good correlation with symptomatic Alzheimer ( Demented ) . 
We had saved the Model and built a simple UI Screen to predit early detection of Alzheimer. 
Here is the Modules and description 
Supervised_RegressionModel_Alzheimer_Logistic regression.ipynb - Doing data fetch , data cleansing and model export
final_model.pkl - Final Model pkl file 
column_names.pkl - Input features pkl file
Flask_api_model_deployment.py - Flask API to predict the model 
UI_Predict.html - HTML Code to give inputs and predict the value. 
