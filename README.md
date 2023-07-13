# Extended-Decision-Trees-Ensembles-and-Neural-Networks-prediction-project

In this project, you have to predict the length of stay (in days) of a patient that is entering an ICU (Intensive Care Unit) using decision tree and ensemble models.

The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

Each row of mimic_train.csv correponds to one ICU stay (hadm_id+icustay_id) of one patient (subject_id). Column LOS is the length of stay of this patient, equal to discharge time minus admit time. The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at mimic_patient_metadata.csv. Please don't use any feature that you infer you don't know the first day of a patient in an ICU.

Note that the main cause/disease of patient contidition is embedded as a code at ICD9_diagnosis column. The meaning of this code can be found at MIMIC_metadata_diagnose.csv. But this is only the main one; a patient can have co-occurrent diseases (comorbidities). These secondary codes can be found at extra_data/MIMIC_diagnoses.csv.

As performance metric, please use RMSE (root mean squared error).

Main tasks are:

Using mimic_train.csv file build a predictive model for LOS .
For this analysis there is an extra test dataset, mimic_test_los.csv. Apply your final model to this extra dataset and generate predictions following the same format as mimic_kaggle_los_sample_submission.csv. Once ready, you can submit to our Kaggle competition and iterate to improve the accuracy.