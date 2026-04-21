# Car_price_prediction

Car Price Prediction End-to-End System
📌 Project Overview
This project is an end-to-end Machine Learning application that predicts the selling price of used cars based on various features like age, mileage, fuel type, and transmission. The project includes a full pipeline: data preprocessing, exploratory data analysis (EDA), model training with hyperparameter tuning, and a web-based user interface for real-time predictions.

📊 Dataset & Features
The model is trained on a dataset containing 301 records of used cars.

Key Features used:

Present_Price: Current showroom price of the car.

Kms_Driven: Total distance covered in kilometers.

Fuel_Type: Petrol, Diesel, or CNG.

Seller_Type: Dealer or Individual.

Transmission: Manual or Automatic.

Owner: Number of previous owners.

no_year: Age of the car (Derived from the current year 2026).

🚀 Technical Workflow
1. Data Preprocessing & Engineering

Feature Engineering: Created a new feature no_year by subtracting the car's manufacturing year from the current year (2026) to capture the car's age.


Categorical Encoding: Applied One-Hot Encoding (get_dummies) to handle categorical variables like Fuel_Type and Transmission.


Scaling: Used StandardScaler to normalize the Kms_Driven feature for better model performance.

2. Model Development

Feature Selection: Utilized ExtraTreesRegressor to identify the top features impacting car prices.


Algorithm: Implemented a Random Forest Regressor.


Hyperparameter Tuning: Used RandomizedSearchCV to optimize parameters such as n_estimators, max_depth, and min_samples_split over 5-fold cross-validation.

3. Deployment
Backend: Flask Framework.

Frontend: HTML/CSS based user interface for data entry.


Serialization: The trained model is saved using pickle as random_forest_regression_model.pkl for fast loading during deployment.

💻 Installation & Setup
Clone the repository:

Bash
git clone https://github.com/sattvikkk/Car-Price-Prediction.git
cd Car-Price-Prediction
Install dependencies:

Bash
pip install -r requirements.txt
Run the application:

Bash
python app.py
Open http://127.0.0.1:5000/ in your browser.

📈 Visualizations
The project includes automated visualization of:


Feature Importance: Bar chart showing which factors (like Present Price) most influence the prediction.


Correlation Heatmap: Analyzing the relationship between independent and dependent variables.


Error Distribution: A histogram of residuals (y_test - predictions) to validate model accuracy.

🛠️ Tools & Libraries Used
Languages: Python

Data Manipulation: Pandas, NumPy

Visualization: Matplotlib, Seaborn

ML Frameworks: Scikit-learn

Deployment: Flask, Pickle
