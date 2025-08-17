# ECG Arrhythmia Detection

A CNN-based project for classifying ECG heartbeats using the MIT-BIH Arrhythmia dataset.

## Project Overview
- **Dataset:** MIT-BIH Arrhythmia
- **Input:** 187-sample ECG signals per heartbeat
- **Model:** Convolutional Neural Network (CNN)
- **Output:** Predicted heartbeat class

## Files
- `arrhythmia.ipynb` : Jupyter notebook with data preprocessing, model training, and evaluation.
- `ecg_model.keras` : Trained Keras model (can be converted to TensorFlow.js for web integration)

## Notes
- This is a work-in-progress project for research and learning purposes.
- Demonstrates the full pipeline from data preprocessing to CNN-based ECG classification.
- ## How to Test Your ECG Data

You can input your own ECG signals to test the model using a **CSV file**.

### 1. CSV Format
- Each row should contain **187 numeric ECG values** corresponding to a single heartbeat.
- Example (`sample_ecg.csv`):


- Each row represents **one heartbeat**.

### 2. Using the Web App / Backend
1. Go to the **ECG prediction endpoint**: `/predict`  
2. Upload your CSV file containing ECG rows.  
3. The model will return a **predicted class** for each heartbeat.

### 3. Sample Code (Python)
```python
import requests

url = "http://localhost:5000/predict"
files = {'ecgfile': open('sample_ecg.csv', 'rb')}

response = requests.post(url, files=files)
print(response.json())



## Author
Shubham Thakur
