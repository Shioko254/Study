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
- AUPR: Precision and Recall
- AUPRO: For better deflect region
- Confusion matrix: a N x N matrix, which show the numbers of classification for each classes or categories.


REGRESSION METRICS
------------------
- Mean Absolute Error (MAE): calculates the average of the absolute differences between the predicted and actual values
$$\text{MAE} = \frac{1}{N} \sum_{j=1}^{N} |y_j - \hat{y}_
j|$$
- Mean Squared Error (MSE): Caculate the average of the squared differences between the predicted and actual values. Squaring the differences ensures that larger errors are penalized more heavily helps in making it sensitive to outliers. This is useful when large errors are undesirable but it can be problematic when outliers are not relevant to the model’s purpose.
$$\text{MSE} = \frac{1}{N} \sum_{j=1}^{N} (y_{j} - \hat{y}_
{j})^{2}$$
- Root Mean Squared Error (RMSE): is the square root of MSE, bring the metric back to the original scale of the data. It heavily penalizes larger errors and easy to know how much our predictions deviate from the actual values.
$$\text{RMSE} = \sqrt{\frac{\sum_{j=1}^{N} (y_{j} - \hat{y}_
{j})^{2}}{N}}$$
- Root Mean Squared Logarithmic Error (RMSLE): RMSLE is useful when the target variable spans a wide range of values such as prices or population. It penalizes underestimations more than overestimations.
$$\text{RMSLE} = \sqrt{\frac{1}{N} \sum_{j=1}^{N} \left( \log(y_{j}+1) - \log(\hat{y}_
{j}+1) \right)^{2}}$$
- R-squared: Represents the proportion of the variance in the dependent variable that is predictable from the independent variables.
$$R^{2} = 1 - \frac{\sum_{j=1}^{n} (y_{j} - \hat{y}_{j})^{2}}{\sum_{j=1}^{n} (y_{j} - \bar{y})^{2}}$$


CLUSTERING METRICS
------------------
- Silhouette Score: evaluates how well a data point fits within its assigned cluster considering how close it is to points in its own cluster (cohesion) and how far it is from points in other clusters (separation). A higher silhouette score (close to +1) shows well-clustered data while a score near -1 suggests that the data point is in the wrong cluster. Silhouette Score = (b-a) / max(a,b) ; with a, b is Average distance between a sample and all other points in the same/nearest cluster
- Davies- Bouldin Index: measures the average similarity between each cluster and its most similar cluster
$$\text{Davies-Bouldin Index} = \frac{1}{N} \sum_{i=1}^{N} \max_{i \neq j} \left( \frac{\sigma_{i} + \sigma_{j}}{d(c_{i}, c_{j})} \right)$$
