# Food Order Prediction using Machine Learning

## Project objective
Predict the most likely cuisine type for a food order using customer and order-context features from Vijayawada.

## Dataset
The project uses `vijayawada_food_orders_dataset.csv`, a reproducible synthetic dataset containing 10,000 records and 8 categorical columns. It is intended for educational use and does not represent real customer data.

## Models
1. K-Nearest Neighbors (KNN)
2. Logistic Regression
3. Decision Tree
4. Random Forest

## How to run
1. Extract the ZIP.
2. Open the folder in Jupyter Notebook, JupyterLab, or VS Code.
3. Install dependencies with `pip install -r requirements.txt`.
4. Run `Dataset_Generation.ipynb` only if you want to regenerate the dataset.
5. Run the four model notebooks.
6. Run `Model_Comparison.ipynb` for the final comparison.

## Important
- All models use the same 80/20 stratified train/test split (`random_state=42`).
- Categorical encoding is fitted inside each scikit-learn pipeline, preventing test-set leakage.
- Report the metrics produced by the notebooks; no performance value is hard-coded.
- The dataset is synthetic, so results should not be interpreted as real-world restaurant demand performance.
