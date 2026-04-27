Anomaly Detection
- the analytical technique used to indentify data points or behaviors that deviate from expected patterns. 
- focuses on descovering irregularities that may indicate underlying problems or abnormal system behavior.
- the system needs to learn about the normal behavior of the object first, then it will be able to detect the abnormal.


TYPES OF ABNOMALIES
-------------------
- Point anomalies: A point anomaly happens when one data point significantly diffe­rs from the overall data distribution
    example: A credit card transaction much larger than typical spending for that account.

- Contextual anomaly: the data that look normal on a whole but are deviated from normal only in a particular context.
    example: 30 Celsius degree in winter.

- Collective anomaly: a group of data points that appear normal individually but are anomalous when considered together.
    example: Sudden bursts of network traffic from one IP over a short time, potentially indicating a denial-of-service attack 


ABNOMALY DETECTION TECHNIQUES
-----------------------------
- Factual techniques: Use the measurable mearsure such as Mean, Standard devision (độ lệch chuẩn), z-scores
- Density based techniques: measure distances between data points to identify the anomolies.
- Ensemble stategies: Combine multiple anomaly detection methods to improve accuracy.
- Time series analysis: sequential data.


ABNOMALY DETECTION MACHINE LEARNING TECHNIQUES
----------------------------------------------
- `Supervised anomaly detection`: labeled dataset where each data point is marked as “normal” or “anomalous”. 
  Techniques: Decision trees, Support vector machines (SVM) and Neural network.
- `Unsupervised anomaly detection`: Not require labeled dataset. Assume and anomalies are rare or differ significantly from the majority of data points.
  Techniques+ Clustering, density based methods, autoencoders, dimensionality reduction.
- `Semi-supervised anomaly detection`: Only normal data is labeled. 
  Techniques: NN trained to reconstruct normal data and measure deviations using reconstruction error. 
