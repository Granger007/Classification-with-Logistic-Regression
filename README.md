# **Logistic Regression Binary Classifier**

## **Overview**

This project demonstrates a **binary classification model** using **Logistic Regression** on a marketing dataset. The goal is to predict whether a customer is likely to buy a particular category of book (e.g., *Italian Cookbooks*) based on demographic and transactional data.

## **Dataset**

* **Rows**: 4000 samples
* **Features include**:

  * **Demographics** (e.g., *Gender*, *First Purchase*)
  * **Book category purchases** (e.g., *ChildBks*, *CookBks*, *ItalCook*)
  * **RFM metrics** (*Recency*, *Frequency*, *Monetary*)

## **Target Variable**

* **`target`**: Binary column indicating whether the user purchased *Italian cookbooks* (`1`) or not (`0`), derived from the `ItalCook` column.

## **Steps Implemented**

1. **Data Preprocessing**

   * Dropped non-informative columns (`ID#`, `Seq#`)
   * Converted the target variable
   * Standardized feature values using `StandardScaler`

2. **Train/Test Split**

   * 80% training, 20% testing

3. **Model Training**

   * Used `LogisticRegression` from `sklearn`

4. **Evaluation Metrics**

   * **Confusion Matrix**
   * **Precision**, **Recall**, **F1-Score**
   * **ROC-AUC Score** and **ROC Curve**

5. **Threshold Tuning**

   * Adjusted the classification **threshold** to balance precision and recall
   * Visualized **Precision-Recall vs Threshold**

## **Sigmoid Function**

Logistic regression uses the **sigmoid function** to convert linear outputs into probabilities:

$$
\sigma(z) = \frac{1}{1 + e^{-z}} 
$$

This enables **probabilistic interpretation** and **threshold-based classification**.

## **Requirements**

* **Python** 3.8+
* `pandas`
* `scikit-learn`
* `matplotlib`

## **Usage**

1. Load and preprocess the data.
2. Train logistic regression model.
3. Evaluate with default and custom thresholds.
4. Visualize performance metrics.

