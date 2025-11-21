# Credit Card Fraud Detection - Machine Learning Project

## 📋 Project Overview
This project develops machine learning models to detect fraudulent credit card transactions using advanced data preprocessing techniques and classification algorithms.

**Submitted by:** Abdullahi Mohamed Jibril  
**Institution:** Nexford University  
**Date:** November 21, 2025  
**Course:** Data Analytics - Capstone Project

---

## 📊 Dataset Information
- **Total Transactions:** 283,726 (after cleaning)
- **Features:** 30 (28 PCA-transformed + Time + Amount)
- **Target Variable:** Class (0 = Normal, 1 = Fraud)
- **Class Distribution:** 
  - Normal: 283,253 (99.83%)
  - Fraud: 473 (0.17%)
- **Data Sources:**
  - Original Dataset: [Kaggle Credit Card Fraud Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
  - Processed Dataset: [Google Drive](https://drive.google.com/file/d/1CZiBQf-M2I5D1luaom_rmwgt7c22o47E/view?usp=drive_link)

---

## 🔧 Project Structure
```
credit-card-fraud-detection-ml/
│
├── notebooks/
│   ├── 01_exploratory_data_analysis.ipynb
│   └── 02_model_development.ipynb
│
├── presentation/
│   └── Milestone1_Presentation.pptx
│
└── README.md
```


---

## 🛠️ Technologies Used
- **Python 3.x**
- **Libraries:** pandas, numpy, scikit-learn, imbalanced-learn, matplotlib, seaborn
- **Tools:** Jupyter Notebook, Google Colab, GitHub

---

## 📈 Methodology

### 1. Data Preparation
- Removed 1,081 duplicate records
- Scaled Time and Amount features using StandardScaler
- No missing values detected

### 2. Feature Engineering
- Standardized numerical features
- Retained all 30 features for model training

### 3. Handling Class Imbalance
- **Technique:** SMOTE (Synthetic Minority Over-sampling)
- **Result:** Balanced training set (226,602 samples per class)

### 4. Model Development
Two classification models were developed and evaluated:

#### **Logistic Regression**
- Accuracy: 97.37%
- Precision: 5.31%
- Recall: 87.37%
- F1-Score: 10.02%
- ROC-AUC: 96.19%

#### **Random Forest Classifier**
- Accuracy: 99.95%
- Precision: 91.14%
- Recall: 75.79%
- **F1-Score: 82.76%** ⭐
- ROC-AUC: 94.94%

---

## 🏆 Results

### Best Model: **Random Forest Classifier**
- **Superior performance** with F1-Score of 82.76%
- High precision (91.14%) minimizes false alarms
- Balanced recall (75.79%) catches most fraudulent transactions
- **Confusion Matrix:**
  - True Negatives: 56,644
  - False Positives: 7
  - False Negatives: 23
  - True Positives: 72

---

## 💡 Key Findings
1. **Severe class imbalance** successfully addressed using SMOTE
2. Random Forest outperformed Logistic Regression across all metrics except recall
3. **Top predictive features:** V17, V14, V12, V10 (highest correlation with fraud)
4. Model achieves 99.95% accuracy with minimal false positives

---

## 🚀 Business Recommendations
1. **Deploy Random Forest model** for real-time fraud detection
2. Set decision threshold based on cost-benefit analysis
3. Implement continuous model monitoring and retraining
4. Review false positives to minimize customer friction
5. Prioritize high-value transactions for manual review

---

## 📁 Files Description
- `01_exploratory_data_analysis.ipynb`: Complete EDA with visualizations
- `02_model_development.ipynb`: Model training, evaluation, and comparison
- `Milestone1_Presentation.pptx`: EDA presentation slides

**Data Files (External Links):**
- Original Dataset: [Download from Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Processed Dataset: [Download from Google Drive](https://drive.google.com/file/d/1CZiBQf-M2I5D1luaom_rmwgt7c22o47E/view?usp=drive_link)

---

## 🔄 How to Run

### Step 1: Clone Repository
```bash
git clone https://github.com/yourusername/credit-card-fraud-detection-ml.git
cd credit-card-fraud-detection-ml
```

### Step 2: Download Datasets
- Download the original dataset from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Or use the processed dataset from [Google Drive](https://drive.google.com/file/d/1CZiBQf-M2I5D1luaom_rmwgt7c22o47E/view?usp=drive_link)
- Place the CSV file in the project root directory

### Step 3: Install Dependencies
```bash
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn jupyter
```

### Step 4: Run Notebooks
```bash
jupyter notebook notebooks/01_exploratory_data_analysis.ipynb
jupyter notebook notebooks/02_model_development.ipynb
```

---

## 📧 Contact
**Abdullahi Mohamed Jibril**  
Nexford University  
Email: abdulaahimohamed65@gmail.com

---

## 📄 License
This project is submitted as part of academic coursework at Nexford University.

---

## 🙏 Acknowledgments
- Nexford University - Data Analytics Program
- Kaggle - Credit Card Fraud Detection Dataset
- scikit-learn and imbalanced-learn communities

---

⭐ **If you find this project useful, please consider giving it a star!**
