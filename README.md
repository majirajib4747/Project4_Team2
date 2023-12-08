# Project 4 - UPenn Data Science Boot Camp

Group Members: Rajib Maji, Hannah Whang, Michael Cariello, Theresa Bravo, Nick O'karma, Stephen Smith, Arame Diasse.

## Alzheimer Detection and Comparison Between Different Models
Our goal aimed to employ machine learning techniques to predict the likelihood of an individual receiving a diagnosis of Alzheimer's disease. Our approach involved utilizing datasets containing medical data and patient details to create and train predictive models for patient diagnosis. By leveraging sophisticated machine learning algorithms, we aspired to develop a tool that could accurately forecast the probability of an individual being diagnosed with Alzheimer's. The core of our methodology lay in the careful curation and utilization of comprehensive datasets, integrating both medical information and patient-specific details. Through this innovative approach, our project sought to contribute to the advancement of predictive analytics in healthcare, particularly in the early diagnosis and intervention of Alzheimer's disease 

## Questions to Consider:

1. Given the data available, are there certain characteristics such as age, sex, or education that correlate with an Alzheimer diagnosis?
2. Is there a preferred diagnostic method?
3. Of the models that we create, what classifier is the most accurate?
4. What tests correlate with the diagnosis of Alzheimer’s according to the DSM?


## Early Detection of Alzheimer's Disease 

First, we tried to find out whether any early detection is feasible for Alzheimer / Dimentia. We had used a Dataset from [Kaggle]( https://www.kaggle.com/code/ahmedghobashi/detecting-early-alzheimer-s/input ) to find out which feature can be used to detect early Alzheimer. 

| Feature Descriptions  |
|---|
| Subject ID : Subject Identification Number  |
| MRI ID : MRI Exam Identification Number  |
| Group : Class of dementia - Nondemented and Demented  |
| Visit : Nos of Patient vision ( subject ID )  |
| MR Delay : MR Delay Time  |
| M/F : Sex  |
| Hand : Right or left handed  |
| Age : Age of the subject  |
| Education : Years of Education  |
| SES : Socio economic Status ( 1 - 5 )  |
| MMSE : Mini Mental State Examination  |
| CDR : Clinical Dementia Rating  |
| eTIV : Estimated Total Intracranial Volume  |
|  nWBV : Normalize Whole Brain Volume |

Definitely early detection is better so that, more clinical options can be tried on patients as well as Patient's family can be prepared early if they know patient might have Alzheimer in future. 
We had used Logistic regression Model to find out which patient might have early symptomops of Alzheimer. 
There are 3 features - Age , MMSE ( Mini Mental State Examination ) and CDR ( Clinical Dementia Rating ) - These 3 features have pretty good correlation with symptomatic Alzheimer ( Demented ). We had saved the Model and built a simple UI Screen to predit early detection of Alzheimer. This would be the most cost effective model to run for patient diagnosis. <br>

**Modules and description:**<br>
Supervised_RegressionModel_Alzheimer_Logistic regression.ipynb - Doing data fetch , data cleansing and model export<br>
final_model.pkl - Final Model pkl file <br>
column_names.pkl - Input features pkl file<br>
Flask_api_model_deployment.py - Flask API to predict the model <br>
UI_Predict.html - HTML Code to give inputs and predict the value. 

## Convolutional Neural Network

Next we explored supplementary image processing techniques using a dataset comprised of MRI brain scans. Our objective was to create a Neural Network that could determine if a new image of a MRI scan could lead to the diagnosis of Alzheimer's disease. A total of 6400 images were organized on Google Drive and catagorized into four groups: Moderate Demented, Mild Demented, Very Mild Demented, and Non Demented.  

The MRI dataset of patients diagnosed with Alzheimer's can be found [here.](https://www.kaggle.com/datasets/sachinkumar413/alzheimer-mri-dataset)
* Request access to [Google Drive folder](https://drive.google.com/drive/folders/1BM7i7OU4pHrukjwFYiMMQL0WyNlAlK0q?usp=drive_link) for images.
* Images were resized to 224 x 224.
* Preprocessing and loading of images was done for each category. 
* Data  was trained, tested, one hot encoded, and a CNN model was created. 
* Initial accuracy was 74%.
* Considerations: MRI scans can be costly to run. It can be difficult to explain neural networks because there are many parameters.

## Colored MRI Image Proccessing

Lastly, we used supervised learning to process colored images of [MRI scans.](https://www.kaggle.com/datasets/sachinkumar413/alzheimer-mri-dataset/data)
The data in two different ways:
    1. Alzheimer Detection: Whether the patient has the Alzheimer or not (non vs all other categories)
    2. Alzheimer Classifier: Define what stage the patient is in the Alzheimer.

The models that are going to be tested:
* PCA for Alzheimer Detection
* LDA for Alzheimer Detection
* SVM for Alzheimer Detection and Alzheimer Classifier
* CNN for Alzheimer Detection(VGG16) and Alzheimer Classifier(EfficientNetB0)

After evaluating all models, we found that Linear Regression was the most accurate model with an accuracy of 98%.

* Considerations: 
    * This is the most expensive model to run.

## Conclusions
	
**add here later!**


## Difficulties

1.Data Privacy and Ethics:
Dealing with sensitive medical data requires strict adherence to privacy regulations and ethical considerations. Ensuring compliance with data protection laws and obtaining proper consents can be challenging.
2.Dynamic Nature of Medical Data:
Medical data is dynamic, and the predictive patterns may change over time. Regular updates and adaptations to the model may be necessary to account for evolving trends and understandings in Alzheimer's diagnosis.
3.Ethical Use of Predictions:
Determining how predictions will be used and ensuring ethical implications are considered is essential. Preventing misuse and ensuring responsible deployment of the model is a challenge that requires careful planning
## Suggestions for the future

Take outputs of the models we created and feed them into a random forest model to see if accuracy improves.

Look at EEGs datasets and other pretrained models to compare model accuracy.

Develop an application enabling users to enter responses from the MMSE (Mini Mental State Examination), with the system generating corresponding suggestions.
