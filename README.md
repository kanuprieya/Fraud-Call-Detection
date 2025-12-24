The fraud call detection model uses 3 ML models - Naive Bayes, Random Forest and SVM to compare their results and to find which model gives the best results.
Multiple Hugging face datasets have been modified to form 1 single dataset for the model to work on (

Datasets Used:
1. Combined Training Dataset (combined_dataset.csv)
Created by aggregating multiple scam-related datasets from Hugging Face
Text and labels are normalized into a binary format
1 → Scam
0 → Not Scam
Used only for training and validation
This dataset is generated inside the notebook using Hugging Face’s load_dataset API.

2. Balanced Testing Dataset (balanced_dataset.csv)
Separate dataset with balanced class distribution
Used only for evaluation
Ensures fair performance measurement and avoids data leakage

Final results:

🔍 Evaluating Naive Bayes
✅ Accuracy: 0.7200
📊 Classification Report:
              precision    recall  f1-score   support

    Not Scam       0.68      0.84      0.75      1250
        Scam       0.79      0.60      0.68      1250

    accuracy                           0.72      2500
   macro avg       0.73      0.72      0.72      2500
weighted avg       0.73      0.72      0.72      2500


🔍 Evaluating SVM
✅ Accuracy: 0.9524
📊 Classification Report:
              precision    recall  f1-score   support

    Not Scam       0.93      0.98      0.95      1250
        Scam       0.98      0.92      0.95      1250

    accuracy                           0.95      2500
   macro avg       0.95      0.95      0.95      2500
weighted avg       0.95      0.95      0.95      2500


🔍 Evaluating Random Forest
✅ Accuracy: 0.9548
📊 Classification Report:
              precision    recall  f1-score   support

    Not Scam       0.93      0.98      0.96      1250
        Scam       0.98      0.92      0.95      1250

    accuracy                           0.95      2500
   macro avg       0.96      0.95      0.95      2500
weighted avg       0.96      0.95      0.95      2500

Further, the file has code for plotting the Accuracy and other Performance Metrics comparison of the 3 models.
