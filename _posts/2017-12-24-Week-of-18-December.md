---
layout: post
title: "#17: Week of 18 December"
---

- Studied the theory and mathematics behind graph convolutional networks as described in the paper by M. Defferrard et al.
- Worked on the Rotten Tomatoes model ([GitHub](github.com/SuyashLakhotia/RottenTomatoesCNN)).
  - Cleaned up and restructured the codebase to make it easier to maintain and extend for other datasets.
  - Implemented a version of the graph CNN model with an architecture similar to previous models i.e. parallel convolutional + pooling layers whose outputs are concatenated before being fed to the softmax layer. The resulting model had a similar accuracy as the model with the single graph convolutional layer.
  - Trained another version of the single graph convolutional layer model with different hyperparameters (matching those from Michael Defferrard's [implementation](https://github.com/mdeff/cnn_graph/blob/master/nips2016/20news.ipynb) on the 20 Newsgroups dataset).
  - Implemented a couple baseline models (Multinomial Naive Bayes & Linear Support Vector Classifier) to better gauge the performance of the more complex models.
- Set up the server for GPU computations (installed CUDA, cuDNN, TensorFlow GPU etc.).
