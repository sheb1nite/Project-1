### Identify semantically duplicate questions using Machine Learning

### Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-soures)
- [Objectives](#objectives)
- [Data Collection](#data-collection)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Description of Columns](#description-of-columns)
- [Feature Engineering](#feature_engineering)
- [Machine Learning Models](#machine-learning-models)
- [Model Evaluation](#model-evaluation)
- [Results](#results)


### Project Overview
In this project, taking Quora for our case study, we explored and applied different machine
learning and deep learning techniques on the task of identifying duplicate questions on Quora’s
question pair dataset. By using feature engineering, feature importance techniques, and machine
learning algorithms that include Random Forest and XGBoost.

### Data Sources
Question Pairs Data: The primary dataset for this project is [Download here](https://www.kaggle.com/c/quora-question-pairs), containing detailed information about question pairs available on Quora.

### Objectives
1. Collect and preprocess a large dataset of questions from online forums and
question-answering websites, such as Quora, that are labeled as semantically similar or
not.
2. Develop and evaluate machine learning models, such as Random Forest and XGBoost, to
accurately identify semantically similar questions based on their text.
3. Implement natural language processing techniques, such as word embeddings and
semantic similarity measures, to improve the accuracy of the machine learning models.
4. Evaluate the performance of the machine learning models using appropriate metrics, such
as precision, recall, F1 score, and accuracy.
5. Compare the performance of different models and techniques to identify the most
effective approach for identifying semantically duplicate questions.
6. Use the developed approach to identify and group semantically similar questions on
online forums and question-answering websites, such as Quora, to improve the efficiency
and accuracy of information retrieval systems.

### Data Collection
The data for this research work is taken from the First Quora Dataset release hosted on Amazon
S36 . There is a total of 404351 rows and 6 columns in the dataset, which also indicates that
there are total 404351 question pairs.

### Exploratory Data Analysis
Performed the necessary statistics on the dataset, which helps us to give a more detailed
understanding of the duplicate Quora question dataset. There is a total of six columns in the
dataset. Each of the columns is meaningful and describe the characteristic of the row.

### Description of Columns
● id: A unique identifier assigned to each row in the dataset. The first row has an id of 0,
and the last row has id 404351
● qid1: A unique identifier for the question in question1 column.
● qid2: A unique identifier for the question in question2 column.
● question1 and question2: contains the questions that has to be compared.
● is_duplicate: is_duplicate is the result of a semantical comparison of question pair.
0 indicates false i.e. question pair is not duplicate and
1 indicates true i.e. question pair is duplicate.

### Feature Engineering 
The initial raw dataset had a total 6 columns, which included columns such as id, qid1, qid2,
question1 and question2. To make the dataset more useful, we dropped the first three columns
and added 12 new derived features. Therefore, we have a total of 15 columns in dataset provided
as input to the machine learning classifiers.

### Machine Learning Models
We have used two machine learning classifiers Random Forest and XGBoost and also a
statistical feature TF-IDF.

### Model Evaluation
Evaluation metrics include Accuracy, F1 Score, Precision and Recall.

### Results 
We ensure that, the train and test data is split into 80/20 respectively throughout the experiments.
We also ensure that the class labels in the test data set has proportionate distribution of samples
as in our original dataset. All the hyper-parameters are selected based on grid search performed
on the 10% of dataset from the training set, thus we ensure that our result do not suffer from
overfitting. Our results with TF-IDF and ML classifiers show that not all models performed well
in ensemble with TF-IDF character level, but our best model Random Forest achieved the
accuracy of 82.4 % and F1 score of 0.706. This has demonstrated that machine learning models
are efficient in solving natural language problem of detecting semantically similar question
