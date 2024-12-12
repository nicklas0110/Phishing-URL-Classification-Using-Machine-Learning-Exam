# **Phishing URL Classification Project**

This project was completed as part of a machine learning exam. The goal is to classify URLs as either phishing or legitimate using structured data from the PhiUSIIL Phishing URL Dataset. Two machine learning models, Random Forest and Multilayer Perceptron (MLP), were trained, fine-tuned, and compared.

## **Dataset**
- **Name:** PhiUSIIL Phishing URL Dataset
- **Size:** 235,795 samples with 56 features
- **Target Variable:** `label` (1 for phishing, 0 for legitimate)

## **Project Overview**
1. **Data Preprocessing:**
   - Removed irrelevant columns such as `FILENAME` and `URL`
   - Encoded categorical variables
   - Standardized numerical features

2. **Models Used:**
   - **Random Forest:**
     - An ensemble learning model that aggregates multiple decision trees for robust predictions.
     - **Fine-Tuned Hyperparameters:**
       - `n_estimators=100` (number of trees)
       - `max_depth=None` (unlimited depth)
       - `min_samples_split=2` (minimum samples to split)
       - `min_samples_leaf=1` (minimum samples at leaf node)

   - **Multilayer Perceptron (MLP):**
     - A neural network with fully connected layers to capture complex patterns.
     - **Fine-Tuned Hyperparameters:**
       - `hidden_layer_sizes=(50, 50)` (two hidden layers with 50 neurons each)
       - `activation='relu'` (activation function for non-linearity)
       - `alpha=0.001` (regularization term)
       - `learning_rate_init=0.01` (initial learning rate)

3. **Model Comparison:**
   - Random Forest achieved a cross-validation accuracy of 100%.
   - MLP achieved a cross-validation accuracy of 99.99%.
   - Random Forest performed slightly better due to its simplicity and robustness with structured data.

## **Usage**
1. Clone this repository:
   ```bash
   git clone <repository-link>
   cd <repository-folder>
   ```
2. Ensure Python and required libraries are installed.
3. Run the provided Jupyter Notebook or Python script to replicate results.

## **Key Results**
- Random Forest and MLP models both demonstrated excellent performance.
- Fine-tuned models provided high accuracy and reliable predictions.

## **Repository Contents**
- **`main.py`:** Main Python script for training and evaluating models.
- **Dataset:** The PhiUSIIL dataset should be in the working directory.
- **Results:** Outputs include model reports and confusion matrices.