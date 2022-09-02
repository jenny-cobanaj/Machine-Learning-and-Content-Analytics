# MBTI Personality Prediction Project


## Table of contents

* Introduction

* Our vision

* The MBTI

* Data

* Methodology

* Conclusion

* Notebooks



## Introduction

The main idea of this project is to classify people into their Myers-Briggs Type Index (MBTI) personality type (output) based on text samples (input) from their posts in social media, employing Machine Learning algorithms such as Logistic Regression and XGBoost, and Deep Learning techniques such as Convolutional Neural Networks and Transformers and evaluating the accuracy of these models and their ability to predict the Myers-Briggs Personality Indicator. In other words, we will work on building models in order to detect a person’s personality type in connection to his style of writing. Focusing on the business aspect of the project, we are mainly aiming at two ends. Firstly, to provide a solution that will improve the performance of online marketing, since, identifying personality types will help companies to build more efficient targeted campaigns reducing the advertising costs and increasing their revenues at the same time. Secondly, we want to assess how reliable are these tests in the process of evaluation of a particular candidate’s personality by theirs answers in these type of assessments. Generally, we wanted to build a more generalizable system that can incorporate meaning of writing to determine overall personality types.



## Our Vision

## The MBTI

![MBTI TYPES]/(https://github.com/jenny-cobanaj/Machine-Learning-and-Content-Analytics/blob/3a9a1cce2032ee7807274fad4a87cf4cfcb21fd8/A-chart-with-descriptions-of-each-Myers-Briggs-personality-type-24.ppm?raw=true)


Focusing on the sixteen different types of personality, the dichotomies are Extraversion-Introversion, Sensing-Intuition, Thinking-Feeling, and Judging-Perceiving as we can also see from Figure 2, which they are usually represented by their first letter with “N” standing for Intuition. Analyzing the aforementioned dichotomies, the E-I dichotomy describes how people respond and interact with the world around them with extraverts being action-oriented, enjoying social interaction and the introverts being thought-oriented, enjoying deeper/meaningful social interactions [4]. In addition, S-N dichotomy is looking at how people gather information from the world around them, with sensing people preferring to focus on facts and enjoying hands-on experience, while those who prefer intuition enjoy thinking abstract theories and imagining the future. Following the T-F dichotomy, it focuses on how people make decisions based on the information gathered from their sensing or intuition functions. In specific, thinking personalities prefer to make consistent decisions based on logical reasoning while feeling personalities are attached to their emotions. In contrast with the E-I, S-N and T-F which are independent of each other, J-P was found to have link with at least one of the previous dichotomies. The J-P scale focuses on how people tend to deal with the outside world with judging personalities prefer structure and robust decisions, while perceiving personalities are more supple and protean.


## Data

The actual data source that our personality type dataset came from is [Kaggle](https://www.kaggle.com/datasets/datasnaek/mbti-type). It consists of 8675 unique observations (people) and two “attributes”. Every person is accompanied by its’ Myers-Briggs personality type as a 4-letter code (1st column/type) and a collection of its’ last 50 social networking posts (2nd column/posts) coming from “PersonalityCafe” forum. Every user has undertaken a questionnaire concerning the Myers-Briggs personality test prior to joining the forum and later has been interacting in this forum with other users. Each post is separated by “|||”.
