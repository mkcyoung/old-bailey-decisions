# old-bailey-decisions

[View project on kaggle](https://www.kaggle.com/c/uofu-ml-fall-2020/overview)

[View leaderboard](https://www.kaggle.com/c/uofu-ml-fall-2020/leaderboard)

[Project report](Project-Final-Report.pdf)

## Predicting trial decisions from transcripts.

The Old Bailey is the colloquial name for the Central Criminal Court of England and Wales, which deals with with major criminal cases in Greater London, and also sometimes from the rest of England and Wales. This court has existed in some form or another since the 16th century.

The proceedings of this court have been digitized and available online via the Old Bailey Proceedings Online project. From the project website:

The Old Bailey Proceedings Online makes available a fully searchable, digitised collection of all surviving editions of the Old Bailey Proceedings from 1674 to 1913, and of the Ordinary of Newgate's Accounts between 1676 and 1772. It allows access to over 197,000 trials and biographical details of approximately 2,500 men and women executed at Tyburn […].

Task definition
Since all the text of the trials from 1674 to 1913 are available, we can ask the following text classification question: Can we predict the decision of the court using the transcribed dialogue during a trial?

The goal of this project is to explore classifiers that predict the outcomes of trials. That is, the instances for classification are the transcripts of trials, and the labels are either guilty (denoted by 0) or not guilty (denoted by 1).

To this end, you will use various feature representations of the data (including ones you may develop) and the different learning algorithms we see in class.

## Acknowledgements


