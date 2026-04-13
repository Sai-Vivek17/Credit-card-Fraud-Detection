# Credit Card Fraud Detection
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-0.24+-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.2+-green.svg)

An end-to-end Machine Learning project designed to identify fraudulent credit card transactions. This project utilizes **Logistic Regression** and **Random Forest** classifiers, specifically addressing the challenge of highly imbalanced datasets through **Under-Sampling** techniques.

## 📌 Project Overview
Credit card fraud detection is a critical application of data science in the financial sector. The primary challenge is that fraudulent transactions are rare compared to legitimate ones. This project demonstrates:
* **Data Preprocessing:** Handling missing values and data cleaning.
* **Class Imbalance Management:** Implementing Under-Sampling to create a balanced dataset for training.
* **Comparative Modeling:** Evaluating multiple algorithms to find the most robust solution.
* **Model Persistence:** Saving trained models using `joblib` for future deployment.

## 📊 Dataset
The dataset contains transactions made by credit cards in September 2013 by European cardholders. 
* **Features:** Includes numerical input variables `V1, V2, ... V28` (resulting from a PCA transformation) along with `Time` and `Amount`.
* **Target:** `Class` (0 for legitimate transactions, 1 for fraudulent).

> **Note on Dataset Access:** Due to the large file size, the raw dataset is hosted externally.
> **[https://drive.google.com/drive/folders/1EpId8NUP55ULvxBTbIBldSt_rK4TovL4?usp=sharing]**

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `pandas` & `numpy` (Data Manipulation)
    * `scikit-learn` (Machine Learning & Evaluation)
    * `joblib` (Model Serialization)

## ⚙️ Workflow
1. **Data Exploration:** Analyzing the distribution of legitimate vs. fraudulent cases.
2. **Under-Sampling:** Since the original data is heavily skewed, a sample of legitimate transactions was combined with all fraudulent cases to create a balanced distribution (492 legitimate vs. 93 fraudulent in this specific version).
3. **Data Splitting:** Using `train_test_split` with stratification to maintain class ratios.
4. **Model Training:**
    * **Logistic Regression:** A baseline linear model.
    * **Random Forest:** An ensemble method for higher accuracy.
5. **Evaluation:** Comparing models based on Accuracy Scores.

## 📈 Performance Results
The models were evaluated on both training and test data:

| Model | Training Accuracy | Test Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | ~97.8% | ~98.3% |
| **Random Forest** | ~100% | **~99.1%** |

*Conclusion: The **Random Forest Classifier** provided superior performance and was selected as the final model for deployment.*

## 📂 Repository Structure
```text
├── data/                   # Folder for the dataset (ignored by git)
├── models/                 # Saved machine learning models (.pkl)
│   └── fraud_detection_model.pkl
├── notebooks/              # Jupyter/Colab notebooks for exploration and training
│   └── fraud_detection_training.ipynb
├── requirements.txt        # List of dependencies required to run the code
└── README.md               # Project documentation
## 🚀 How to Use
1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Credit-Card-Fraud-Detection.git](https://github.com/YOUR_USERNAME/Credit-Card-Fraud-Detection.git)
