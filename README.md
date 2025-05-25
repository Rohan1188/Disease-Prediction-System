# Disease-Prediction-System
A Flask-based web application that predicts diseases based on user-input symptoms using a machine learning model (Random Forest). It also provides detailed information about the disease, including description, medications, precautions, workouts, and diets.


# 🧠 Disease Prediction System

A Flask-based web application that predicts diseases based on user-input symptoms using a machine learning model (Random Forest). It also provides detailed information about the disease, including description, medications, precautions, workouts, and diets.

## 🔍 Features

* ✅ Predicts disease based on multiple symptoms
* 📖 Returns disease description
* 💊 Suggests medications
* 🥗 Recommends diets
* 🧘‍♀️ Provides workout suggestions
* ⚠️ Lists precautionary measures
* 🧠 Auto-corrects misspelled symptoms using fuzzy matching

## 🛠️ Tech Stack

* **Frontend**: HTML + CSS (via Jinja2 templating in Flask)
* **Backend**: Python, Flask
* **ML Model**: Random Forest (trained and saved as `RandomForest.pkl`)
* **Datasets**: Kaggle-sourced CSVs (symptoms, description, medications, etc.)

## 📁 Folder Structure

```
├── main.py                    # Main Flask app
├── templates/
│   └── index.html             # Frontend UI
├── model/
│   └── RandomForest.pkl       # Trained model
├── kaggle_dataset/
│   ├── symptoms_df.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── description.csv
│   ├── medications.csv
│   └── diets.csv
```

## 🚀 How to Run

### 🔧 Requirements

Install required packages:

```bash
pip install flask pandas numpy scikit-learn fuzzywuzzy python-Levenshtein
```

### ▶️ Run the App

```bash
python main.py
```

Then open your browser and go to:
👉 `http://127.0.0.1:5000/`

## 📝 Usage

1. Enter your symptoms separated by commas.
2. Click on "Predict".
3. View the predicted disease and all relevant medical suggestions.

Example input:

```
fever, headache, joint pain
```

## 📊 Model

The app uses a **Random Forest Classifier** trained on a symptom-disease mapping dataset to predict the disease from input symptoms.

## 🤖 Spell Correction

The system uses `fuzzywuzzy` to auto-correct user-entered symptoms to handle typos and increase robustness.

## 📌 Note

* All data files must be placed in the `kaggle_dataset/` directory.
* Ensure the `model/RandomForest.pkl` exists.

## 📷 Screenshot
![image](https://github.com/user-attachments/assets/69f5f5c2-8116-4b7d-aeaf-25c55ebc44b7)

![image](https://github.com/user-attachments/assets/742826e9-ff2c-422a-8604-5c3734227351)


