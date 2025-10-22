
# 🩺 Disease Prediction Web App

A **Flask-based Machine Learning web application** that predicts possible diseases based on the symptoms entered by the user.  
The system also provides **disease descriptions, precautions, medications, diet suggestions, and recommended workouts** to help users understand their condition better.

---

## 🚀 Features

- 🧠 Predict disease from given symptoms using a pre-trained ML model  
- 📋 Provides detailed disease **description**  
- 💊 Suggests suitable **medications** and **precautions**  
- 🥗 Recommends healthy **diet plans**  
- 🏋️‍♂️ Suggests relevant **workouts**  
- 🌐 Interactive and simple **Flask web interface**

---

## 🧩 Project Structure

```
Disease-Prediction-App/
│
├── app.py                     # Main Flask application
│
├── models/
│   └── svc.pkl                # Trained Support Vector Classifier (SVC) model
│
├── Dataset/
│   ├── symtoms_df.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── description.csv
│   ├── medications.csv
│   └── diets.csv
│
├── templates
│   └── index.html             # Frontend HTML page
│
├── static/                    # Optional folder for CSS, JS, and images
│
└── README.md                  # Project documentation

```

---

## ⚙️ Installation and Setup

Follow the steps below to run the project locally:

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Dhivya-ramasamy123/Personalized_Medicine_prediction.git
cd Personalized_Medicine_prediction
```

### 2️⃣ Create and activate a virtual environment
```bash
python -m venv venv
venv\Scripts\activate     # On Windows
# OR
source venv/bin/activate  # On Mac/Linux
```

### 3️⃣ Install dependencies
pip install flask numpy pandas scikit-learn

### 4️⃣ Run the Flask app
```bash
python app.py
```

### 5️⃣ Open in your browser  
Visit **http://127.0.0.1:5000/** to use the web app.

---

## 🧠 How It Works

1. The user enters symptoms (comma-separated) — e.g.  
   ```
   itching, skin_rash, fatigue
   ```
2. The app converts the symptoms into a binary vector using a symptom dictionary.
3. The trained **Support Vector Classifier (SVC)** model predicts the disease.
4. The helper function retrieves:
   - Disease description  
   - Precautions  
   - Medications  
   - Diet recommendations  
   - Workouts
5. The results are displayed on the web page.

---

## 📊 Machine Learning Model

- **Model Used:** Support Vector Classifier (SVC)  
- **Framework:** scikit-learn  
- **Input:** Binary vector of 132 symptoms  
- **Output:** Predicted disease label (e.g., Diabetes, Dengue, Malaria, etc.)

---

## 📁 Datasets Used

| File Name | Description |
|------------|--------------|
| `symtoms_df.csv` | Contains list of symptoms for training |
| `precautions_df.csv` | Contains precautions for each disease |
| `workout_df.csv` | Suggests exercises for diseases |
| `description.csv` | Short description of each disease |
| `medications.csv` | Suggested medicines |
| `diets.csv` | Recommended diet information |

---

## 🖥️ Example Input and Output

**Input:**  
```
itching, skin_rash, nodal_skin_eruptions
```

**Output:**  
- **Predicted Disease:** Fungal Infection  
- **Description:** A common skin infection caused by fungus.  
- **Precautions:** Keep the area dry, use antifungal creams, avoid tight clothing.  
- **Medications:** Ketoconazole, Clotrimazole  
- **Diet:** Avoid sugar-rich foods.  
- **Workout:** Light stretching.

---


