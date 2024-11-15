# Ex.No: 13 Learning – Use Supervised Learning  
### DATE:4.11.2024                                                                            
### REGISTER NUMBER : 212221060117
### AIM:
To write a program to train the classifier for cancer prediction level.
###  Algorithm:
```
1.import necessary  libraries.
2.Load Model and Encode.
3.Create a new DataFrame new_data with the input features required by the model. Replace these with actual data as needed.
4.Use the loaded model to predict the class for the new data.
5.Store the decoded class label in predicted_level.
6.Print the result, which is the predicted level for the new data point.
```

### Program:
```
import pandas as pd
import joblib

# Load the trained model and LabelEncoder
model = joblib.load('random_forest_model.pkl')
label_encoder = joblib.load('label_encoder.pkl')

# New input data (replace with actual data as needed)
new_data = pd.DataFrame({
    'Age': [25],
    'Gender': [1],
    'Air Pollution': [3],
    'Alcohol use': [2],
    'Dust Allergy': [5],
    'OccuPational Hazards': [4],
    'Genetic Risk': [3],
    'chronic Lung Disease': [2],
    'Balanced Diet': [5],
    'Obesity': [4],
    'Smoking': [3],
    'Passive Smoker': [1],
    'Chest Pain': [2],
    'Coughing of Blood': [4],
    'Fatigue': [3],
    'Weight Loss': [4],
    'Shortness of Breath': [2],
    'Wheezing': [2],
    'Swallowing Difficulty': [3],
    'Clubbing of Finger Nails': [1],
    'Frequent Cold': [2],
    'Dry Cough': [3],
    'Snoring': [4]
})

# Predict the 'Level' for the new data
new_prediction = model.predict(new_data)

# Convert the numeric prediction back to the original class labels
predicted_level = label_encoder.inverse_transform(new_prediction)

print(f"Predicted Level: {predicted_level[0]}")
```



### Output:
![Screenshot_13-11-2024_105553_colab research google com](https://github.com/user-attachments/assets/bffddeca-9b6c-4d8d-9962-e40d835dc0ee)





### Result:
Thus the system was trained successfully and the prediction was carried out.
