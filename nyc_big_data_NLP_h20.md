NYC Big Data Science
[Natural Language Processing with H2O](https://www.meetup.com/NYC-Big-Data-Science/events/238249001/)
Michal and Megan Kurka H20.ai


R is just wrapper for h20
All computations done optimized

NLP
Word2vec
Embeddings capture meaning of words
Single hidden layer
Uses trick to formulate problem as supervised problem
Similar to auto encoders
Embeddings are weight matrix from input layer to hidden layer

Optimization
Hierarchical softmax - binary tree
Negative sampling
Hog Wild! - Lock free parallelization

Skipgram works better with larger training data.  Represents even rare words and phrases.


Word2vec usage - typically as preprocessing
Need to aggregate embeddings
Pooling
Averaging
TD-IDF (Not as good for sentiment analysis)
PCA and Fisher vectors
(Recommends paragraph vectors and convnets for NLP)

sent_sample_rate down samples frequent words
Cannot do lemmatization in H2O well.

H2O does anomaly detection using autoencoder