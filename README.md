# Early Stage Heart Diease Detection with Federated Learning

![Contributors](https://img.shields.io/github/contributors/EthanWTL/HeartDiseasePakula?style=plastic)
![Forks](https://img.shields.io/github/forks/EthanWTL/HeartDiseasePakula)
![Stars](https://img.shields.io/github/stars/EthanWTL/HeartDiseasePakula)
![Licence](https://img.shields.io/github/license/EthanWTL/HeartDiseasePakula)
![Issues](https://img.shields.io/github/issues/EthanWTL/HeartDiseasePakula)

## Description

Welcome! 😀

We are dedicated data scientists working with [Pakula BioMedical Fellowship Program](https://www.beloit.edu/academics/biology/resources-opportunities/summer-research/) for summer research! 

It has a focus on implementing Federated Learning on [UCI Heart Disease dataset](https://archive.ics.uci.edu/dataset/45/heart+disease) to help early stage detection of cardiovasular diseases.

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
|  | SOM  | Kmean | ANN | CNN | RNN |
| --- | --- | --- | --- | --- | --- | 
| Accuracy | 81.% | 80%  | 85% |85%| 84%|




## Stage II: Federated Learning
### Getting started with FL
* Download the [MNIST data set from Kaggle](https://www.kaggle.com/datasets/scolianni/mnistasjpg)
* Run the Python files
  ```sh
   python FL_demo/run_federated_learning.py
   ```
* Global Model Accuracy: ```80.20%```
* Check out [Flower](https://github.com/adap/flower) with more detailed explanation about FL.

### Our FL pipeline:
```mermaid
graph TB
    A{Global Model} <-- weights_transfer --> B[Cleveland_model]
    A{Global Model} <-- weights_transfer --> C[Virginia_model]
    A{Global Model} <-- weights_transfer --> D[Hungarian_model]
    A{Global Model} <-- weights_transfer --> E[Switzerland_model]

    B -- training --> F((Cleveland_data))
    C -- training --> G((Virginia_data))
    D -- training --> H((Hungarian_data))
    E -- training --> I((Switerland_data))

    F -- update_model --> J(Cleveland_model_updated)
    G -- update_model --> K(Virginia_model_updated)
    H -- update_model --> L(Hungarian_model_updated)
    I -- update_model --> M(Switzerland_model_updated)

```
### Results:
* ```Learning rate```: 0.01
* ```Optimizer```: SGD
* ```Loss function```: Sparse Cross Entropy
* Result after 100 ```global epochs```:

  | Model  | Accuracy  | Precision | Recall |
  |--------|------------|-------|----------|
  |MLP|85%|85%|85%|
  |CNN|temp|temp|temp|temp|
  |RNN|temp|temp|temp|temp|


---



## Analysis & Comparison





## Roadmap
- [x] Implement Baseline experiment
- [ ] Federated Learning
  - [x] MLP
  - [ ] CNN
  - [ ] RNN
- [ ] Tranfer Learning





## Contact
Ethan Wang - [e13wang@gmail.com](e13wang@gmail.com) - [Linkedin Profile](https://www.linkedin.com/in/ethan-wang-938588175/)

Takeshi Matsuda - [takeshimatsuda27@gmail.com](takeshimatsuda27@gmail.com) - [Linkedin Profile](https://www.linkedin.com/in/takeshi-matsuda-41777b1ab/)

Project Link: [https://github.com/matsudatakeshi27/HeartDiseasePakula](https://github.com/matsudatakeshi27/HeartDiseasePakula)




## Acknowledgments:
* [Back-Propagation Neural Network Versus Logistic Regression in Heart Disease Classification](https://link.springer.com/chapter/10.1007/978-981-13-0680-8_13)
* [Heart Disease Risk Prediction Using Supervised Machine Learning Algorithms](https://link.springer.com/chapter/10.1007/978-981-99-0412-9_11)
* [HEART DISEASE PREDICTION USING DATA MINING TECHNIQUES](https://hal.science/hal-02196156/)
* [A Submodularity-based Agglomerative Clustering Algorithm for the Privacy Funnel](https://www.semanticscholar.org/paper/A-Submodularity-based-Agglomerative-Clustering-for-Ding-Sadeghi/4e7b3b31659c945ed0c953da9fe7af297b3f3675)
* [Early detection of silent ischaemic heart disease by 24-hour electrocardiographic monitoring of active subjects.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC458846/)
* [Development of a federated learning approach to predict acute kidney injury in adult hospitalized patients with COVID-19 in New York City](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8328073/)
* [Federated learning for multi-center imaging diagnostics: a simulation study in cardiovascular disease](https://www.nature.com/articles/s41598-022-07186-4)
