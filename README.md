# A-Python-Project-On-The-Effect-Of-Covid-19-On-People-With-Multiple-Sclerosis
In this project, I critically analyzed and visualized the effect of covid-19 on people with multiple sclerosis. I also constructed a machine learning model capable of making predictions and forecasting trends as regards covid-19 and multiple sclerosis using logistic regression.

Dataset

The dataset for this project was extracted from the physionet.org database. It is a patient level dataset which consist of 1141 rows and 47 columns. Each of the row
represents the record of an individual with multiple sclerosis. To ensure that the data complied with GDPR policies, a de-identification process was performed to maintain
anonymity. The features of the dataset categorically represents; the patient information, covid-19 specific information, multiple sclerosis specific information, comorbidities and other health information. Below is a description of some of the important features of the dataset

Patient Information:
- secret_name: A unique identifier for each patient, anonymized to maintain confidentiality, the ‘p_’ or ‘c_’ represents patient or clinician reported respectively
- age_in_cat: grouped into categories 0-3, where ‘0’ represents ages less than 18 years, ‘1’, for ages between 18 and 50 years, ‘2’, ages between 21 and 70 years, then
category ‘3’ for ages above 70 years.
- sex: this represents the binary classification of patients gender into male or female.
  
COVID-19 Specific Information
- covid19_confirmed_case: this column has two unique values; ‘yes’ and ‘no’ which confirms the patient’s covid-19 diagnostic status.
- covid19_ventilation: this column contains ‘yes’ and ‘no’ which indicates wether the patient used a ventilator or not
- covid19_outcome_recovered: this column contains ‘yes’, ‘no’ and ‘not_applicable’. It indicates if the patient recovered from covid-19 or not.
  
Multiple Sclerosis (MS) Specific Information
- ms_type2: this column represents the type of MS. It has three unique entries, ‘relapse_remitting’, ‘progressive_ms’ and ‘other’ which stands for other types of MS
that are not the both already mentioned.

Other Health Information
- bmi_in_cat2: this column represents the patient’s body mass index. There are two unique entries, ‘overweight’, which indicates patients with BMI values above of
30kg/m2 and ‘not_overweight’ for BMI values less that 30kg/m2.

Analysis and Result

Dataset was cleaned by handling missing values(There were loads of them) and dropping some values. The cleaned data was analyzed and visualized to explore the relationship between the features (note: some visualizations were done on tableau).

Logistic Regression Model

For the prediction  model, the 'covid19_outcome_recovered' column was chosen as the target variable for the regression analysis. The column has three unique values; ‘Yes’, ‘No’, and ‘Not Applicable’. For the purpose of this regression, the ‘Not applicable’ value was filtered out since it
represents unknown response and will not add any value to the regression result. PCA method was employed for feature extraction. On training, the model achieved a great accuracy of 98%, and a very excellent Precision, Recall and F1 score for both categories of the target variable, indicating the model's tendency to effectively identify
recoveries based on  provided data characteristics.

Limitations

One of the biggest challenges of this project is related to the quality of the data. Having a dataset with a significant amount of missing values and inconsistency in data collection can lead to misleading analysis outcome. Another challenge encountered was because of the existence of class imbalance. Also model selection and tuning, considering the nature of the dataset, choosing the right model and tuning hyperparameters are critical and can be time-consuming, requiring a balance between model complexity and performance.

Summary

In summary, the effects of COVID-19 on MS patients are influenced by a complex interplay of various factors such as; demographic factors (age, BMI), the level of disability (EDSS score), and medical treatments (DMT), etc. No single factor alone seems to dictate outcomes, highlighting the need for a holistic approach in managing MS patients during the pandemic. Generally, the data emphasizes the need for ongoing research and careful management of MS patients during health crises like the COVID-19 pandemic. It also points to the importance of considering a range of factors when assessing risk and outcomes for these patients. This understanding can help in better preparing and protecting vulnerable populations in future health emergencies.
