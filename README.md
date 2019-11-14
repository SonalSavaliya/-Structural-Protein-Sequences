# Structural-Protein-Sequences

My aim is to classify maximum protein types in the Structural Protein Sequences dataset using multiple machine learning classification algorithms. The dataset is from [Kaggle](https://www.kaggle.com/shahir/protein-data-set).

## Data Preprocessing
  - Format the classification names 
  - Remove the outliers for phValue and Molecular Weight. However, there are some high values in Molecular Weight which I think "Molecular weight is calculated using sequence using the weight of each amino acid. Thus, if a sequence is long, then it can have a large weight" 
  - Remove crystallizationMethod, crystallizationTempK, publicationYear and pdbxDetails. crystallizationMethod and crystallizationTempK have 22% missing values
  - Drop some rows based on : densityMatthews, densityPercentSol, resolution, and sequence
  - Replace phValue nan value with the average value of that particular class and remove all classes if all phValues are null
  - Didn't consider classes that have less than 100 values per class
  - Added class variable as a target value. Assign a unique class number to each protein class

## Data Analysis

I compared a few models with cross-validation and hyperparameter tuning with Grid Search and Randomized Search. The following models were compared:
- Random Forest
- Decision Tree
- Gradient Boosting
- Gaussian Naive Bayes
- Multinomial Naive Bayes
- Support Vector Machine (SVM)
- K Nearest Neighbors (KNN)


Random Forest is the best among all above models. KNN also works well whereas all other models give very poor performance. 

#### Future Work
 - Will build deep learning models
