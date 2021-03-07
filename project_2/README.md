# Project 2: Predicting Ames, Iowa Housing Information to Determine Sale Price

In this project, our objective is to is to develop a model to predict the selling price of a given home in Ames, Iowa from the given datasets. This information can then be used for real estate and relevant industry to make predictions on the value of a home within Ames.  

Our selected model performs well with with a root mean squared error (RMSE) of $30,000 on a dataset with a mean of $181,000.

## 1.1  Executive Summary
Our process is summarized as such:

1. Train and test set data is cleaned with rows of missing data either removed or imputed.
2. Ordinal categorical data is put into a scalar numeric form in-line with its impact.
3. Nominal categorical data is dummified with cardinalities with low representation merged (10% of all data have their cardinalities merged into an 'others' category where appropriate)
4. Linear, Ridge and Lasso regression models are produced and compared to decide on which has the best results.  

We have found that house prices are best prediced by its indoor area and features (number of rooms, fireplaces, etc.), age of the property, and quality metrics available in the dataset. These are all expected.

Surprisingly, adjacent features (its surrounding area and amenities) and open areas (porches) do not and overall lot area do not correlate to the sale price as much. Further, very large houses tend to be predicted by another pricing algorithm.

Our report could have been improved with better information on each home's location (their address) and information on when these sales prices were published. Time of sale affects the variability of the results significantly. For example, if these sales were made in an economic boom, sale price would be largely inflated. Conversely, in a recession, they would be deflated.