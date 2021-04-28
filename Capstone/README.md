# Capstone Project: Aspect-Based Sentiment Analysis of Luxury Hotels in Singapore


Online hotel reviews are part of a paradigm shift which have affected hotels' reputations, and subsequently their bottom lines since the early 2000s. They are written by the hotels' visitors with the intent of addressing other potential visitors. Potential visitors to the hotel often consider reviews when making their choices of place to stay. For hotel management, online reviews are a valuable source of feedback from their guests. While good reviews encourage more people to stay, so do negative reviews drive people away. [(Source)](https://www.researchgate.net/publication/291164180_Understanding_the_Impact_of_Online_Reviews_on_Hotel_Performance_An_Empirical_Analysis)

## Problem Statement
The management of online reviews is a subset of what is called Reputation Management in hotel work. Reputation Management is typically an executive-level function often under the purview of the hotel's General Manager, but the actual management of online reviews tend to fall under the Marketing Department of a large hotel. Within said Marketing Department, there is often only a small team (often just one person) involved in the processing of review data for the purpose of producing valuable insights for the executive and feedback for different branches of a hotel in-charge of different functions. This involved lengthy communication with each different stakeholder to complete.

Such work was highly tedious due to the subjective and multi-faceted (one review talked about many different things) nature of hotel reviews and required personnel skilled in understanding nuances of the English Language to be accurately produced. That said, online reviews tend to be repetitive in their use of words to describe different parts of a hotel -- making them good candidates to be processed by data analysis techniques. The reduction of said labour and time required to derive insights from online reviews is the motivation of this project.

## Data Science Problem

1. Create a model which will correctly identify aspects of a hotel being reviewed from sections of online review data with highest possible accuracy.
2. Model will subsequently identify the general sentiment (positive, neutral, negative) of target aspect section.

It is the hope that such automatic processing of online review data will enable all stakeholders to receive only information which is relevant to them, and to reduce labour of hotels' Marketing Departments.

## Results

Our model predicted Aspects and Sentiment respectively with Micro F1 Scores respectively of 0.80 and 0.75. While the model fulfils its purpose, it is nevertheless in need of much greater sophistication to be of use in a production enviroment.
