# Early Stage Heart Diease Detection with Federated Learning

![Contributors](https://img.shields.io/github/contributors/EthanWTL/HeartDiseasePakula?style=plastic)
![Forks](https://img.shields.io/github/forks/EthanWTL/HeartDiseasePakula)
![Stars](https://img.shields.io/github/stars/EthanWTL/HeartDiseasePakula)
![Licence](https://img.shields.io/github/license/EthanWTL/HeartDiseasePakula)
![Issues](https://img.shields.io/github/issues/EthanWTL/HeartDiseasePakula)

## Description

Welcome aboard! 😀

We are dedicated data scientists working on this Data Science Reserach Project. 

It has a focus on implement Federated Learning on [UCI Heart Disease dataset](https://archive.ics.uci.edu/dataset/45/heart+disease) to help early stage detection of Cardiovasular Disease.

---
## Stage I: Baseline Modeling

To create a baseline understanding of the project as well as testing our data cleaning accuracy, we delpoyed a set of traditional machine learning technique, the results for Cleveland datasets are shown as following.

| ML Technique  | Our Accuracy  | Other Research's Accuracy  |
| ------------- | ------------- | ------------------------ |
| Decision Tree  | 75.82%  | 83.57%  [Shrinivas D Desai et al.](https://link.springer.com/chapter/10.1007/978-981-13-0680-8_13)  |
| Random Forest  | 84.37%  |  86.90% [Pal and Parija](https://link.springer.com/chapter/10.1007/978-981-99-0412-9_11)  |
| SVM | 86.89%  |   77.70%    [Anitha S., Sridevi N.](https://hal.science/hal-02196156/)  |
| Bayesian Classifier  | 82.26%  |   86.60%      [Anitha S., Sridevi N.](https://hal.science/hal-02196156/)  |


Besides machine learning techniques, we also deployed clustering and deep learning methods for cross reference.
| ML Technique  | Our Accuracy  |
| ------------- | ------------- |
| SOM  | 81.19%  |
| Kmean  | 80.52%  |
|CNN | 79.85%|
|RNN|82.04%|

---
# Stage II: Federated Learning


This is an example of federated learning using MNIST dataset, first download the [MNIST data set from Kaggle](), and run the Python files.

