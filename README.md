# Heart Disease Detection

This project uses classical machine learning to predict the presence of heart disease from clinical measurements in the popular UCI heart-disease dataset (303 patients, 13 features + target).
## Dataset

- File: `heart disease.csv`
- Target column: `target` (1 = heart disease, 0 = no disease)
- Features: age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting ECG, max heart rate, exercise-induced angina, ST depression (`oldpeak`), slope, number of major vessels (`ca`), and thalassemia type. [web:62]

## Methods

1. Load and explore the dataset in `Heart data.ipynb`.
2. Split into features `X` and target `y` using `target` as the label.
3. Perform a stratified train–test split (80% train, 20% test) with `random_state=42`.
4. Standardize features using `StandardScaler`.
5. Train two models on the scaled data:
   - Logistic Regression
   - Random Forest classifier
6. Evaluate both models on the test set using accuracy, precision, recall, F1-score, and a confusion matrix (for Random Forest). [file:102][web:71]

## Results

On the held-out test set:

- Logistic Regression: Accuracy **0.803**, Precision **0.769**, Recall **0.909**, F1-score **0.833**
- Random Forest: Accuracy **0.820**, Precision **0.762**, Recall **0.853**, F1-score **0.853**

The Random Forest achieves slightly higher overall F1-score, while Logistic Regression achieves higher recall. [file:102]

## How to run

git clone https://github.com/Islam-DS/Heart_Disease_Data.git
cd Heart_Disease_Data
pip install -r requirements.txt
jupyter notebook


## Project summary

Built and compared Logistic Regression and Random Forest models on a clinical heart-disease dataset, using stratified train–test splits, feature scaling, and multiple evaluation metrics to achieve strong test performance and interpret model trade-offs.
