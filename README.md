# TasteMovie

DataSet & TasteMovie Recommendation Algorithm
DataSet Link:
For details of the dataset, visit (https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata/data).

Algorithm:
TasteMovie Recommendation Algorithm

TasteMovie uses an advanced recommendation algorithm to provide users with the most suitable movie suggestions. This algorithm measures the similarities between movies to identify content that may interest the user.

Here's how the process works below:

1. TF-IDF (Term Frequency-Inverse Document Frequency) Approach:

To gather information about movies, we combine their summaries, genres, cast, and other keywords to create unique "tags" for each film. However, some words are more frequently used and less distinctive. TF-IDF is used to make these tags more meaningful and distinctive:

-TF (Term Frequency): Measures how often a specific word appears in a movie's tag.

-IDF (Inverse Document Frequency): Evaluates how common or rare this word is across all movies. As a result, common but less informative words have less impact, while rarer and more significant words have a higher weight.

2.Cosine Similarity:

Once the TF-IDF vectors are created, Cosine Similarity is applied to measure the similarity between movies. This method calculates the angle between two movie vectors. A smaller angle indicates higher similarity:

Value Close to 1: The movies are very similar.

Value Close to 0: The movies are very different.

For instance, if you select an action-sci-fi movie, the algorithm will recommend other movies with similar action and sci-fi elements.

3. User-Focused Recommendation Mechanism When a user selects a movie, the algorithm retrieves the TF-IDF vector for that movie and compares it with all other movies. The movies with the highest similarity scores are then ranked and recommended to the user.

4. Dynamic and Personalized Recommendations The algorithm can continuously update to find movies that match users' tastes. For example, as more movies with different genres or themes are tagged, the system can offer a broader range of recommendations.
