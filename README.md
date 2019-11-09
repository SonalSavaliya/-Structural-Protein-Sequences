# Structural-Protein-Sequences

My aim is to classify maximum protein types in the Structural Protein Sequences dataset using multiple machine learning classification algorithms. The dataset is from [Kaggle](https://www.kaggle.com/shahir/protein-data-set).

## Data Preprocessing
  - Format the classification names 
  - Remove the outliers for phValue and Molecular Weight. However, there are some high values in Molecular Weight which I think "Molecular weight is calculated using sequence using the weight of each amino acid. Thus, if a sequence is long, then it can have a large weight" 
  - Remove crystallizationMethod, crystallizationTempK, publicationYear and pdbxDetails. crystallizationMethod and crystallizationTempK have 22% missing values
  - Drop some rows based on : densityMatthews, densityPercentSol, resolution, and sequence
  - Replace phValue nan value with an average value of that particular class and Remove all classes if all phValues are null
  - Didn't consider classes that have less than 100 values per class
  - Added class variable as a target value. Assign a unique class number to each protein class


## Exploratory Data Analysis

Working on this part...

## Classification
 
- [x] Used RandomForest algorithm so far and it gives me 87% accuracy rate with a single random train-test split and 88% with cross-validation
- [ ] Working on other classification algorithms. I will add it soon...
