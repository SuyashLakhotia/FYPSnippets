---
layout: post
title: "#22: Week of 22 January 2018"
---

- Investigated the effect of different weight initializations with differing vocabulary sizes on `gcnn_chebyshev` for 20 Newsgroups. From the results below (`[X]` = Xavier Initialization; `[T]` = Truncated Normal Initialization), we see that for a smaller vocabulary size, truncated normal initialization performs significantly better than Xavier initialization for the weights in the fully-connected layer, however, for a large vocabulary, the difference in the resulting test accuracies is negligible.

| Vocabulary Size | Model                | Test Accuracy | Timestamp  |
|:---------------:|:--------------------:|:-------------:|:----------:|
| 1000            | GC15_5               | 0.584843493   | 1516650391 |
|                 | GC15_5-FC100 [X]     | 0.471469223   | 1516652523 |
|                 | GC15_5-FC100 [T]     | 0.531076831   | 1516701282 |
| 10000           | GC15_5               | 0.709111488   | 1516650374 |
|                 | GC15_5-FC100 [X]     | 0.704725523   | 1516654770 |
|                 | GC15_5-FC100 [T]     | 0.703310696   | 1516688197 |

- Experimented with smaller support sizes (i.e. filter sizes) & lesser number of features in the graph convolutional layers of `gcnn_chebyshev` for 20 Newsgroups. As can be seen in the results below (for `|V| = 10000`), reducing the filter size & number of features still results in an accurate model, however, reducing the filter size to `1` prevents the model from learning anything useful.

| Filter Size | Number of Features | Test Accuracy | Timestamp  |
|:-----------:|:------------------:|:-------------:|:----------:|
| 5           | 32                 | 0.716529846   | 1514229132 |
| 5           | 8                  | 0.717600453   | 1516702205 |
| 2           | 4                  | 0.716185625   | 1516654550 |
| 1           | 4                  | 0.054329372   | 1516683318 |

- Ran `gcnn_chebyshev` with one of the architectures listed in [M. Henaff, 2015](https://arxiv.org/abs/1506.05163) (`GC4-P4-FC1000`) which resulted in a model with a maximum test accuracy of 62.99% on 20 Newsgroups.
- Experimented with running `gcnn_chebyshev` on 20 Newsgroups with consecutive graph convolutional layers, however, the network fails to converge when more than two convolutional layers are added (specifically, `GC2_4-GC2_8-GC2_16` doesn't converge while `GC2_4-GC2_8` does). However, even `GC2_4-GC2_8` does not outperform `GC2_4`.
- Implemented `cnn_fchollet`, a CNN architecture for text classification by Francois Chollet, which is blogged about [here](https://blog.keras.io/using-pre-trained-word-embeddings-in-a-keras-model.html) ([Keras Implementation](https://github.com/fchollet/keras/blob/master/examples/pretrained_word_embeddings.py)) and ran it on 20 Newsgroups and RT Polarity. It didn't outperform `cnn_ykim` on both datasets.
- Ran experiments with `cnn_ykim` by tweaking the maximum sequence length and other hyperparameters.
  - Ran the model on 20 Newsgroups with a sequence length of 10,000 and 1,000. Both resulted in very similar test accuracies.
  - Ran the model on RT Polarity with filter sizes `[3, 4, 5]`, `[7, 7, 7]` and `[7]`. All three resulting test accuracies were very similar.
- Wrote the interim report, which serves as a progress update and a preliminary draft of my final report.
