# KNN Handwritten Digit Classification

This project implements a handwritten digit classification system using the **K-Nearest Neighbors (KNN)** algorithm.  

---

## Project Overview

The goal of this project is to classify handwritten digits (0–9) using the KNN algorithm and analyze how different values of K affect model performance.  
The project uses the **Sklearn Digits dataset**, which contains grayscale images of handwritten digits represented as numerical feature vectors.

---

## Dataset Description

- Dataset used: `load_digits()` from Scikit-learn  
- Number of samples: 1797  
- Image size: 8 × 8 pixels  
- Number of classes: 10 (digits 0–9)  

Each image is flattened into a feature vector before being passed to the model.

---

## Methodology

1. Loaded the digit dataset using Scikit-learn.
2. Visualized sample digit images to verify labels.
3. Split the dataset into training and testing sets.
4. Applied feature scaling using `StandardScaler`.
5. Trained a K-Nearest Neighbors classifier.
6. Tested multiple values of K (3, 5, 7, 9).
7. Evaluated model performance using accuracy.
8. Visualized results using:
   - Accuracy vs K graph  
   - Confusion matrix  
   - Predicted digit outputs  

---

## What I learned 

K-Nearest Neighbors is a distance-based classification algorithm that assigns a class to a data point based on the majority class of its nearest neighbors. The value of **K** represents the number of nearest data points considered during classification.

During this project, it became clear that choosing the correct value of K is important. A very small value of K makes the model highly sensitive to noise, which can lead to overfitting. On the other hand, a very large value of K can cause underfitting by oversmoothing the decision boundaries. By testing multiple values of K, the optimal balance between bias and variance was observed.

Feature scaling played a crucial role in improving model performance. Since KNN relies on distance calculations, features with larger numerical values can dominate the distance metric if scaling is not applied. Standardization ensures that all features contribute equally to distance computation.

The distance metric used in this project is **Euclidean distance**, which measures the straight-line distance between two points in multidimensional space. It is commonly used in KNN because of its simplicity and effectiveness for continuous numerical data.

The confusion matrix provided insights into classification errors and helped identify which digits were misclassified most frequently. This helped in understanding the limitations of the model and evaluating its real-world performance.

Although KNN is simple and effective for small datasets, it has some limitations. It requires high memory usage because it stores the entire dataset, and prediction time increases with dataset size. Additionally, its performance heavily depends on proper feature scaling and the choice of K.

---

## Results

- Achieved high classification accuracy on test data
- Observed optimal performance at specific K values
- Successfully visualized classification results and errors
- Demonstrated working of distance-based classification
