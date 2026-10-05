# 🔥 Forest Fire Weather Index (FWI) Prediction

An end-to-end Machine Learning project that predicts the **Forest Fire Weather Index (FWI)** using environmental and fire-weather parameters.

The project uses **Ridge Regression** for prediction and **StandardScaler** for feature scaling. The trained Machine Learning model is deployed as a web application using **Flask**, allowing users to enter input values through an HTML interface and receive an FWI prediction.

---

## 📌 Project Overview

Forest fires are influenced by several environmental factors such as temperature, relative humidity, wind speed, rainfall, and fire-weather indices.

This project demonstrates how a trained Machine Learning model can be converted into a working web application.

### End-to-End Workflow

```text
Dataset
   ↓
Data Preprocessing
   ↓
Feature Engineering
   ↓
Model Training
   ↓
Ridge Regression
   ↓
StandardScaler
   ↓
Model Serialization
   ↓
Flask Application
   ↓
HTML Interface
   ↓
User Input
   ↓
FWI Prediction


🚀 Features
Forest Fire Weather Index prediction
Ridge Regression model
StandardScaler feature preprocessing
Pickle-based model serialization
Flask web application
HTML-based prediction form
User input through web interface
End-to-end Machine Learning deployment workflow


📊 Dataset

The project uses the Algerian Forest Fires Dataset.

The dataset contains weather and fire-related parameters used to analyze forest fire conditions.

🤖 Machine Learning Model
Ridge Regression

Ridge Regression is used to predict the Forest Fire Weather Index.

Ridge Regression is a regularized version of linear regression that uses L2 regularization to reduce overfitting and control large model coefficients.

The trained model is saved as:models/ridge.pkl

⚙️ Feature Scaling

Before making predictions, the input data is transformed using a previously trained StandardScaler.

The scaler is saved as:models/scaler.pkl

The Flask application loads the trained model and scaler using Pickle.

ridge_model = pickle.load(open('models/ridge.pkl', 'rb'))
standard_scaler = pickle.load(open('models/scaler.pkl', 'rb'))

The user input is first scaled and then passed to the Ridge Regression model.

🌐 Flask Application

The Flask application is implemented in:

application.py
Home Route
GET /

The home route displays the main webpage.

@app.route("/")
def index():
    return render_template('index.html')
Prediction Route
GET /predictdata
POST /predictdata

The prediction route receives user input from the HTML form, processes the values, applies feature scaling, and generates the FWI prediction.

@app.route('/predictdata', methods=['GET', 'POST'])
def predict_datapoint():
🖥️ User Input

The web application accepts environmental parameters through an HTML form.

The input fields include:

Temperature
RH
Ws
Rain
FFMC
DMC
ISI
Classes
Region

The data is submitted to Flask using the HTTP POST method.

🔄 Prediction Workflow

When the user clicks the Predict button:

User enters values
        ↓
HTML Form
        ↓
POST Request
        ↓
Flask /predictdata
        ↓
Read User Input
        ↓
Convert Input to Numeric Values
        ↓
StandardScaler
        ↓
Ridge Regression Model
        ↓
FWI Prediction
        ↓
Display Result
📂 Project Structure
Flastk-Lab/
│
├── .vscode/
│
├── models/
│   ├── ridge.pkl
│   └── scaler.pkl
│
├── notebooks/
│   ├── Algerian_forest_fires_dataset_UPDATE.csv
│   ├── Model_Training.ipynb
│   └── Ridge_Lasso_Regression.ipynb
│
├── templates/
│   ├── home.html
│   └── index.html
│
├── application.py
├── requirements.txt
└── README.md
💻 Installation
1. Clone the Repository
git clone <your-repository-url>

Navigate to the project directory:

cd Flastk-Lab
2. Create a Virtual Environment
python -m venv venv

Activate the virtual environment on Windows:

venv\Scripts\activate
3. Install Dependencies
pip install -r requirements.txt
📦 Requirements

The project requires the following Python libraries:

Flask
NumPy
Pandas
Scikit-learn
▶️ Run the Application

Start the Flask application:

python application.py

After starting the application, Flask will display:

Running on http://127.0.0.1:5000

Open the following URL in your browser:

http://127.0.0.1:5000
🧪 How to Use
Start the Flask application.
Open http://127.0.0.1:5000 in your browser.
Enter the required environmental values.
Click the Predict button.
Flask receives the input values.
The input values are scaled using the trained StandardScaler.
The Ridge Regression model generates the FWI prediction.
The prediction is displayed on the webpage.
📁 Model Files

The application uses two trained model artifacts:

ridge.pkl

Contains the trained Ridge Regression model.

scaler.pkl

Contains the trained StandardScaler used for preprocessing the input features.

Both files are required for the Flask application to make predictions.

🧠 Machine Learning Concepts

This project demonstrates:

Data preprocessing
Feature engineering
Feature scaling
Regression
Ridge Regression
L2 Regularization
Model training
Model serialization
Pickle
Model loading
Prediction pipeline
Machine Learning deployment
Flask integration
HTML form handling
📚 Learning Outcomes

Through this project, I learned how to:

Prepare data for Machine Learning
Train a regression model
Apply feature scaling
Save trained Machine Learning models
Load .pkl model files
Build a Flask application
Create an HTML prediction form
Receive user input using Flask
Connect a Machine Learning model with a web application
Build an end-to-end Machine Learning prediction system
Deploy a trained model through a web interface
🔮 Future Improvements

Future improvements can include:

Better UI/UX design
CSS styling
Input validation
Error handling
Prediction history
Data visualization
Model performance dashboard
REST API
Dockerization
Cloud deployment
Automated testing
Production deployment using a WSGI server
⚠️ Disclaimer

This project is created for educational and demonstration purposes.

The predictions generated by this application should not be used as the sole basis for real-world wildfire risk assessment or emergency decision-making.

👨‍💻 Author

Karthik T

B.Tech — Artificial Intelligence and Machine Learning

Areas of Interest
Data Analytics
Machine Learning
Python
Data Visualization
Power BI
End-to-End Machine Learning Projects
⭐ Project Highlights
✔ End-to-End Machine Learning Project
✔ Ridge Regression
✔ StandardScaler
✔ Flask Web Application
✔ HTML Prediction Interface
✔ Pickle Model Deployment
✔ Real-World Forest Fire Dataset
✔ Machine Learning Model Integration
📜 License

This project is created for educational and learning purposes.