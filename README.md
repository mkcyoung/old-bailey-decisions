# old-bailey-decisions

[View project on kaggle](https://www.kaggle.com/c/uofu-ml-fall-2020/overview)

[Leaderboard (#2 out of 103)](https://www.kaggle.com/c/uofu-ml-fall-2020/leaderboard)

[Project report](Project-Final-Report.pdf)

## Predicting trial decisions from transcripts.

The Old Bailey is the colloquial name for the Central Criminal Court of England and Wales, which deals with with major criminal cases in Greater London, and also sometimes from the rest of England and Wales. This court has existed in some form or another since the 16th century. The proceedings of this court have been digitized and available online via the Old Bailey Proceedings Online project.

### Task definition
Since all the text of the trials from 1674 to 1913 are available, we can ask the following text classification question: **Can we predict the decision of the court using the transcribed dialogue during a trial?**

The goal of this project is to explore classifiers that predict the outcomes of trials. That is, the instances for classification are the transcripts of trials, and the labels are either guilty (denoted by 0) or not guilty (denoted by 1).

## The Data
The transcribed dialogue was provided to us in the form of 3 preprocessed feature sets:   
1. **Bag of words:** A 10,000 element vector in which each dimension corresponds to a word and the value stored corresponds to how many times that word appeared in the court dialogue. The 10,000 words represented were the 10,000 most frequently used across all the cases.
2. **TF-IDF:** A remix of bag-of-words where instead of the counts being stored for each word, a value that seeks to capture how relevant a word is to a document is stored. Once again, the top 10,000 words were considered.
3. **GLOVE:** The average of each word’s “embedding” in the document, weighted by the word’s tf-idf score. Each example was a 300 dimensional vector.   

Additionally, we were provided with a metadata set consisting of 6 facts about the trial (such as age and gender of the defendant). This data was not preprocessed. I processed this metadata set by converting each feature to a one hot encoding. For the numeric data (age + number of victims), I binned using ranges that I thought would lead to compelling categories. Later, in an effort to improve my results, I binned these variables using quantile binning. 

## Algorithms

To tackle the task at hand, I implemented the following algorithms from scratch:
1. [Perceptron](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/perceptron/perceptron_v2.ipynb)
2. [Support Vector Machine (SVM)](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/svm/SVM.ipynb)
3. [Logistic Regression](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/ensemble/logistic_regression.ipynb)
4. [Decision Tree](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/decision%20tree/dec_tree_v1.ipynb)   
 
Additionally, I used XGBoost, scikit-learn, and PyTorch to implement these algorithms:  
1. [Neural Network](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/neural%20net%20and%20random%20forest/pytorch.ipynb)
2. [Random Forrest](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/neural%20net%20and%20random%20forest/pytorch.ipynb)
3. [XGBoost](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/gradient%20boosting/XGBoost.ipynb)
  
Ultimately, an [ensemble](https://github.com/mkcyoung/old-bailey-decisions/blob/main/code/ensemble/logistic_regression.ipynb) of Perceptron, Logistic Regression, and SVM yielded the best performance on the evaluation set and resulted in 2nd place in the final standings.

## Acknowledgements
