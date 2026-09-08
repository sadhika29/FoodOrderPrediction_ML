# 🍔 Food Order Prediction using Machine Learning

## 📌 Project Overview

Food Order Prediction is a Machine Learning project that predicts the **cuisine type** of a food order based on customer and order-related information.

The project implements and compares four supervised Machine Learning classification algorithms:

- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**

The main objective is to preprocess the food-order data, train multiple classification models, evaluate their performance, compare the results, and identify the most suitable model for the prediction task.

> **Note:** The dataset used in this project is a synthetic educational dataset created to demonstrate the complete Machine Learning workflow.

---

## 🎯 Objectives

- Analyze food-order-related data.
- Perform data validation and preprocessing.
- Convert categorical data into numerical features.
- Build multiple Machine Learning classification models.
- Evaluate each model using standard performance metrics.
- Compare all models using the same dataset and preprocessing procedure.
- Identify the best-performing model.
- Predict the cuisine type for a new food-order profile.

---

## 📊 Dataset

The dataset contains **10,000 food-order records** and **8 columns**.

### Features

| Feature | Description |
|---|---|
| Gender | Gender category of the customer |
| Age_Group | Age category of the customer |
| Marital_Status | Marital status of the customer |
| Income_Level | Customer income category |
| Time_of_Day | Time period of the order |
| Day | Day on which the order was placed |
| Location | Customer/order location |
| Cuisine_Type | Target cuisine category |

### Target Variable

**Cuisine_Type**

The target contains the following cuisine categories:

- Bakery
- Biryani
- Chinese
- Continental
- Fast Food
- North Indian
- South Indian
- Street Food

---

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Validation
   ↓
Data Preprocessing
   ↓
One-Hot Encoding
   ↓
Target Encoding
   ↓
Stratified 80:20 Train-Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Best Model Selection
   ↓
Cuisine Prediction
```

---

## 🛠️ Data Preprocessing

The following preprocessing steps were performed:

1. Checked the dataset dimensions.
2. Checked for missing values.
3. Checked for duplicate records.
4. Separated input features and target variable.
5. Applied **Label Encoding** to the target variable.
6. Applied **One-Hot Encoding** to categorical input features.
7. Used a **stratified 80:20 train-test split**.
8. Used the same preprocessing pipeline for all models to ensure a fair comparison.

---

## 🤖 Machine Learning Algorithms

### 1. K-Nearest Neighbors (KNN)

KNN is a distance-based classification algorithm. It predicts the class of a new data point by examining the nearest training examples and assigning the most suitable class.

### 2. Logistic Regression

Logistic Regression is a classification algorithm that estimates the probability of an input belonging to different classes. It is efficient and works well when the relationships between encoded features and target classes can be represented effectively.

### 3. Decision Tree

A Decision Tree predicts the target by creating a sequence of decision rules based on the input features. It is easy to understand and interpret.

### 4. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple Decision Trees. Each tree produces a prediction and the forest combines these predictions to produce the final classification.

---

## 📈 Model Performance

All four algorithms were evaluated using the **same dataset, preprocessing pipeline, and stratified 80:20 train-test split**.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| K-Nearest Neighbors (KNN) | 53.45% | 53.70% | 53.45% | 53.42% |
| Logistic Regression | **66.20%** | **67.37%** | 66.20% | 65.76% |
| Decision Tree | 59.10% | 59.40% | 59.10% | 58.67% |
| Random Forest | **66.20%** | 67.19% | 66.20% | **65.80%** |

---

## 🏆 Best Performing Model

### Logistic Regression — 66.20% Accuracy

**Logistic Regression was selected as the best-performing model for this project.**

Logistic Regression and Random Forest achieved the **same highest accuracy of 66.20%**. However, Logistic Regression achieved a slightly higher weighted precision:

- **Logistic Regression:** 67.37%
- **Random Forest:** 67.19%

Therefore, Logistic Regression was selected as the best model based on the overall model comparison and ranking used in the project.

### Why did Logistic Regression work best?

The dataset mainly contains categorical customer and order-related features. These features were converted into numerical representations using **One-Hot Encoding**.

After encoding, Logistic Regression was able to learn useful relationships between the feature combinations and the different cuisine classes. It also provides a simple, efficient, and interpretable classification approach.

Random Forest performed almost identically and achieved the same accuracy, showing that it was also effective for this dataset. However, Logistic Regression had slightly higher weighted precision and was selected as the final model.

---

## 📊 Evaluation Metrics

### Accuracy

Measures the percentage of correctly classified food orders.

### Precision

Measures how many of the orders predicted as a particular cuisine actually belong to that cuisine.

### Recall

Measures how many of the actual orders belonging to a cuisine were correctly identified.

### F1-Score

Provides a balance between precision and recall.

### Confusion Matrix

Shows the number of correct and incorrect predictions for each cuisine category.

---

## 🔮 Example Prediction

The trained best-performing model can be used to predict the cuisine type for a new food-order profile.

Example input:

```text
Gender: Female
Age Group: 25-34
Marital Status: Single
Income Level: Upper-Middle
Time of Day: Dinner
Day: Saturday
Location: MG Road
```

The trained model then predicts the most likely **Cuisine_Type** for the given customer/order profile.

---

## 📓 Google Colab

The complete project is available as a single Google Colab-ready notebook containing the complete workflow from dataset loading and preprocessing to model training, evaluation, comparison, and prediction.

👉 [**Open the Complete Project in Google Colab**](https://colab.research.google.com/github/sadhika29/FoodOrderPrediction_ML/blob/main/Food_Order_Prediction_Complete_Colab.ipynb)

---

## 📁 Project Structure

```text
FoodOrderPrediction_ML/
│
├── Food_Order_Prediction_Complete_Colab.ipynb
├── Dataset_Generation.ipynb
├── KNN.ipynb
├── LogisticRegression.ipynb
├── DecisionTree.ipynb
├── RandomForest.ipynb
├── Model_Comparison.ipynb
├── vijayawada_food_orders_dataset.csv
├── requirements.txt
└── README.md
```

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Google Colab
- GitHub

---

## ▶️ How to Run

### Google Colab

1. Open the Google Colab link provided above.
2. Open the complete notebook.
3. Run the cells from top to bottom.
4. The notebook loads the dataset and performs the complete Machine Learning workflow.

### Local Environment

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open the notebooks using Jupyter Notebook or VS Code.

---

## 📌 Results and Conclusion

The project successfully demonstrates the use of four supervised Machine Learning classification algorithms for predicting food cuisine types.

The final accuracy results are:

- **KNN:** 53.45%
- **Logistic Regression:** 66.20%
- **Decision Tree:** 59.10%
- **Random Forest:** 66.20%

**Logistic Regression was selected as the best-performing model**, achieving **66.20% accuracy** and **67.37% weighted precision**.

Random Forest achieved the same accuracy of **66.20%** and performed very closely to Logistic Regression.

The comparison demonstrates that different Machine Learning algorithms can produce different results on the same classification problem, and evaluating multiple models helps identify a suitable algorithm for the given dataset.

---

## 🚀 Future Enhancements

The project can be further improved by:

- Using a larger real-world food-order dataset.
- Collecting actual historical customer order data.
- Performing more extensive hyperparameter tuning.
- Applying additional feature engineering.
- Testing additional classification algorithms.
- Using cross-validation for more robust model evaluation.
- Deploying the trained model as a web application.
- Adding a user interface for real-time cuisine prediction.
- Monitoring model performance after deployment.

---

## 👩‍💻 Author

**Sadhika Mahammad**

GitHub: 
