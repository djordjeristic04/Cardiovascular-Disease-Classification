# Cardiovascular Disease Classification

## Project Description
This repository contains an applied artificial intelligence project focused on the classification and prediction of cardiovascular diseases in patients. The project was developed as part of the Medical Decision Systems course at the School of Electrical Engineering, University of Belgrade (academic year 2025/26). 

Timely prediction is of exceptional clinical importance, as it provides an opportunity for early prevention based on basic demographic and physiological factors.

## Dataset
The models were trained using the *Cardiovascular Disease Dataset* from Kaggle.
* **Dataset Size:** The original dataset comprises 70,000 patient records.
* **Features:** The dataset contains 13 features, including continuous variables (age, height, weight, systolic and diastolic blood pressure) and categorical/binary indicators (gender, cholesterol and glucose levels, smoking, alcohol consumption, physical activity).
* **Target Variable:** Binary classification indicating the presence (`1`) or absence (`0`) of cardiovascular disease.

## Methodology and Data Preprocessing
* **Data Cleaning:** Invalid clinical blood pressure values (less than or equal to zero) were filtered and removed from the dataset.
* **Outlier Handling:** Outliers were addressed using the IQR (Interquartile Range) approach with a clipping strategy to preserve the overall dataset size.
* **Encoding:** Categorical features were transformed using One-Hot Encoding.
* **Feature Selection & Correlation:** The top 10 most significant features were extracted using information gain, and their linear dependencies were analyzed via a Pearson correlation matrix.
* **Dimensionality Reduction:** Linear Discriminant Analysis (LDA) was applied to the entire dataset.

## Machine Learning Models
Three classification models were evaluated using Python and scikit-learn to solve this problem:
1. **Parametric Classification (Linear Classifier):** Applied on a 1D LDA projection based on the target output.
2. **Non-parametric Classification (Decision Tree):** The maximum depth was optimized to 5 levels through 5-fold cross-validation, which successfully preserved the interpretability of the decision rules.
3. **Neural Networks (MLPClassifier):** Implemented with an architecture consisting of two hidden layers (16 and 8 neurons). The model was safeguarded against overfitting by applying early stopping and L2 regularization techniques.

## How to Run

Clone the repository using `git clone https://github.com/djordjeristic04/Cardiovascular-Disease-Classification.git`, navigate into the project folder with `cd Cardiovascular-Disease-Classification`, install the required dependencies with `pip install -r requirements.txt`, and then open `Projekat.ipynb` in Jupyter Notebook or JupyterLab by running `jupyter notebook Projekat.ipynb` to execute all cells.

## Results
A comparative analysis showed that all three applied methods converged to a similar accuracy range of 72% to 73%. These results indicate that the performance ceiling for this specific feature set has been reached. The limiting factor is the informational value of the clinical data itself, rather than the capacity or complexity of the classification algorithms.

## Documentation
A comprehensive analysis of the dataset, graphical representations of correlations and LDA components, and a detailed discussion of the results for each model are available within the repository. For all theoretical and methodological details regarding the experiments, please refer to the `Izvestaj.pdf` file.

## Authors
Undergraduate students, Signals and Systems department:
* Rastko Lazarević (2023/0016)
* Đorđe Ristić (2023/0064)
