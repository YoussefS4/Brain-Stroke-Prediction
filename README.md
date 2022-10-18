# Brain Stroke Prediction
## Dataset Description
This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relavant information about the patient.

## Explanation of each column

- gender: "Male", "Female"
- age: age of the patient
- hypertension: 1 if the patient has hypertension, 0 otherwise
- heart_disease: 1 if the patient has any heart diseases, 0 otherwise
- ever_married: "No" or "Yes"
- work_type: "Private","Self-employed", "Govtjov" or "children"
- residence_type: "Rural" or "Urban"
- avg_glucose_level: average glucose level in blood
- bmi: body mass index
- smoking_status: "never smoked", "formerly smoked", "smokes" or "Unknown"
- stroke: 1 if the patient had a stroke, 0 otherwise

## More Information
- For BMI levels:
below 18.5 : you're in the underweight range
between 18.5 and 24.9 : you're in the healthy weight range
between 25 and 29.9 : you're in the overweight range
between 30 and 39.9 : you're in the obese range
- For glucose levels:
A fasting blood sugar level of 99 mg/dL or lower is normal
100 to 125 mg/dL indicates you have prediabetes
126 mg/dL or higher indicates you have diabetes

## Questions for Analysis

- Question 1: what is the relation between stroke and features?
- Question 2: Which age category is more likely to have hypertension?
- Question 3: Which age category is more likely to have heart disease?
- Question 4: Which gender is more likely to have hypertension?
- Question 5: Which gender is more likely to have heart disease?
- Question 6: Is smoking a factor for hypertension?
- Question 7: Is smoking a factor for heart disease?
- Question 8: Does high bmi levels can be a factor for hypertension?
- Question 9: Does high bmi levels can be a factor for heart disease?
- Question 10: Is marriage a factor for hypertension?
- Question 11: Is marriage a factor for heart disease?
- Question 12: Is there a relation between bmi and age?
- Question 13: Does work type can be a factor for hypertension and heartdisease?
- Question 14: Does BMI levels have a relation with avg_glucose_levels?

## Findings
- Females are more likely to have hypertension and stroke but Males are more likely to have heart disease
- People who have aged more than 40 are more likely to have hypertension, heart disease and stroke
- An unexpected result of smoking is that the "never smoked" category is more likely to have hypertension, heart disease, and stroke also the category that does not have hypertension and heart disease is more likely to have a stroke
- Marriage people are more likely to have hypertension, heart disease, and stroke :-)
- High levels of BMI can be a factor in hypertension, heart_disease, and stroke
- People with low and high levels of glucose both can get hypertension, heart disease, and stroke
- Getting old can cause an increase in BMI levels
- Increasing BMI levels can cause an increase of avg_glucose levels
- The dataset is imbalanced and will resolve this by sampling (Oversampling), so in this dataset, we will focus on AUC-ROC and Recall metrics because we don't want to misclassify any stroke patient as a non-stroke patient

# Modeling 
## The Algorithms used:

- Logistic Regression
      - Accuracy: 77.1% 
      - Precision: 75.3%
      - Recall: 80%
      - F1-score: 77%
      - AUC-ROC score: 84.5%
- XGB Classifier
      - Accuracy: 96.3% 
      - Precision: 93.2%
      - Recall: 100%
      - F1-score: 96.4%
      - AUC-ROC score: 99.3%
- Decision Tree Classifier
      - Accuracy: 97.6% 
      - Precision: 95.5%
      - Recall: 100%
      - F1-score: 97.7%
      - AUC-ROC score: 97.6%
- SVC
      - Accuracy: 77.4% 
      - Precision: 73.2%
      - Recall: 86.2%
      - F1-score: 79.2%
      - AUC-ROC score: 84.8%
- Extra Trees Classifier
      - Accuracy: 98.6% 
      - Precision: 97.3%
      - Recall: 100%
      - F1-score: 98.6%
      - AUC-ROC score: 99.8%
      
## Conclusion:
- Extra Trees Classifier Model performs the best with 100% Recall and 99.8% AUC score
- The model does not misclassify any stroke patient as a non-stroke patient, which is fascinating. We don't want any patient who is suffering from a stroke to be categorized as having a non-stroke and so not receive the necessary medical care
## Project Scope
- Data Wrangling 
- Exploratory Data Analysis (EDA)
- Data Visualization 
- Data Preparation
- Modeling

## Tools
- Programming Language: Python
- Libraries: Pandas, Numpy, Matplotlib, Seaborn, Sklearn
- Jupyter Notebook
