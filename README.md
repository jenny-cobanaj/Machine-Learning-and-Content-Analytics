# MBTI Personality Prediction Project


## Table of contents

* Introduction

* Our Project

* The MBTI

* Data

* Methodology

* Conclusion

* Notebooks

* Authors


## Introduction

The way that a person behaves in a particular situation or under particular conditions is commonly studied and supervised by many areas of research. For instance, the situation and condition may vary but lead to an inference of personality indicator. Currently many personality tests are available and used by recruiters and companies, universities and other fields to access someone’s behavior and identifying human personality. Among the most known ones are the Myers-Briggs Type Indicator, the DISC personality test and the Caliper Profile one. In this current era of rise in Artificial Intelligence and Machine Learning many algorithms have been developed and trained to make such predictions in Natural Language Processing and Text classification with a very high level of accuracy.


## Our Project

The main idea of this project is to classify people into their Myers-Briggs Type Index (MBTI) personality type (output) based on text samples (input) from their posts in social media, employing Machine Learning algorithms such as Logistic Regression and XGBoost, and Deep Learning techniques such as Convolutional Neural Networks and Transformers and evaluating the accuracy of these models and their ability to predict the Myers-Briggs Personality Indicator. In other words, we will work on building models in order to detect a person’s personality type in connection to his style of writing. Focusing on the business aspect of the project, we are mainly aiming at two ends. Firstly, to provide a solution that will improve the performance of online marketing, since, identifying personality types will help companies to build more efficient targeted campaigns reducing the advertising costs and increasing their revenues at the same time. Secondly, we want to assess how reliable are these tests in the process of evaluation of a particular candidate’s personality by theirs answers in these type of assessments. Generally, we wanted to build a more generalizable system that can incorporate meaning of writing to determine overall personality types.


## The MBTI

![183bfb8961470846df475ba48e41bbd3-1024x768-1](https://user-images.githubusercontent.com/112647046/188272224-03464cd9-e23d-4e18-a4ab-c3bf423fa91b.png)


Focusing on the sixteen different types of personality, the dichotomies are Extraversion-Introversion, Sensing-Intuition, Thinking-Feeling, and Judging-Perceiving as we can also see from Figure 2, which they are usually represented by their first letter with “N” standing for Intuition. Analyzing the aforementioned dichotomies, the E-I dichotomy describes how people respond and interact with the world around them with extraverts being action-oriented, enjoying social interaction and the introverts being thought-oriented, enjoying deeper/meaningful social interactions [4]. In addition, S-N dichotomy is looking at how people gather information from the world around them, with sensing people preferring to focus on facts and enjoying hands-on experience, while those who prefer intuition enjoy thinking abstract theories and imagining the future. Following the T-F dichotomy, it focuses on how people make decisions based on the information gathered from their sensing or intuition functions. In specific, thinking personalities prefer to make consistent decisions based on logical reasoning while feeling personalities are attached to their emotions. In contrast with the E-I, S-N and T-F which are independent of each other, J-P was found to have link with at least one of the previous dichotomies. The J-P scale focuses on how people tend to deal with the outside world with judging personalities prefer structure and robust decisions, while perceiving personalities are more supple and protean.


## Data

The actual data source that our personality type dataset came from is [Kaggle](https://www.kaggle.com/datasets/datasnaek/mbti-type). It consists of 8675 unique observations (people) and two “attributes”. Every person is accompanied by its’ Myers-Briggs personality type as a 4-letter code (1st column/type) and a collection of its’ last 50 social networking posts (2nd column/posts) coming from “PersonalityCafe” forum. Every user has undertaken a questionnaire concerning the Myers-Briggs personality test prior to joining the forum and later has been interacting in this forum with other users. Each post is separated by “|||”.



## Methodology

To find the best classifier in order to predict an individual’s personality type according to the Myers Briggs Type-Indicator, a selection of Machine Learning and Neural Network methods were used. We used a Logistic Regression as the baseline model. For a more thorough experiment and analysis we applied machine learning classical models, which we tuned, specifically a Logistic Regression and an XGBoost model. Furthermore, in this particular project, going a step further and trying to increase efficiency, we trained four types of Deep Learning Models. The models used were Feed Forward Network (FFN), Multilayer Perceptron (MLP), Recurrent Neural Networks (RNN), Convolutional Neural Networks (CNN) and the ‘DistilBert’ model, which is based on the BERT architecture. Later a comparative analysis of these classifiers was implemented. All the models were trained on the training data and evaluated using the validation set. The test was used only for the predictions of the last model, the Transformer one, which was the one with the lowest validation loss and highest accuracy scores. The evaluation results are comprised of validation accuracy, validation loss, hamming loss, Exact match ratio and ROC curves.

* Approach :

We will create a function for producing four binary target variables (4 dichotomies for the 16 different personality types), transforming the task from multiclass to multilabel. In the multilabel problem, each label represents a different classification task and in contrast with the multiclass problem, the tasks are not mutually exclusive. Thus, we will create four new columns named “Extraversion”, “Sensing”, “Thinking”, “Judging” in which, the existence of a dichotomy will be represented by “1” while the non-existence from “0”. Thus, for each column we have the first one for Extraversion (E), /Introversion (I), the second category for Sensing (S) /Intuition (N), the third for Thinking (T)/Feeling (F) and the fourth category for Judging (J)/Perceiving (P). For example, if a person has MBTI ESFJ will be represented as 1,1,0,1 in the four columns respectively. In Figure 10 we can observe the final shape of the dataset until this time.



## Conclusion

In conclusion, this project provides a solution for predicting personality, utilizing social network data with machine learning and deep learning algorithms that we applied. Beginning with the data preprocessing, we applied multiple tasks to convert the texts in a way that will hold meaningful information and in order to be treated equally, applying lowercase transformation, removing non-words, punctuations, the 4-letter code of MBTI etc. In advance, we proceeded on transforming the problem from multilabel to multiclass and on combining a custom stop word vocabulary with the NLTK package English stop words, in order to be used on the tokenization and stemming process. Then, we segregated the data for training and testing and implemented a series of Machine and Deep Learning algorithms to obtain the best accuracy results. From this project, we resulted on the Transformers model ‘DistilBert’ as the one which had the highest accuracy score in comparison to the rest, for predicting personality based on the “MBTI” personality indicator.



## Notebooks

* [EDA & Cleaning](1.EDA_Data_Cleaning.ipynb)
* [Logistic Regression & XGBoost](2.Traditional_ML_Approach.ipynb)
* [Recurrent Neural Networks](3.RNN_Models.ipynb)
* [Myltilayer Perceptron Networks](4.MLP_Models.ipynb)
* [Convolutional Neural Networks](5.CNN_Models.ipynb)
* [Transformers model](6.Transformers_Fine_Tuning.ipynb)



## Authors

* Nikos Matzakos

* [Dimitris Papageorgiou](https://github.com/jimpap1997)

* [Tzeni Tsobanaj](https://github.com/jenny-cobanaj)

