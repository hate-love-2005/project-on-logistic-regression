Project Structure:-

project-on-logistic-regression/
│
├── placement.csv        # Dataset containing student records
├── placement.ipynb      # Jupyter Notebook (data analysis + model training)
├── model.pkl            # Saved trained Logistic Regression model
└── README.md            # Project documentation


Problem Statement:-
The goal is to classify whether a student will be placed (1) or not placed (0) based on input features such as:

CGPA / academic performance
IQ / aptitude score (if present in dataset)
Other numerical features in dataset


Tech Stack & Libraries Used
:-
Python 
NumPy → numerical operations
Pandas → data handling & CSV processing
Matplotlib → visualization
Seaborn → data visualization
Scikit-learn → Logistic Regression model + evaluation
Pickle → saving trained model (model.pkl)
Jupyter Notebook → development environment
Machine Learning Model
Algorithm Used:
 Logistic Regression (Supervised Classification Algorithm)

Why Logistic Regression?
Works well for binary classification problems
Outputs probability between 0 and 1 using sigmoid function
Easy to interpret and highly efficient for small datasets

 
 Workflow of the Project
Load dataset (placement.csv)
Perform Exploratory Data Analysis (EDA)
Select input features (X) and target variable (y)
Split dataset into training and testing sets
Train Logistic Regression model using sklearn
Evaluate model performance
Save trained model using pickle → model.pkl

 
 How to Run the Project
1. Clone the repository
git clone https://github.com/hate-love-2005/project-on-logistic-regression.git
cd project-on-logistic-regression
2. Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn
3. Run the notebook
jupyter notebook placement.ipynb
Run all cells to:
Train the model
Test predictions
Generate model.pkl



 How to Use the Saved Model:-
 
After training, the model is saved as model.pkl.

Example prediction:

import pickle

model = pickle.load(open("model.pkl", "rb"))

# Example input (replace with actual feature values from dataset)
prediction = model.predict([[feature1, feature2]])

print(prediction)

# Output:
# 1 → Placed
# 0 → Not Placed
Model Output


The model evaluates performance using:
Accuracy Score
Confusion Matrix (if used in notebook)
Train/Test split validation
