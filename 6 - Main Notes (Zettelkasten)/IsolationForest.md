2025-09-25 07:55

### Status: #baby

### Tags: [[machine-learning]]

# What is  IsolationForest?

[IsolationForest] is an unsupervised anomaly detection algorithm that relies on the principle that anomalies are **few and different**. Based on that assumption, it directly isolates anomalies by surfacing and exploiting key characteristics.

### Isolation through random partitioning
The algorithm works by randomly partitioning data points through binary trees. Key insights are:
- Normal points require many random splits to isolate as they are surrounded by similar points
- Anomalous points require few random splits to isolate, since they already are in sparse regions
![[Pasted image 20250925075940.png]]


## Descriptions





# References









