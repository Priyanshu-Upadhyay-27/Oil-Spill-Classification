# Oil Spill Detection Using Machine Learning

## 📖 Project Overview

This project is a comprehensive analysis aimed at identifying the most effective machine learning model for detecting oil spills from satellite imagery data. The goal is to perform binary classification on a dataset with 49 features to predict the presence (`1`) or absence (`0`) of an oil spill.

The notebook covers:
- **Exploratory Data Analysis (EDA)**: Initial analysis and visualization of the dataset to understand its structure and distributions.
- **Data Preprocessing**: Scaling the features to prepare them for various machine learning algorithms.
- **Model Training**: Implementing and training several classification models.
- **Performance Comparison**: Evaluating and comparing the models based on key metrics like Accuracy, Precision, Recall, and F1-Score to determine the best-performing algorithm for this task.

---

### Dataset

The dataset used is `oil_spill.csv`, which contains 937 samples and 50 columns. The `target` column is our dependent variable, while `f_1` to `f_49` are the features.

---

### ⚙️ Installation

To run this project locally, you'll need to have Python installed. Then, clone the repository and install the required packages.

```bash
# Clone the repository
git clone [https://github.com/your-username/oil-spill-detection-ensemble-learning.git](https://github.com/your-username/oil-spill-detection-ensemble-learning.git)
cd oil-spill-detection-ensemble-learning

# Install the required packages
pip install -r requirements.txt
```

---

### 🚀 Usage

You can run the Jupyter Notebook to see the complete analysis, from data loading to model evaluation.

1.  Start Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
2.  Open the `Oil_Spill_Ensemble.ipynb` file.
3.  Run the cells sequentially to reproduce the analysis.

---

### 🤖 Models Explored

This project utilizes several machine learning techniques for different tasks:

* **Dimensionality Reduction**:
    * Principal Component Analysis (PCA)
* **Supervised Classification**:
    * Random Forest Classifier
    * Support Vector Machine (SVM)
* **Unsupervised Clustering**:
    * K-Means Clustering

---

### 📊 Results & Metrics

The comparison of model metrics is the core finding of the analysis. It demonstrates my ability to not only build models but also to evaluate and select the best one based on performance. It is the most important part of this project.

Here is a summary of the model performances:

| Model | Accuracy | Precision | Recall | F1-Score | Cross-Val-Score
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Random Forest Classifier** | 0.9609 | 0.50 | 0.27 | 0.35 | 0.938 |
| **Random Forest Classifier(Using best unskewed Cols)** | 0.9734 | 0.33 | 0.17 | 0.22 | 0.941 |
| **Support Vector Machine**| 0.9734 | 1.00 | 0.17 | 0.29 | 0.956 |
| **Support Vector Machine(After RandomizedSearchCV)** | 0.9734 | 0.56 | 0.83 | 0.67 | 0.956 |

### Clustering Performance
The K-Means model was evaluated on the 2D data created by PCA:

| Model | Inertia | Silhouette Score | Davies Bouldin Score |
| :--- | :--- | :--- | :--- |
| **K-Means** | 1465035668058315.5 | 0.9403 | 0.3579 |

---
**Conclusion**: For the primary goal of predicting oil spills, the **Support Vector Machine (After RandomizedSearchCV)** is the clear winner. While several models achieved high accuracy, its superior Recall (0.83) and F1-Score (0.67) make it the most reliable for identifying the rare positive class. For the task of exploratory data analysis, the **K-Means Clustering** model also performed exceptionally well, successfully identifying distinct patterns in the data.
