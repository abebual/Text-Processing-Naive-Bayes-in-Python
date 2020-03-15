# Text-Processing-Naive-Bayes-in-Python
In the mini-project, you'll learn the basics of text analysis using a subset of movie reviews from the rotten tomatoes database. You'll also use a fundamental technique in Bayesian inference, called Naive Bayes. This mini-project is based on Lab 10 of Harvard's CS109 class. Please free to go to the original lab for additional exercises and solutions.

Picking Hyperparameters for Naive Bayes and Text Maintenance

We need to know what value to use for 𝛼, and we also need to know which words to include in the vocabulary. As mentioned earlier, some words are obvious stopwords. Other words appear so infrequently that they serve as noise, and other words in addition to stopwords appear so frequently that they may also serve as noise.

First, let's find an appropriate value for min_df for the CountVectorizer. min_df can be either an integer or a float/decimal. If it is an integer, min_df represents the minimum number of documents a word must appear in for it to be included in the vocabulary. If it is a float, it represents the minimum percentage of documents a word must appear in to be included in the vocabulary. 
Aside: TF-IDF Weighting for Term Importance
TF-IDF stands for 
Term-Frequency X Inverse Document Frequency.
In the standard CountVectorizer model above, we used just the term frequency in a document of words in our vocabulary. In TF-IDF, we weight this term frequency by the inverse of its popularity in all documents. For example, if the word "movie" showed up in all the documents, it would not have much predictive value. It could actually be considered a stopword. By weighing its counts by 1 divided by its overall frequency, we downweight it. We can then use this TF-IDF weighted features as inputs to any classifier. TF-IDF is essentially a measure of term importance, and of how discriminative a word is in a corpus.
