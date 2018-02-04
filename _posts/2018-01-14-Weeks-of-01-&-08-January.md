---
layout: post
title: "#19 & #20: Weeks of 1 & 8 January 2018"
---

- Worked on the text categorization models ([GitHub](https://github.com/SuyashLakhotia/TextCategorization)).
  - Investigated an issue where adding fully-connected layers to the graph CNN prevented the network from converging. Changing the weight initialization (for the fully-connected layers & output layer) to `tf.truncated_normal(0, 0.1)` from Xavier initialization and reducing the vocabulary size from 10,000 to 1,000 seemed to solve the problem, however, multiple runs of training revealed that the model did not *always* converge. Additionally, reducing the vocabulary size dramatically reduces the accuracy of the model so this is not a feasible solution.
  - Implemented the other graph convolutional networks (i.e. Non-Param & Spline) mentioned in M. Defferrard's paper by adapting the code from [GitHub](https://github.com/mdeff/cnn_graph/) and ran them with the same hyperparameters as the model introduced in the paper (i.e. Chebyshev) for the 20 Newsgroups dataset. The resulting accuracies can be found [here](github.com/SuyashLakhotia/TextCategorization/blob/master/results.csv).
  - Cleaned up the codebase by merging the code for the graph convolutional networks, adding command-line arguments and further abstracting away data-related code to make the models truly dataset-independent.
  - Rewrote the preprocessing code for the Rotten Tomatoes movie review dataset for this repository, added the dataset and ran the different models on it (resulting test accuracies can be found [here](github.com/SuyashLakhotia/TextCategorization/blob/master/results.csv)).
  - Started work on incorporating the RCV1 dataset by studying the dataset (as provided by [sklearn](http://scikit-learn.org/stable/datasets/rcv1.html)) and writing parts of the preprocessing code.
- Revisited the paper by M. Defferrard et al. ([arXiv](https://arxiv.org/abs/1606.09375)) and the papers referenced by the authors (specifically [J. Bruna, 2014](https://arxiv.org/abs/1312.6203) & [M. Henaff, 2015](https://arxiv.org/abs/1506.05163)) to further understand the details behind graph convolutional neural networks.
