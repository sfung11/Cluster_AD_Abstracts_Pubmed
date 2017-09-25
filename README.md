# Clustering Pubmed abstracts about Alzheimer's Disease (AD)

Objective: Cluster Pubmed abstracts about AD.

Data: Journal articles, including reviews, were accessed using [Biopython](http://biopython.org) query tools. Retrieved information from 130,672 results was stored in mongoDB on AWS. Note there is a bug in the example code in the docs if using NCBI's history support. This is found in "9.15.2  Searching for and downloading abstracts using the history". The while loop will go into an infinite loop; my code in data_collection.ipynb fixes this (in a hacky way).

Algorithm: Clustering (unsupervised learning) using KMeans. 

Evaluation: After clustering, topic modeling was done for abstracts as well as titles and a subset was visualized by using t-distributed stochastic neighbor embedding (t-SNE).

Further Improvement: Improve topic modeling by working on text preprocessing. Topic words, like "alzheimers", "neurodegenerative", "diseases" may benefit from being removed. Expanding this project to include additional neurodenerative diseases is possible and start a focused recommender system is possible.
