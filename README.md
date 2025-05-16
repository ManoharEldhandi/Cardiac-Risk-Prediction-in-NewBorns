# 🧬 A Machine Learning Approach Using Statistical Models for Early Detection

This project implements a web-based machine learning system that enables **early detection of cardiac arrest risk in newborns** based on vital signs and medical indicators. Built using **Django for the backend** and **MySQL for data persistence**, the solution integrates a robust **ML prediction engine** powered by **scikit-learn** to assist healthcare professionals in proactive risk assessment.

---

## 📦 System Requirements

- **Python 3.10+**
- **Django 4.0+**
- **pip3**
- **MySQL**
- **httpd (Apache via Homebrew)**
- **brew (for macOS service management)**

---

## 🔧 Installation - Required Packages

Install all required packages with the following command:
```bash
pip3 install django djangorestframework pandas numpy scikit-learn matplotlib seaborn xgboost imbalanced-learn joblib mysqlclient mariadb --break-system-packages
```

If you're using `sklearn`, you may need to:
```bash
export SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL=True
pip3 install sklearn --break-system-packages
```

---

## 🚀 Getting Started - How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/YourUsername/Cardiac_Early_Detection.git
cd Cardiac_Early_Detection
```

### 2️⃣ Start Backend Services

```bash
brew services start mysql
brew services start httpd
```

### 3️⃣ Create MySQL Database

```bash
mysql -u root -p
# Password: sqlpassword
```

Once inside MySQL:
```sql
CREATE DATABASE cardiac_detection;
USE cardiac_detection;
```

### 4️⃣ Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5️⃣ Run the Server

```bash
python manage.py runserver
```

### 6️⃣ Open in Your Browser

```
Visit http://127.0.0.1:8000/ to interact with the application.
```

---

## 🧪 Usage Workflow

```text
1. Register/Login as a remote user.
2. Navigate to the “Cardiac Arrest Prediction” module.
3. Fill in the health profile form:
   • Heart Rate
   • Respiratory Rate
   • Oxygen Saturation
   • Blood Pressure
   • Temperature
   • Glucose levels, etc.
4. Submit to receive real-time ML prediction.
5. Prediction outcome is logged in your history for later review.
```

---

## 🌟 Core Features

```yaml
✅ User Authentication System
✅ Dynamic Form-Based Medical Input
✅ Backend Integration with ML Model
✅ Uses Multiple Classifiers: 
   - Naive Bayes
   - Decision Tree
   - SVM
   - Logistic Regression
✅ Ensemble Voting Prediction Output
✅ Accurate Clinical Prediction with Preprocessed Data
✅ Admin Panel for Monitoring Users and Predictions
✅ Detailed Prediction Logs Stored in MySQL
```

---

## 🧠 Machine Learning Details

| Model               | Role                    | Description |
|--------------------|-------------------------|-------------|
| Logistic Regression| Baseline clinical model | Good for linearly separable classes |
| Decision Tree      | Nonlinear boundary logic| Easy to interpret medically |
| SVM                | High-dimensional support| Works well with small data |
| Naive Bayes        | Probabilistic classifier| Fast and efficient |
| Voting Classifier  | Final predictor         | Aggregates best results |

Each model is trained on a clean, structured dataset and evaluated with precision, recall, F1-score, and ROC-AUC metrics.

---

## 🛠️ Architecture Overview

```
[Frontend (Templates)]
     |
     v
[Django Views] <---> [Trained ML Model (.pkl)]
     |
     v
[MySQL Database]
```

---

## 📂 Folder Structure

```
Cardiac_Early_Detection/
├── remote_user/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
├── service_provider/
│   └── ...
├── manage.py
├── db.sqlite3 (initially)
└── static/
```

---

## 📊 Sample Predictions

| Input Features | Prediction |
|----------------|------------|
| HR: 140, RR: 35, O2: 96%     | ❗ High Risk |
| HR: 120, RR: 30, O2: 98%     | ✅ Normal |
| HR: 160, RR: 40, O2: 90%     | ❗ High Risk |

---

## 🧑‍💻 Author

**Manohar Eldhandi**  
🎓 CMR Institute of Technology  
📧 manohareldhandi@gmail.com  
🌐 [LinkedIn](https://www.linkedin.com/in/manohar-eldhandi-baa016264/)  
💻 [GitHub](https://github.com/ManoharEldhandi)

---

## 🛡️ License

This project is open-sourced under the **MIT License**.
