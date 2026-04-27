EVALUATION METRICS
------------------
Evaluation metrics are used to measure how well a machine learning model performs.


Classification metrics
----------------------
- Accuracy: Correct predictions / Total of predictions
  it can be misleading in cases of imbalanced datasets.
- Precision: It measures how many of the positive predictions made by the model are actually correct.
  Precision = TP / (FP + TP)
- Recall:  How many of the actual positive cases were correctly identified by the model
  Recall = TP / (TP + FN)
- F1 score: Is the harmornic mean of Precision and Recall.
  F1 score = 2 x Precision x Recall / (Precision + Recall)
- Logarithmic Loss: measures the uncertainty of the model’s predictions
$$\text{Logarithmic Loss} = -\frac{1}{N} \sum_{i=1}^{N} \sum_{j=1}^{M} y_{ij} \cdot \log(p_{ij})$$
- AUC and ROC Curve: useful for binary classification tasks. AUC represents the probalility that the model will rank a randomly choén positive example higher than a randomly chosen negative example. AUC ranges from 0 to 1 with higher values showing better model performance.
    - True positive rate (TPR): Also known as Sensitivity or Recall
    - True negative rate (TNR): TNR = TN / (TN + FP)
    - False positive rate (FPR): FPR = FP / (FP + TN)
    - False negative rate (FNR): FNR = FN / (FN + TP)
- ROC curve: It is a graphical representation of TPR and FPR at different classification thresholds. 
- Confusion matrix: a N x N matrix, which show the numbers of classification for each classes or categories.


REGRESSION METRICS
------------------
- Mean Absolute Error (MAE): calculates the average of the absolute differences between the predicted and actual values
$$\text{MAE} = \frac{1}{N} \sum_{j=1}^{N} |y_j - \hat{y}_j|$$
