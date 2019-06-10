## Overview
This project was created to build a recommendation engine to provide, existing and new users, with new articles to read from the IBM Watson studio platform.

## Description
This recommendation engine project was build by four different types of recommendations:

  **Rank Based**

  This type of recommendation strategy works by  finding the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, it is easy to assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users (or anyone depending on what we know about them).

  **User-User Based Collaborative Filtering**

  This type of recommendation works by looking at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users.

  **Content Based**
  
  This type of recommendation works by looking at articles that share similar characteristics based on the content of each. In this specific task, i used  NLP to recommend articles by first, getting the top 5 most used words in the title of interest, then i match this result to the titles that share the same words in their names, to finally give the user this new list of articles to read sorted by how many times this top 5 words appeared each title name.

  **SVD (Singular Value Decomposition)**

 This is a machine learning approach to building recommendations. Using the user-item interactions, a matrix decomposition is build. Using this decomposition, one can get an idea of how well one can predict new articles an individual might interact with (in this task it isn't great).

> My suggestion for a recommendation system for this dataset is that SVD would not be an ideal choice, instead, the system would be a combination of different models: rank based, content based and maybe SVD, it will depend on the results it may show from an experiment design application, this can be an A/B test for example to check how well the engine is doing to then, choose the best strategy.

## Files
- recommendations_with_IBM.ipynb : Jupyter Notebook containing the code for the recommendation engine

- user-item-interactions.csv: Database containing the information about the interactions between users and articles in the form of `article_id`, `title`, and `email`.

- articles_community.csv: Database containing information about articles in the form of: `doc_body`, `doc_description`, `doc_full_name`, `doc_satatus`, `article_id`.


# Libraries
- pandas
- numpy
- matplotlib
- seaborn
- nltk
- collections
