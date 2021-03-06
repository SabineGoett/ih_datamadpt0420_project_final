# -ih_datamadpt0420_project_final

![picture](./charts/film-4208954_640.jpg)

## 1) Topic

NLP project in Spanish and German - film evaluations:

The following issues will be analysed:

How well works the sentiment analysis in the spanish and german language?

Are there any differences in the evaluation of films in Spain and in Germany?


## 2) Process

**a) Data aquisition**

The evaluation of 600 films were analysed (100 most popular films (of the given evaluation) in each language and each of the following categories: drama, comedy and action)

The following information were extracted:

* _written evaluation_
* _number of stars given by the users_ 


**b) Data classification with sentiment-analysis**

The following multilingual model:  nlptown/bert-base-multilingual-uncased-sentiment was downloaded 
It is a pre-trained sequence classification model, that predicts labels (stars 1-5) to a given text. 

A program was written to label all the written evaluations with this model, so that for every film a star evaluation given by the user and a star evaluation of the same
text with the classifier is available. 

**c) Comparison of evaluation of films**

Films which are identical in the 100 best valued films in each language and of each category are extracted and compared.

## 3) Results

**a) Comparison of user evaluation and evaluation with the classifier**

The sentiment analysis works pretty well in both languages, however in this analysis it seems to work slightly better with the german evaluation. In enclosed violinplot you can see the differences in the star evaluation of the users in comparison to the star evalution gained with the classification model. 


![compare the star evaluation of users and gained by the classifier](./charts/violinplot_classifier_user.png)



In the following analysis only the star evaluation of the classifier will be used. 

**b) Differences in film evaluations on the spanish and the german website**

The choice of the 100 top films in the categories (drama, comedy and action) are different.

Only about one third of the considered films are identical among the spanish and the german evaluations. This result is similar for
all three categories. The evaluation for the films which are identical in both evaluations do not differ so much. 


![compare spanish and german film evaluation](./charts/table_comparison_of_spanish_and_german_film_evaluations.png)

**c) Comparison of films**

![compare films](./charts/drama_evaluation_sp_ge.png)

![compare films](./charts/comedy_evaluation_sp_ge.png)

![compare films](./charts/action_evaluation_sp_ge.png)


