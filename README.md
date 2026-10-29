# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Import the required Python libraries, NumPy, and Scikit-learn.
2. Initialize the study hours and marks scored as input data.
3. Train a Simple Linear Regression model using the given data.
4. Predict the marks for the given study hours and display the result with a graph.
## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: ESHAANI.S
RegisterNumber: 212225220031 
*/

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Input data
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([20, 35, 50, 65, 80])

# Create and train the model
model = LinearRegression()
model.fit(X, Y)

# Predict marks
hours = np.array([[6]])
predicted_marks = model.predict(hours)

print("Study Hours:", hours[0][0])
print("Predicted Marks:", predicted_marks[0])

# Plot the graph
plt.scatter(X, Y, color='blue', label='Actual Marks')
plt.plot(X, model.predict(X), color='red', label='Regression Line')
plt.scatter(hours, predicted_marks, color='green', label='Predicted Marks')
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Student Marks Prediction using Linear Regression")
plt.legend()
plt.show()
```


## Output:
<img width="842" height="652" alt="image" src="https://github.com/user-attachments/assets/9e873902-9f90-4a5f-a193-565c4b71abeb" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
