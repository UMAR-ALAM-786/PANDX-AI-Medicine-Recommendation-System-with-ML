#  *PANDx AI – Personalized Medical Diagnosis and Health Recommendation System*

Welcome to **PANDx AI**, an intelligent healthcare assistant designed to provide *accurate disease prediction* and *personalized health recommendations* based on user-input symptoms. Built with an integrated Flask web framework and powered by machine learning, PANDx aims to bridge the medical accessibility gap—especially in underserved and rural regions.

---

# Live post: https://www.linkedin.com/posts/umar-alam-khan_excited-ai-machinelearning-activity-7317358004100612098-wKII?utm_source=share&utm_medium=member_desktop&rcm=ACoAAD-syYsBKd9HWIEqgk_fRUjb1v5b9uRQhiU

---

## 🚀 *Project Highlights*

- 🔍 **95%+ Prediction Accuracy** using a trained Support Vector Classifier (SVC) on multi-disease datasets.
- 🩺 **30+ Diseases Diagnosed** from 100+ symptom inputs.
- 💊 **Tailored Recommendations**: Medicines, Precautions, Diet, Workout, and Disease Descriptions.
- 🌐 **Flask Web Interface** for real-time prediction and feedback.
- 🔒 **Privacy-first Approach** with no data storage—processed entirely in session.
- ⚡ **Fast & Lightweight**: Hosted locally or on cloud for instant access.

---

## 🛠️ *Tech Stack*

- **Frontend**: HTML, CSS, Bootstrap (via Flask templates)
- **Backend**: Python, Flask, NumPy, Pandas, Pickle
- **ML Models**: Scikit-learn (SVC classifier)
- **Data Handling**: CSVs for symptoms, diseases, medications, diets, workouts, and descriptions
- **Deployment Tools**: Flask Server (locally with `app.run(debug=True)`)

  
---

## Working Flow

### User Input
- Users enter one or more symptoms in a comma-separated format on the home page (`index.html`).

### Validation & Preprocessing
- Input is parsed and validated against a dictionary of over 130 known symptoms.
- The symptom string is transformed into a binary vector corresponding to the trained dataset.

### Disease Prediction
- The binary vector is passed to an SVC model loaded from `svc.pkl`.
- A single disease is predicted from a predefined list of 30+ diseases.

### Recommendations Engine
- Based on the predicted disease, the system retrieves:
  - Description
  - Top 5 medications
  - 4 precautionary measures
  - Diet recommendations
  - Suggested workout or exercise

### User Output
- All information is dynamically rendered on the result page.
- The output is relevant, concise, and tailored to the selected disease.

---

## Key Features

### Comprehensive Symptom Checker
- Accepts over 130 symptoms, each mapped to specific medical conditions.

### Multidimensional Output
- Provides not just disease name but actionable suggestions across treatment, lifestyle, and diet.

### Expandable Architecture
- Easily adaptable to add new diseases, symptoms, or ML models.

### Multi-Page Flask Routing
- Built-in routes for About, Contact, Blog, and Developer sections for future expansion.

---

## Example Use Case

**Input:**

**Output:**
- **Predicted Disease:** Malaria
- **Description:** Malaria is a mosquito-borne disease caused by a parasite.
- **Medications:** Artesunate, Chloroquine, Primaquine
- **Precautions:** Use mosquito nets, avoid stagnant water, take antimalarials
- **Diet:** Hydrating fruits, light carbohydrates, iron-rich foods
- **Workout:** Light walking, low-intensity physical activity

1. Disease Description
-Provides a concise medical overview of the predicted disease.
-Explains the cause, mechanism, and common symptoms to help users understand the condition in plain language.
-Information is sourced from the description.csv dataset and dynamically retrieved based on the model’s prediction.

2. Precautionary Measures
-Lists 4 actionable precautions tailored to the diagnosed disease.
-Helps prevent the condition from worsening and assists in early recovery or symptom management.
-Examples include lifestyle adjustments, hygiene practices, or environmental cautions.
-Data is extracted from precautions_df.csv.

3. Medications
-Recommends top medications commonly prescribed for the predicted disease.
-Medication data is mapped from medications.csv and includes non-branded names typically used in diagnosis-related treatment plans.
-The suggestions are informative and not prescriptive (meant to educate, not replace medical advice).

4. Workouts
-Suggests safe physical activities or workouts based on the nature of the disease.
-For chronic or recovery-phase illnesses, light exercises such as walking or breathing routines are proposed.
-Fetched from workout_df.csv to promote overall wellness and aid physical recovery.

5. Diet Recommendations
-Recommends a custom diet plan supportive of treatment and recovery.
-Includes food items to boost immunity, reduce inflammation, or restore lost nutrients.
-Pulled from diets.csv, this data is curated to align with the nutritional needs of the disease in focus.



---

## Developer Note

This system is built for **educational and research purposes only**. It is not intended as a substitute for professional medical advice. Accuracy and outputs depend on the quality and coverage of the dataset used. Continuous improvements are planned to enhance prediction and recommendation accuracy.

---

## Contributions & Future Scope

- Add support for multi-label classification (handling overlapping diseases).
- Integrate NLP for symptom extraction via voice or typed natural language.
- Deploy on cloud platforms like **Heroku**, **AWS**, or **Streamlit Cloud**.
- Expand dataset using anonymized crowd-sourced data to improve model learning.

---

## Contact

- **Email:** alamumar91@gmail.com  
- **Phone:** +91-7398032771  
- **LinkedIn:** [UMAR ALAM](https://www.linkedin.com/in/umar-alam-khan/)  
- **GitHub:** [UMAR-ALAM-786](https://github.com/UMAR-ALAM-786)

---

*Empowering health decisions through AI – because care should be accessible to all.*


---

## 📁 *Directory Structure*

```bash
PANDx_AI/
│
├── models/
│   └── svc.pkl                # Trained machine learning model
│
├── datasets/
│   ├── symtoms_df.csv         # Symptom-to-disease mapping
│   ├── precautions_df.csv     # Preventive measures for diseases
│   ├── medications.csv        # Recommended medicines
│   ├── diets.csv              # Diet recommendations
│   ├── workout_df.csv         # Suggested exercises/workouts
│   └── description.csv        # Disease descriptions
│
├── templates/
│   ├── index.html             # Main UI for user interaction
│   ├── about.html
│   ├── contact.html
│   └── developer.html
│
├── app.py                     # Main Flask backend
└── README.md



