# Hospital Readmissions Project

## Project Overview
This project analyzes hospital readmissions data to identify opportunities for improving hospital efficiency and reducing costs. The goals are to:
- Reduce hospital stay delays by targeting specific age groups.
- Cut medication waste by 15% by addressing over-prescription in readmitted patients.
- Predict readmissions with 80% accuracy using machine learning.

## Data Engineering
- **Data Cleaning:** Cleaned the dataset (`cleaned_readmissions.csv`) by removing null values, eliminating duplicates, and capping outliers to ensure data quality for analysis and modeling.
- **Data Aggregation:** Used SQL to compute average hospital stays by age group and average medication usage by readmission status.

## Data Analysis and Visualizations

### Hospital Stay Analysis
The bar chart below shows the average hospital stay by age group. Older patients (80-90: 4.79 days, 70-80: 4.57 days) have the longest stays, above the overall average of 4.40 days.

![Average Hospital Stay by Age Group]([Sheet 1.png](https://github.com/dm97764n/hospital-readmissions-project/blob/main/Sheet%201.png))

- **Recommendation:** Target the 80-90 and 70-80 age groups to reduce stays by 20% (e.g., 4.79 to 3.83 days for 80-90), saving approximately 1 day per patient.
- **Impact:** Reducing hospital stays for older patients could streamline operations, free up beds, and reduce delays.

### Medication Usage Analysis
The bar chart below reveals that readmitted patients use 16.37 medications on average, 6.6% more than non-readmitted patients (15.35).

![Average Medications by Readmission Status]([meds_by_readmission.png](https://github.com/dm97764n/hospital-readmissions-project/blob/main/Average%20Medications%20by%20Readmission%20Status.png))

- **Recommendation:** Reduce medication usage for readmitted patients by 15% (16.37 to 13.91 meds), saving ~2.5 medications per patient.
- **Impact:** This could cut waste, lower costs, and reduce over-prescription risks, aligning with the 15% waste reduction goal.

## Predictive Modeling
- **Readmission Prediction Model:** Built a logistic regression model to predict hospital readmissions using features like hospital stay duration, number of medications, lab procedures, diagnoses, and demographic flags. The model achieved an accuracy of 56% on the test set. While this is below the target of 80% accuracy, it provides a strong baseline. Future improvements could include adding more features (e.g., number of procedures, diabetes medication usage), trying ensemble methods like Random Forest, or performing hyperparameter tuning to reach the 80% goal.
