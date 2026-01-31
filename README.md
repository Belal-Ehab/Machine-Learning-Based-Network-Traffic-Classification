# Machine Learning Based Network Traffic Classification

## Overview
This project applies machine learning techniques to classify network traffic as **benign or malicious** using statistical feature selection and supervised learning models. The goal is to evaluate and compare multiple classifiers for malicious traffic detection in a cybersecurity context.

The project was developed as part of a **Computer Networks Course** and focuses on practical data preprocessing, feature engineering, model evaluation, and performance visualization.

---

## Methodology

### Dataset
Network traffic data was collected from four sources:
- output-of-benign-pcap-0
- output-of-malware-pcap
- output-of-phishing-pcap
- output-of-spam-pcap

Each flow is labeled as:
- `0` → Benign  
- `1` → Malicious

To address class imbalance:
- Benign samples: **75,000**
- Malicious samples: **25,000**

> Raw CSV files are intentionally excluded from this repository due to size and data handling considerations.

---

### Data Preprocessing
- Removal of non-informative identifiers (IP addresses, ports, timestamps, domain-based fields)
- Handling missing and infinite values
- Feature scaling using **StandardScaler**
- Variance-based feature filtering

---

### Feature Selection
A two-stage feature reduction strategy was used:
1. **Global reduction** using ANOVA F-test scores
2. **Final selection** using `SelectKBest` to retain the most discriminative features

---

### Models Evaluated
The following classifiers were implemented and compared:
- LASSO Logistic Regression
- Support Vector Machine (RBF kernel)
- k-Nearest Neighbors (k = 5, 7)
- Random Forest

All models were evaluated using **5-fold stratified cross-validation**.

---

## Evaluation Metrics
Models were compared using:
- Accuracy
- Precision
- Recall
- F1-score
- Training time

Performance comparisons and statistical visualizations are included in the notebook.

---

## Repository Contents
- Machine_Learning_Based_Network_Traffic_Classification.ipynb
- LICENSE
- README.md

---

## Contributors
This project was completed as a **group project**.

- **Belal Ehab**  
- **Fahd Rashdan**  
- **Farida Salama**
- **Merola Refaat**
- **Nour ElKhouly**
  
---

## License
This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.

---

## Author
**Belal Ehab**  
Computer Networks Project  
2026
