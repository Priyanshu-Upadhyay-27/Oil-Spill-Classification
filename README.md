# Oil Spill Detection Using Machine Learning

![Banner Image](https<i>:</i>//i.imgur.com/your-banner-image.png) 
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

The following machine learning models were trained and evaluated:

1.  **Logistic Regression**
2.  **K-Nearest Neighbors (KNN)**
3.  **Support Vector Machine (SVM)**
4.  **Decision Tree Classifier**
5.  **Random Forest Classifier**
6.  **AdaBoost Classifier**
7.  **Gradient Boosting Classifier**

---

### 📊 Results & Metrics

**Should you show metrics in the README?**
**Yes, absolutely!** The comparison of model metrics is the core finding of your analysis. It demonstrates your ability to not only build models but also to evaluate and select the best one based on performance. It is the most important part of this project.

Here is a summary of the model performances, which you should definitely include:

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | 0.962 | 0.667 | 0.400 | 0.500 |
| **K-Nearest Neighbors** | 0.957 | 0.500 | 0.200 | 0.286 |
| **Support Vector Machine**| 0.957 | 0.000 | 0.000 | 0.000 |
| **Decision Tree** | 0.925 | 0.231 | 0.300 | 0.261 |
| **Random Forest** | 0.962 | 0.600 | 0.300 | 0.400 |
| **AdaBoost** | 0.973 | 0.800 | 0.400 | 0.533 |
| **Gradient Boosting** | 0.957 | 0.500 | 0.200 | 0.286 |

**Conclusion:** Based on the results, **AdaBoost Classifier** appears to be the most effective model for this task, showing the highest accuracy and a good balance of precision and recall.

---

### 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.
