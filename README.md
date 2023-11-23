# Salary_of_jobs
A project in unimelb COMP90049 (Introduction to Machine Learning)

In this project, you will develop and critically analyse models for predicting the the salary of jobs. That is, given a job description, gender class it falls under: balanced male-female (0) or maledominated (1) or female-dominated (2), and the predicted value: salary (mean_salary or salary_bin).

## Reading data

There are two versions of datasets.

"raw-data": the raw requirements and role in each job id.
"tfidf_data": (1) removed all stopwords and (2) only retained the 500 words in the full raw job description data set with highest TFIDF values. As a result, each job ad is now represented as a 500 dimensional feature vector, each dimension corresponding to one of the 500 words.

## Data overview

Checked the basic information of features as well as balanced labels in train and test sets. 

## Feature selection

- Used mutual information to select important features by calculating entropy between each feature and label. 
- Ranked  these features and Ploted a historgram to examine the distributions

## Supervised machine learning

- Using Logistic regression and Gaussian Naive Bayes to train labeled data

- Results: Both of two models gived similar results, with accuracies of 0.21 for GNB and 0.22 for LR. 

## Semi-supervised learning

- Definition: Giving unlabeled data a predicted label using trained ML algorithms under supervised learning.

- Purpose: Gaining more labeled data to improve the accuracy of ML algorithms

- Results: After using semi-supervised learning, both LR got slightly improvements from 0.22 to 0.23, while GNB remained the same. 
