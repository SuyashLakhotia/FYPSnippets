---
layout: post
title: "#18: Week of 25 December"
---

- Started work on implementing models for text categorization that are dataset-independent ([GitHub](https://github.com/SuyashLakhotia/TextCategorization)).
  - Ported over the useful models from the ones implemented for the Rotten Tomatoes dataset (i.e. Baseline Models, Yoon Kim's CNN & Michael Defferrard's Graph CNN).
  - Implemented a generic MLP model (fully-connected hidden layers followed by a softmax layer) to provide a point of comparison.
  - Abstracted away the preprocessing & training code to make it consistent across all models.
  - Started experiments with the 20 Newsgroups dataset ([scikit-learn documentation](http://scikit-learn.org/stable/datasets/twenty_newsgroups.html)). The test accuracies of the different models can be found [here](https://github.com/SuyashLakhotia/TextCategorization/blob/master/results.csv).
- Cleaned up the [codebase & documentation](https://github.com/SuyashLakhotia/RottenTomatoesCNN) for the Rotten Tomatoes models, which will no longer be worked on.
