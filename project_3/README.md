# Project 3: Predicting Reddit Post Membership in r/ADHD and r/OCD using NLP and Classification Modeling

## Executive Summary

ABC Research Group was tasked with creating a chat bot for its client, the Department of Psychology of the National University of Singapore, using NLP to correctly predict the nature of enquirers' problems and to accurately direct them to the right staff-on-hand for the purpose of reducing the need for paid volunteer staff and costly miscategorized enquiries.

In Phase I of this project, a model trained on posts in Reddit's r/ADHD and r/OCD subreddit post data predicted that posts belonged to either subreddit with an accuracy of nearly 90% utilizing lemmatized text, sklearn's TF-IDF Vectorizer and Multinomial Naive Bayes classifier. This model was also better at inference than a competing model using sklearn's Count Vectorizer and Logistic Regression. Data from reddit was used in absence of prior data from the Department itself.

Our process is summarized as such:

1. Data from r/ADHD and r/OCD is scarped and then wrangled.
2. Duplicated data is removed from our dataset. Text-based data we will use for NLP is merged into a single column.
3. Data is lemmatized and stop words removed.
4. Data is processed via a combination of algorithm models using TF-IDF/Count Vectorizers, and the Multinomial Naive Bayes and Logistic Regression classifiers.
5. Important words and patterns in predictive features were analyzed for insights into the data.

While the Phase I model is sufficient for understanding the context of each enquiry if it pertains to ADHD or OCD, other algorithms will have to be utilized to if classifications are to be more fine. For example, whether to direct an enquirer who is already diagnosed and simply needs to buy medicine for his condition, or if it is a enquirer who has yet to see a professional for a diagnosis attempting to find out more about the condition he believes he has.