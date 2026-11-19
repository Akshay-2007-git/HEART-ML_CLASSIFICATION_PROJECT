# ❤️ HEART-ML_CLASSIFICATION_PROJECT

A Machine Learning project that predicts the likelihood of heart disease using Logistic Regression, with an interactive web application built using Streamlit.
## 🌐 Live Deployment

The Heart Disease Prediction application has been successfully deployed using **Streamlit Community Cloud**.

🚀 **Live Application:** [Heart Disease Prediction – Try it here](https://heartstrokepredictionbyakshay.streamlit.app/)

Users can access the application online and interact with the trained Logistic Regression model to generate predictions.

## 🚀 Project Overview

This project focuses on predicting the likelihood of heart disease based on various patient health parameters using Machine Learning classification techniques.

The project uses a heart disease dataset (`heart.csv`) for exploratory data analysis, data preprocessing, model training, and evaluation.

Multiple classification algorithms are trained and evaluated, and Logistic Regression is selected as the final model based on its performance.

The trained model is integrated into a Streamlit web application where users can enter medical parameters and receive an instant prediction.

## 🛠️ Technologies & Libraries Used

- **Python** – Programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **Scikit-learn** – Machine Learning algorithms and preprocessing
- **Logistic Regression** – Final classification algorithm
- **K-Nearest Neighbors (KNN)** – Classification
- **Naive Bayes** – Classification
- **Support Vector Machine (SVM)** – Classification
- **Decision Tree** – Classification
- **StandardScaler** – Feature scaling
- **Joblib** – Model saving and loading
- **Streamlit** – Interactive web application

## 📊 Dataset

The project uses `heart.csv` as the dataset for training and evaluating the Machine Learning models.

The dataset contains medical attributes that help identify patterns associated with heart disease.

### Input Features

| Feature | Description |
|---|---|
| Age | Age of the patient |
| Sex | Gender of the patient |
| ChestPainType | Type of chest pain |
| RestingBP | Resting blood pressure |
| Cholesterol | Cholesterol level (mg/dL) |
| FastingBS | Fasting blood sugar greater than 120 mg/dL |
| RestingECG | Resting electrocardiogram results |
| MaxHR | Maximum heart rate achieved |
| ExerciseAngina | Exercise-induced angina |
| Oldpeak | ST depression induced by exercise |
| ST_Slope | Slope of the peak exercise ST segment |

**Target Variable:** `HeartDisease`

- `0` – No heart disease
- `1` – Heart disease

## 🧠 Machine Learning Workflow

The following steps were performed during the development of this project:

1. **Dataset Loading:** Imported the heart disease dataset using Pandas.
2. **Exploratory Data Analysis (EDA):** Analyzed the dataset to understand feature distributions and relationships.
3. **Data Preprocessing:** Prepared the dataset for Machine Learning.
4. **Categorical Encoding:** Converted categorical features into numerical representations.
5. **Feature Scaling:** Applied StandardScaler to standardize numerical features.
6. **Train-Test Split:** Divided the dataset into training and testing sets.
7. **Model Training:** Trained multiple classification algorithms.
8. **Model Evaluation:** Compared models using Accuracy and F1-score.
9. **Model Selection:** Selected Logistic Regression based on its evaluation performance.
10. **Model Persistence:** Saved the trained model and preprocessing objects using Joblib.
11. **Web Application:** Integrated the trained model into Streamlit for interactive predictions.

## 📈 Model Performance

The following classification algorithms were evaluated:

| Model | Accuracy | F1-score |
|---|---:|---:|
| Logistic Regression | **86.96%** | **0.8857** |
| KNN | 86.41% | 0.8815 |
| Naive Bayes | 85.33% | 0.8683 |
| SVM | 84.78% | 0.8679 |
| Decision Tree | 78.26% | 0.8020 |

### Final Model: Logistic Regression

Logistic Regression achieved the highest accuracy and F1-score among the evaluated models and was selected for the Streamlit application.

## 🌐 Streamlit Web Application

The trained Logistic Regression model is integrated into an interactive Streamlit frontend.

### Application Features

- Interactive patient information form.
- Age selection using sliders.
- Medical parameter selection using dropdown menus.
- Automatic categorical feature alignment.
- Feature scaling using the saved StandardScaler.
- Instant heart disease prediction.
- Clear prediction results displayed through Streamlit.

### Prediction Workflow

1. User enters patient health information.
2. Input data is converted into a Pandas DataFrame.
3. Missing encoded columns are filled with zeros.
4. Features are arranged in the expected training order.
5. StandardScaler transforms the input data.
6. The trained Logistic Regression model generates a prediction.
7. The application displays the prediction result.

## 📁 Project Structure

```text
HEART-ML_CLASSIFICATION_PROJECT/
│
├── app.py              # Streamlit web application
│
├── heart.pkl           # Trained Logistic Regression model
├── scaler.pkl          # Fitted StandardScaler
├── columns.pkl         # Expected feature column names
│
├── Heart.ipynb         # Jupyter Notebook for EDA and model training
├── heart.csv           # Heart disease dataset
│
└── README.md           # Project documentation
```

### File Descriptions

| File | Purpose |
|---|---|
| `app.py` | Streamlit frontend and prediction logic |
| `heart.pkl` | Stores the trained Logistic Regression model |
| `scaler.pkl` | Stores the fitted StandardScaler |
| `columns.pkl` | Stores expected feature names and their order |
| `Heart.ipynb` | Contains EDA, preprocessing, model training and evaluation |
| `heart.csv` | Dataset used for model development |
| `README.md` | Project documentation |

## 💾 Model Persistence Using Joblib

The trained model and preprocessing objects are saved using Joblib.

```python
import joblib

joblib.dump(models['Logistic Regression'], 'heart.pkl')
joblib.dump(scaler, 'scaler.pkl')
joblib.dump(X.columns.tolist(), 'columns.pkl')
```

These objects are loaded in the Streamlit application:

```python
model = joblib.load("heart.pkl")
scaler = joblib.load("scaler.pkl")
expected_columns = joblib.load("columns.pkl")
```

This allows the application to generate predictions without retraining the model every time it runs.

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Akshay-2007-git/HEART-ML_CLASSIFICATION_PROJECT.git
```

### 2. Navigate to the Project Directory

```bash
cd HEART-ML_CLASSIFICATION_PROJECT
```

### 3. Install Required Dependencies

```bash
pip install streamlit pandas numpy scikit-learn joblib matplotlib seaborn
```

### 4. Run the Streamlit Application

```bash
streamlit run app.py
```

### 5. Open the Application

Open the following URL in your browser:

```text
http://localhost:8501
```

## ⚠️ Disclaimer

This application is developed for educational and Machine Learning demonstration purposes only.

The predictions are model-generated estimates and are not medical diagnoses. They should not replace professional medical advice, clinical evaluation, or consultation with qualified healthcare professionals.

## 👨‍💻 Author

**Akshay Chandra Abburi**

Machine Learning | Python | Data Science

### 🔗 GitHub Repository

[HEART-ML_CLASSIFICATION_PROJECT](https://github.com/Akshay-2007-git/HEART-ML_CLASSIFICATION_PROJECT)

---

⭐ If you find this project interesting, consider giving the repository a star!
