# multiple-disease-prediction-streamlit-app
This repository contains the codebase for "Multiple Disease Prediction Streamlit App". The training notebooks &amp; the datasets are also provided in the respective folders. 

## how to run this project.
1. Extract the Zip file.
2. open visual studio and upload a extracted folder
3. Goto the app.py and Run the app.py


app.py is the streamlit app code.
run the command 
```
pip install -r requirements.txt
```
to install the required dependencies for the streamlit app.

You may need to install additional libraries for running the jupyter notebooks.

## Common facing Errors
1.Handle missing values before training
```
df.fillna(df.mean(), inplace=True)  # Fill missing values with column mean
```
2.Increase iterations
```
model = LogisticRegression(max_iter=1000)
```
3.Ensure the same preprocessing steps on new data
```
X_new = scaler.transform(X_new)  # Use the same scaler as training data
```
4.Apply same StandardScaler to both train and test data.
```
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```
5.Ensure both training and loading are done using the same Python version.
```
import pickle
with open('model.pkl', 'wb') as f:
    pickle.dump(model, f)
```
