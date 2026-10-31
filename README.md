# 🥛 Milk Quality Classification Using Machine Learning

## 📌 Project Overview

This project uses Machine Learning classification algorithms to predict the quality of milk based on its physical and sensory characteristics.

The goal is to classify milk into three quality categories:

- **Low**
- **Medium**
- **High**

I explored and compared multiple classification algorithms, including Logistic Regression, Decision Tree, Gradient Boosting, and XGBoost. I also experimented with XGBoost hyperparameters to evaluate model performance.

## 📊 Dataset

The dataset contains **1,059 records** and **8 columns**.

### Features

| Feature | Description |
|---|---|
| `ph` | pH level of the milk |
| `temperature` | Milk temperature |
| `taste` | Good (1) or Bad (0) |
| `odor` | Good (1) or Bad (0) |
| `fat` | Optimal (1) or Not optimal (0) |
| `turbidity` | High (1) or Low (0) |
| `colour` | Colour value of the milk |
| `grade` | Target variable: Low, Medium, High |

**Target encoding:**
- Low → 0
- Medium → 1
- High → 2

**Dataset source:** [Milk Quality Dataset – Kaggle](https://www.kaggle.com/datasets/cpluzshrijayan/milkquality/data)

## 🛠️ Technologies and Libraries

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

## 🔍 Project Workflow

### 1. Data Preparation
- Loaded the dataset using Pandas.
- Checked the dataset shape and previewed records.
- Checked for missing values.
- Encoded the target variable.
- Selected input features and target variable.

### 2. Exploratory Data Analysis (EDA)
- Visualized pH distribution.
- Visualized temperature distribution.
- Used histograms to understand feature distributions.

### 3. Model Training

The dataset was divided into:
- Training set: 70%
- Testing set: 30%

The split used `random_state=43`.

I trained and evaluated four classification algorithms:

1. Logistic Regression
2. Decision Tree Classifier
3. Gradient Boosting Classifier
4. XGBoost Classifier

### 4. XGBoost Hyperparameter Experimentation

I experimented with the following XGBoost parameters:

| Parameter | Value |
|---|---:|
| `n_estimators` | 100 |
| `max_depth` | 5 |
| `learning_rate` | 0.1 |
| `colsample_bytree` | 0.5 |

I evaluated the tuned model using:
- Accuracy
- Classification Report
- Confusion Matrix

## 📈 Model Performance

The following accuracy scores are based on the classification reports saved in the notebook.

| Model | Test Accuracy |
|---|---:|
| Logistic Regression | 73% |
| Decision Tree | 99% |
| Gradient Boosting | 100% |
| XGBoost | 100% |
| Tuned XGBoost | 100% |

**Note:** These are results from a single 70/30 train-test split. Further cross-validation and testing on unseen data would help assess how well the models generalize.

## 💡 Key Learnings

Through this project, I gained practical experience in:

- Preparing and exploring a classification dataset.
- Handling categorical target encoding.
- Training and comparing multiple Machine Learning models.
- Understanding ensemble learning techniques.
- Implementing Gradient Boosting and XGBoost.
- Experimenting with XGBoost hyperparameters.
- Evaluating classification models using precision, recall, F1-score, and confusion matrices.

## 🚀 Future Improvements

- Apply cross-validation for more reliable evaluation.
- Perform feature importance analysis.
- Experiment with additional hyperparameter tuning.
- Investigate model generalization and potential overfitting.
- Compare models using additional evaluation metrics.

## ▶️ How to Run the Project

1. Clone this repository:

   ```bash
   git clone YOUR_REPOSITORY_URL
   ```

2. Navigate to the project folder:

   ```bash
   cd Milk-Quality-Classification
   ```

3. Install the required libraries:

   ```bash
   pip install pandas matplotlib seaborn scikit-learn xgboost jupyter
   ```

4. Make sure `milk_quality_data.csv` is in the project folder.

5. Open the Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. Run the notebook cells to reproduce the analysis and model training.

## 🙏 Acknowledgment

Thanks to **Codebasics** for the Machine Learning learning resources and practical guidance.

Dataset credit: [shrijayan – Kaggle](https://www.kaggle.com/datasets/cpluzshrijayan/milkquality/data)

---

⭐ If you find this project useful, feel free to explore the repository!
