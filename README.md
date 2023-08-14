# Movie-Reccomendation-System
This project implements a simple movie recommender system using cosine similarity between movie vectors.

## Contents
The project contains the following files:
* `Main.ipynb`: Jupyter notebook containing the code to load data, vectorize movie tags, generate similarity matrix, and make recommendations
* `movies_list.pkl`: Pickle file containing the filtered movie dataframe
* `similarity.pkl`: Pickle file containing the pre-computed similarity matrix
* `dataset.csv`: Movie dataset used for training

## Usage
The key steps are:

1. Import libraries and load data
2. Select features and create a tags column
3. Vectorize tags using CountVectorizer
4. Compute cosine similarity matrix
5. Define a recommendation function
6. Save data and model pickles

To get recommendations for a movie, pass the title to the `recommend()` function. This will return the 5 most similar movies based on the pre-computed similarity matrix.

The benefit of pickling the data and model is that recommendations can be made quickly without having to re-compute the similarity matrix each time.

## Next Steps
Some ways this recommender could be improved:

* Incorporate additional data like genres, keywords, etc to make more robust movie vectors
* Apply dimensionality reduction techniques like LSA to reduce noise before computing similarity
* Use matrix factorization methods to predict ratings and recommend based on predicted preferences
* Evaluate performance quantitatively by splitting data into train and test sets
* Deploy model and serve recommendations via a web application
