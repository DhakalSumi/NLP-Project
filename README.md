# NLP-Project
🚨 Disaster Tweet Classification
This project focuses on classifying tweets as disaster-related (1) or not disaster-related (0) using various machine learning and deep learning models.

📁 Dataset
train.csv: Contains tweets and corresponding target labels.

text: The tweet content.

target: 1 if about a disaster, 0 otherwise.

🧠 Models & Results
1️⃣ Logistic Regression
Accuracy: 0.798
Precision (class 1): 0.82
Recall (class 1): 0.68
F1-score (class 1): 0.74
Best Params: {'C': 1, 'solver': 'liblinear'}

Confusion Matrix:
[[777  97]
 [210 439]]
 
2️⃣ Random Forest
Accuracy: 0.772
Precision (class 1): 0.76
Recall (class 1): 0.68
F1-score (class 1): 0.72
Best Params: {'n_estimators': 100, 'max_depth': None, 'min_samples_split': 5, 'min_samples_leaf': 1}

Confusion Matrix:
[[733 141]
 [206 443]]
 
3️⃣ LSTM (Deep Learning)
Accuracy: 0.57
Precision (class 1): 0.00
Recall (class 1): 0.00
F1-score (class 1): 0.00
Classification Report:
                  precision  recall  f1-score   support

           0       0.57      1.00      0.73       874
           1       0.00      0.00      0.00       649

    accuracy                           0.57      1523
   macro avg       0.29      0.50      0.36      1523
weighted avg       0.33      0.57      0.42      1523

⚠️ Note: The LSTM model underperformed in this case. This could be due to limited training time, small batch size, or insufficient data. Improvements can be made by adding pre-trained word embeddings (e.g., GloVe), more epochs, and hyperparameter tuning.

📊 Visuals
ROC curves and confusion matrices were plotted to visually compare performance.

Logistic Regression showed the most balanced results overall.

🚀 Future Improvements
Implement GloVe embeddings in LSTM

Try other deep learning models (Bi-LSTM, GRU)

Use transformers (e.g., BERT) for better context

Perform oversampling to address class imbalance

