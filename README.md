# AI-Powered-System-for-Early-Detection-of-Cardiovascular-Event

## Background
Cardiovascular diseases (CVDs) remain the leading cause of morbidity and mortality in the US and globally. A major portion of the CVD events, such as stroke and Heart Attack, occur unwitnessed, delaying treatment and increasing the risk of death or disability. The delayed detection and management of these CVD events increases the cost of medical care which is associated with poor prognosis. However, timely detection and alerts to caregivers or emergency responders could help reduce treatment delays and facilitate a faster recovery. Artificial Intelligence (AI) offers the opportunity to leverage real-time monitoring data from wearable devices to detect major events and alert the caregivers and emergency services for prompt responses

<img width="1146" height="542" alt="image" src="https://github.com/user-attachments/assets/c1a3c9be-280e-4a46-8614-463997d1759d" />

## Objectives
Develop an AI-powered system for early detection of cardiovascular events (stroke & heart attack).
Implement automated alerts for caregivers and emergency responders to ensure a timely and effective response.
HYPOTHESES
Primary: An AI-powered system integrating real-time data from wearable devices can accurately detect early signs of cardiovascular events (e.g., stroke, myocardial infarction) with higher sensitivity and specificity >95%.
Secondary: Automated alert delivery to patients, caregivers, and emergency responders reduces the time-to-intervention for cardiovascular emergencies, thereby improving patient outcomes and survival rates.

## Dataset
The dataset is taken from Kaggle, which was extracted from MIMIC III. It consists of 23,468 samples. Features used include heart rate, blood pressure, SpO2, respiratory rate, and temperature. Target labels are 0 and 1, indicating the absence or presence of a CVD event, respectively.

<img width="2100" height="584" alt="image" src="https://github.com/user-attachments/assets/f47fd055-b04c-41f5-b08c-cca049cdc9a2" />

## Machine Learning Models
Logistic Regression: A good and computationally efficient baseline model for binary classification tasks.
Decision Trees: A simple ensemble algorithm noted for capturing non-linear relationships between features.
Random Forest: An ensemble method that combines multiple decision trees. This often leads to improved accuracy and robustness compared to a single decision tree.
Extreme Gradient Boosting: A gradient boosting algorithm known for its high performance and ability to handle complex datasets.
Train-Test Split and Cross Validation
Train-Test-Split: The data was split into training (80%) and testing (20%) sets using train_test_split with random_state=42 Cross-Validation:  To get a more robust evaluation of model performance by splitting the data into multiple folds and running the model on different combinations of these folds. This helps to reduce the impact of a single train/test split and provides a better estimate of how the model will perform on unseen data. A 10-fold cross-validation was used to validate the models adequately.

## Cross-Validation Results (10-fold)
Cross-validation confirmed the strong performance of the tree-based models (Decision Tree, Random Forest, and XGBoost) with mean ROC-AUC scores very close to 1.0000 and low standard deviations, indicating robust performance across different subsets of the data. Logistic Regression had the lowest ROC-AUC

<img width="979" height="707" alt="image" src="https://github.com/user-attachments/assets/e5713484-f21a-4c4c-a79c-dc51cc55b546" />

## Models Performance
Evaluation Metrics: Models were evaluated using Accuracy, Precision, Recall (Sensitivity), F1-score, ROC-AUC, and Specificity on the test set, and Mean ROC-AUC (CV) and Standard Deviation ROC-AUC (CV) from 10-fold cross-validation.

<img width="1095" height="805" alt="image" src="https://github.com/user-attachments/assets/2a9eec0a-c8ad-41a0-bcb1-0aeba12fec84" />

## Best Performing Models
Both Decision Tree and Random Forest models achieved perfect or near-perfect scores (1.0000) across most metrics on the test set, including Accuracy, Precision, Recall, F1-score, and ROC-AUC. XGBoost also performed exceptionally well

<img width="979" height="682" alt="image" src="https://github.com/user-attachments/assets/38bf69a7-15b0-4462-b81b-580847462c41" />

## Overfitting Analysis
Training accuracy and ROC-AUC scores were calculated for all trained models. The difference between training and testing scores for all models was found to be very small (less than 0.05 for both accuracy and ROC-AUC), indicating no significant overfitting.

<img width="979" height="417" alt="image" src="https://github.com/user-attachments/assets/407c10fe-957f-4a2d-be76-fb9842e870fc" /> <img width="926" height="381" alt="image" src="https://github.com/user-attachments/assets/644a2976-9737-45e2-8fe6-5fea4844ab38" />



## Correlation Heatmap
The correlation heatmap visualizes the pairwise correlations between the features in the dataset. Each cell in the heatmap represents the correlation coefficient between two features.
<img width="979" height="555" alt="image" src="https://github.com/user-attachments/assets/356d4e86-ed4e-41ea-ac56-81e122d7cd5d" />


## Conclusion
This research demonstrates that integrating AI-powered predictive modeling with wearable devices and interoperable health data systems can provide real-time detection of cardiovascular emergencies such as strokes and heart attacks. By linking patient-generated health data to a cloud-based AI engine and delivering timely alerts to patients, caregivers, and emergency responders, the system addresses a critical gap in early recognition of unwitnessed events
The proposed solution not only enhances patient safety and outcomes but also reduces delays in treatment, potentially lowering morbidity and mortality. Furthermore, the feedback loop into EHRs ensures continuous learning and system improvement, making the platform adaptive and scalable.
SIGNIFICANCE AND IMPACT
Quality of Care: Early detection and intervention directly translate into better recovery, reduce complications, and improve patient and caregiver satisfaction
Access to Care: As a digital safety net, the system ensures that a timely emergency response is available for vulnerable populations without robust social support.
Population Health Impact: By addressing the 25-36 % of unwitnessed strokes and up to 45% of silent MI, the system targets a substantial fraction of cardiovascular events.
Healthcare System Efficiency: Early interventions reduce the high costs associated with delayed treatment and complications
