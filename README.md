# Task-7-Support-Vector-Machines-SVM

1.Load and prepare a dataset for binary classification.

2.Train an SVM with linear and RBF kernel.

3.Visualize decision boundary using 2D data.

4.Tune hyperparameters like C and gamma.

5.Use cross-validation to evaluate performance.

---

# Objective:
Use SVMs for linear and non-linear classification.

---
# Tools:
Scikit-learn, NumPy, Matplotlib

---

# Code Explanation 

---

 1. Import Libraries

Imported necessary Python libraries:

pandas, numpy for data manipulation.

matplotlib, seaborn for visualizations.

scikit-learn tools for model building, scaling, evaluation, and PCA.




---

 2. Load and Prepare Dataset

Loaded the Breast Cancer dataset from a CSV file.

Dropped unnecessary columns like id if present.

Converted the diagnosis column:

'M' (Malignant) → 1

'B' (Benign) → 0 (binary classification)


Separated:

Features (X)

Target (y)




---

 3. Data Visualization (EDA)

Class Distribution: Used a bar chart to show the number of malignant vs benign cases.

Correlation Heatmap: Plotted correlations between all features to identify strong linear relationships.



---

 4. Split and Standardize the Data

Used an 80/20 train-test split to evaluate model performance on unseen data.

Applied standardization using StandardScaler:

Ensures all features have zero mean and unit variance.

Necessary for SVMs to perform effectively.




---

 5. Train Linear SVM

Trained an SVM classifier with a linear kernel.

Made predictions on the test set.

Evaluated performance using:

Accuracy

Classification Report (Precision, Recall, F1-score)

Confusion Matrix (though not shown graphically here)




---

 6. Train SVM with RBF Kernel

Trained another SVM with a Radial Basis Function (RBF) kernel.

This kernel handles non-linear decision boundaries.

Again, evaluated performance using classification metrics.



---

 7. Visualize Decision Boundary using PCA

Used Principal Component Analysis (PCA) to reduce feature dimensions to 2D for visualization.

Trained an RBF SVM on the PCA-transformed data.

Created a contour plot:

Shows how the SVM separates classes in 2D.

Each region colored by predicted class.

Actual data points plotted on top.




---

 8. Hyperparameter Tuning with GridSearchCV

Used GridSearchCV to find best C and gamma values for RBF kernel.

C controls margin hardness.

gamma defines influence of single training example.


Used 5-fold cross-validation during tuning.

Displayed the mean test scores as a heatmap for better visualization of hyperparameter impact.



---

 9. Evaluate Tuned SVM

Used the best model obtained from GridSearchCV to predict on test data.

Printed full classification report.

Showed improved accuracy compared to default models.



---

 10. Cross-Validation Accuracy

Used cross_val_score on the full dataset with the best SVM model.

Calculated and printed:

All fold accuracies.

Mean accuracy (overall generalization performance).




---

 11. Compare Model Accuracies (Visualization)

Plotted a bar chart comparing:

Linear SVM accuracy

RBF SVM accuracy

Tuned (best) SVM accuracy





---


