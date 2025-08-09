# CodeAlpha_Credit_Disease_prediction
Modular ML pipeline for disease prediction using SVM. Covers heart disease, breast cancer, and diabetes datasets with reusable functions for cleaning, encoding (binary, ordinal, one-hot), scaling, and model evaluation. Built for clarity, flexibility, and medical data analysis.
🧠 Multi-Disease Prediction System Using SVM
This project provides a modular and scalable machine learning pipeline to predict the likelihood of heart disease, diabetes, and cancer using Support Vector Machines (SVM). It includes preprocessing, training, evaluation, and single-patient prediction capabilities.

📁 Project Structure
├── disease_svm.py         # Core class for training and prediction
├── data/                  # Folder containing CSV datasets
│   ├── heart.csv
│   ├── diabetes.csv
│   └── cancer.csv
├── notebooks/             # Jupyter notebooks for experimentation
├── README.md              # Project documentation



⚙️ Features
- 🔄 Unified class DiseaseSVM to handle multiple diseases
- 🧼 Modular preprocessing (encoding, scaling, imputation)
- 📊 Model evaluation (accuracy, classification report)
- 🧍 Single-patient prediction with automatic feature alignment
- 🔌 Easily extendable to other diseases or models

📦 Requirements
Install dependencies using pip:
pip install pandas scikit-learn numpy



🚀 How to Use
1. Prepare Your Data
Each dataset should be a CSV file with features and a target column (target, Outcome, or similar). Example:
Age,Gender,Blood Pressure,Cholesterol Level,...,target
58,1,140,250,...,1


2. Train Models
from disease_svm import DiseaseSVM

svm_system = DiseaseSVM()

# Load and preprocess datasets
X_heart, y_heart = load_heart_data()
X_diabetes, y_diabetes = load_diabetes_data()
X_cancer, y_cancer = load_cancer_data()

# Train models
svm_system.fit('heart', X_heart, y_heart)
svm_system.fit('diabetes', X_diabetes, y_diabetes)
svm_system.fit('cancer', X_cancer, y_cancer)


3. Predict for a Single Patient
sample = pd.DataFrame([{
    'Age': 45,
    'Gender': 1,
    'Blood Pressure': 130,
    ...
}])

prediction = svm_system.predict('heart', sample)
print("Heart Disease Prediction:", prediction[0])



📈 Evaluation
Each model can be evaluated using accuracy, precision, recall, and F1-score. You can also visualize confusion matrices and ROC curves.

🧩 Customization
- 🔁 Swap SVC with other classifiers (e.g., RandomForestClassifier)
- 🧠 Add feature selection or hyperparameter tuning
- 🧪 Integrate cross-validation for robust evaluation
- 🌐 Deploy as a REST API using Flask or FastAPI

📚 License
This project is open-source and free to use under the MIT License.

Would you like me to generate a matching disease_svm.py template or add example visualizations to the README?
