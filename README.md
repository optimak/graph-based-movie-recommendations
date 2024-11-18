# Recommendation System Using Multiple Graph-Theory Techniques
- Originally on Colab - [here](https://colab.research.google.com/drive/16GxzzoeQWLcARZhYjCsaHILyKYbij1mA?usp=sharing)

This Python code demonstrates a recommendation system using three different techniques for movie recommendations: **Closeness Centrality**, **Jaccard Similarity**, and **PageRank**.

## Key Steps:
1. **Data Loading**: Loads user-movie rating data from a CSV file.
2. **Train-Test Split**: The dataset is split into training and testing sets for model evaluation.
3. **Closeness Centrality**:
   - A graph is created where users and movies are nodes, and ratings are weighted edges.
   - Closeness centrality for users is calculated to determine how central each user is in the graph, based on their rating patterns.
   - Recommendations are generated by scoring movies based on user centrality and the ratings they have given to other movies.
4. **Jaccard Similarity**:
   - A similarity matrix is created for movies based on the overlap in users who have rated them.
   - Jaccard similarity scores are applied to adjust recommendation scores.
5. **PageRank**:
   - A bipartite graph is created between movies and users, with ratings as edges.
   - PageRank scores are computed for movies, ranking them by influence.
   - Recommendations are made based on these scores.

## Evaluation:
- The **Mean Average Precision (MAP)** is computed to evaluate how well the recommendations match the test data, based on the relevance of recommended movies to the user's actual preferences.

## Why It Stands Out:
- **Closeness Centrality** helps to identify influential users, which can be used to predict what movies other similar users may like.
- **Jaccard Similarity** adds an extra layer by quantifying movie similarities based on shared viewers, improving the precision of recommendations.
- **PageRank** provides a novel way to rank movies based on their influence, treating the recommendation problem as a graph centrality issue, offering an alternative to traditional methods.
- Combining these techniques offers a robust recommendation engine that uses both user behavior and item similarity for personalized recommendations.

## Results
| Model                                    | MAP (%) |
|------------------------------------------|---------|
| Closeness Centrality with Jaccard similarity | 68.50   |
| Closeness Centrality Alone               | 69.05   |
| PageRank                                 | 81.24   |

