# Sampling
by Amrita Bhatia (Roll no. 102017017)

Sampling is a statistical technique used to select a subset of a population. An ideal sample should have all the characteristics of the population it is derived from. This technique allows us to estimate an entire population by using a representative subset and therefore reduce the time required to train models with minimal compromise on the model performance.

This project applies various sampling techniques to different machine learning models and evaluates their performance using the accuracy metric.

Sampling techniques used:
| S. No. | Technique |
|---|---|
| S1  |Simple random sampling (w/0 replacement) |
| S2  |Simple random sampling (with replacement) |
| S3  |Systematic sampling |
| S4  |Stratified sampling |
| S5  |Cluster sampling |

Models used:
|  S. No. | Model |
|---|---|
| M1  |Logistic regression |
| M2  |Naive Bayes classifier |
| M3  |Support vector classifier |
| M4  |Decision tree |
| M5  |Random forest |

## Methodology
- The data was highly imbalanced with a 98.8% majority class. Therefore, SMOTE was used to balance the class distribution.
- The five sampling techniques were then applied to select samples from the data.
- These samples were then used to train the machine learning models. The models were tested on the remaining data not included in the sample.

## Results
The accuracies of the models for each sample are as follows:
|   | logreg | nb | svc | dt | rf |
|---|---|---|---|---|---|
| S1 | 0.818182  | 0.792208  |  0.935065 | 0.948052 |1.000000|
| S2 | 0.917866  | 0.897544  | 0.911092  | 0.970364 |0.990686|
| S3 |  0.906557 | 0.796721  | 0.906557  | 0.947541 |0.991803|
| S4 | 0.922162  | 0.752432  | 0.915676  | 0.966486 |0.992432|
| S5 | 0.458849  |  0.541151 | 0.490168  | 0.446468 |0.448653|

- The highest accuracy (**100%**) is seen in the random forest model using simple random sampling without replacement.
- The worst performing model is the decision tree using the cluster sampling technique with an accuracy of **44.65%**.
