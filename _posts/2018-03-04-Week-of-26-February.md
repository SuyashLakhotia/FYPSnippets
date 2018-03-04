---
layout: post
title: "#27: Week of 26 February"
---

- Ran further experiments on `gcnn_chebyshev` with the RCV1 dataset (`|V| = 10,000`) to study the effect of the number of edges in the feature graph & filter size. Results can be found in this [gist](https://gist.github.com/SuyashLakhotia/b224c8d0d1197073f1b97b2b1312823b) (also embedded below).
- Ran experiments on Linear SVC with the RCV1 dataset (`|V| = 10,000`) to optimize the penalty hyperparameter `C` and establish an unbiased baseline for the more complex models. The results of the experiments can be found in this [gist](https://gist.github.com/SuyashLakhotia/2b114c56c0b131643ea74e91c2461814) (also embedded below).
- In order to improve generalization, re-ran the experiments on Linear SVC's penalty hyperparameter using a separate validation set (10% of training set, ~20,000 documents) instead of the test set (as was done previously). This script is currently still running.
- Currently also running a grid search to optimize the number of edges in the feature graph (`[4, 8, 16]`), filter size (`[2, 4, 5]`) and number of features (`[8, 16, 32]`) for `gcnn_chebyshev` on the RCV1 dataset (`|V| = 10,000`). The hyperparameter values are tuned using a validation set and the final model will be benchmarked using an independent test set.

---

<details>
  <summary>Experiments on No. of Edges & Filter Size</summary>
  <script src="https://gist.github.com/SuyashLakhotia/b224c8d0d1197073f1b97b2b1312823b.js"></script>
</details>

<details>
  <summary>Experiments on Linear SVC Penalty Parameter</summary>
  <script src="https://gist.github.com/SuyashLakhotia/2b114c56c0b131643ea74e91c2461814.js"></script>
</details>
