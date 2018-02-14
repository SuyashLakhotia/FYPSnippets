---
layout: post
title: "#16: Week of 11 December"
---

- Read "Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering" by M. Defferrard, X. Bresson & P. Vandergheynst ([arXiv](https://arxiv.org/abs/1606.09375)) and studied the accompanying code [on GitHub](https://github.com/mdeff/cnn_graph) and in the .zip file provided by Prof. Bresson.
- Continued working on the Rotten Tomatoes model ([GitHub](github.com/SuyashLakhotia/RottenTomatoesCNN)).
  - Studied my previously written code to re-familiarize myself with TensorFlow and the operations (and corresponding tensor shapes) involved.
  - `Model v3`: Created an experimental model that represents every word with a large vector that contains the cosine similarity to every other word in the vocabulary to experiment with a crude form of training CNNs on graphs (represented by a similarity matrix, in this case). However, the model had a large number of trainable parameters (took > 33 hours to train) and resulted in a lower accuracy than `Model v2`.
  - `Model v4`: Implemented a graph convolutional neural network for the problem based on the paper by M. Defferrard et al. The accuracy of the model was slightly lower than `Model v2` but comparable to `Model v1` when implemented with a single graph convolutional layer (as opposed to previous architectures that used three convolutional + pooling layers in parallel) followed by a softmax layer.
- Set up the server provided for CPU operations (installed pyenv, Python 3, TensorFlow etc.).
