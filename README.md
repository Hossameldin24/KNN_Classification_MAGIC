﻿# KNN Classification for MAGIC telescope dataset

This project focuses on the classification of gamma-ray events and hadron events detected by a Cherenkov gamma telescope. The dataset used in this project simulates the detection of high-energy gamma particles, with two classes: **gamma (signal)** and **hadron (background)**. The primary goal is to balance this imbalanced dataset and classify the events using a k-Nearest Neighbors (k-NN) classifier.

## Dataset Overview
The MAGIC Gamma Telescope dataset consists of two classes:
- **Gamma Events**: 12,332 samples
- **Hadron Events**: 6,688 samples

Due to the class imbalance, preprocessing steps were required to ensure both classes have equal representation.

## Project Goals

1. **Balance the Dataset**: Address the class imbalance by downsampling the gamma events to match the number of hadron events.
2. **Split the Dataset**: Randomly split the data into:
   - **Training Set**: 70%
   - **Validation Set**: 15%
   - **Testing Set**: 15% (used solely for final evaluation)
3. **Apply k-NN Classification**: 
   - Train a k-Nearest Neighbors (k-NN) classifier on the dataset.
   - Experiment with different values of `k` to determine the optimal classifier.
4. **Evaluate Models**: 
   - Assess each model's performance in terms of accuracy, precision, recall, F1-score, and the confusion matrix.
   - Compare results for different `k` values and interpret the findings.

## Project Structure

- `data/`: Contains the dataset files (balanced, split into training, validation, and testing sets).
- `src/`: Includes the code for loading data, preprocessing, training, and evaluation.
- `notebooks/`: Jupyter notebooks with detailed exploratory data analysis (EDA) and model evaluation.
- `results/`: Stores results, such as confusion matrices, classification reports, and performance metrics.

## Code and Usage

### Prerequisites
Ensure you have the following packages installed:
```bash
pip install numpy pandas scikit-learn

Evaluation Metrics
Accuracy: The ratio of correctly classified samples to the total samples.
Precision: Measures the proportion of true positive results among the positive predictions.
Recall: The ratio of correctly classified positive samples to the total positive samples.
F1-Score: The harmonic mean of precision and recall.
Confusion Matrix: A matrix representation showing the counts of true positive, true negative, false positive, and false negative results.
Results and Analysis
Best k Value:

Different values of k were tested to achieve the best balance between accuracy and overfitting.
Optimal k value, as well as its detailed evaluation metrics, are discussed in results/summary.txt.
Model Comparison:

A comprehensive analysis of model performance for various k values is provided, with insights into the trade-off between bias and variance as k changes.
Conclusion
The results of the k-NN classifier for different values of k have been compared and analyzed. This project serves as a practical exploration of balancing techniques, data splitting, and model evaluation using fundamental classification metrics.
