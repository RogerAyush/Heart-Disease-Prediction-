# Heart Disease Prediction

This repo uses a Random Forest Classifier to predict heart disease with the Kaggle Cardiovascular Disease dataset (~70,000 records). It analyzes Age, Gender, Blood Pressure, Cholesterol, Resting Heart Rate, Blood Sugar, ECG Results, Smoking, and Exercise Habits to classify patients (1=disease, 0=no). Built in Python, it offers preprocessing, visualization, training, evaluation, and predictions.

## Features
- **Data Prep**: Processes `cardio_train.csv`, converts age, calculates BP, and adds placeholders for missing data.
- **Visuals**: Plots include data distribution and feature importance.
- **Model**: Trains on 20% data, tests on 80%, with ~73–75% accuracy.
- **Evaluation**: Shows accuracy, reports, and confusion matrix.
- **Prediction**: Predicts for new patients (e.g., 55-year-old male smoker).

## Setup
1. Clone: `git clone https://github.com/RogerAyush/HeartDiseasePrediction.git`
2. Install: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Get `cardio_train.csv` from [Kaggle](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset) and add it.
4. Run: `python heart_disease_prediction_full_with_viz.py`

--- Data Visualization ---

<img width="558" height="393" alt="image" src="https://github.com/user-attachments/assets/4e2c9771-0c77-42c5-8275-5b2e2868fb51" />
<img width="704" height="470" alt="image" src="https://github.com/user-attachments/assets/e42e014d-8e84-4ea3-82bb-6adb9471b89e" />
<img width="713" height="470" alt="image" src="https://github.com/user-attachments/assets/9d1477ed-79ef-491d-863f-6960413e6dea" />
<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/d2e1a703-5472-40b9-9e4e-539a207dc333" />
<img width="593" height="455" alt="image" src="https://github.com/user-attachments/assets/e5199a4d-f5ae-41cc-bcbe-004af1e033a5" />
<img width="878" height="795" alt="image" src="https://github.com/user-attachments/assets/3b845767-a89e-4cce-8772-ace1a3b8620b" />
<img width="951" height="547" alt="image" src="https://github.com/user-attachments/assets/9c48f372-1fbe-4123-b3bc-965ce8b2f3af" />

Model Accuracy: 72.91% on test dataset (80% of data)

Classification Report:
              precision    recall  f1-score   support

           0       0.71      0.78      0.74     27684
           1       0.75      0.68      0.71     27111

    accuracy                           0.73     54795
   macro avg       0.73      0.73      0.73     54795
weighted avg       0.73      0.73      0.73     54795

Feature Importance:
              feature  importance
2      blood_pressure    0.617575
0           age_years    0.206973
3         cholesterol    0.100811
5         blood_sugar    0.027813
8     exercise_habits    0.017404
1              gender    0.015751
7             smoking    0.013673
4  resting_heart_rate    0.000000
6         ecg_results    0.000000

New Patient Prediction:
Heart Disease: Positive
Probability: 84.83%

## Usage
Run the script to see visualizations, model metrics, and a sample prediction. Edit the `new_patient` dictionary to test different cases.

## Limitations
- Uses placeholders for missing features (resting heart rate, ECG).
- 80% test split reduces training data; consider 70–30.
- Future improvements: Add real data or a web interface.

## License
MIT License - Free to use with credit. See [LICENSE](LICENSE) for details.

## Security
Use a GitHub Personal Access Token (Settings > Developer Settings) for auth, not passwords. Store it securely.

Explore, tweak, and contribute to heart disease prediction!
