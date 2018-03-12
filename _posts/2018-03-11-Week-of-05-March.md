---
layout: post
title: "#28: Week of 05 March"
---

- Completed the hyperparameter optimization for Linear SVC on the 10,000-word RCV1 dataset using a validation set. Comprehensive results can be found in this [gist](https://gist.github.com/SuyashLakhotia/48235748948bdaa986172b4976d466ba) (also embedded below). The optimal value for `C` was found to be 14.3, which had a validation accuracy of 90.79% and test accuracy of 91.19%.
- Completed the grid search for Graph CNN [Chebyshev] on the 10,000-word RCV1 dataset using a validation set. Comprehensive results can be found in this [gist](https://gist.github.com/SuyashLakhotia/145e3d1709dcee455b30dfc72d951a10) (also embedded below). The optimal values for the number of edges, filter size and number of features were found to be 16, 4 & 8 respectively. The resulting model had a validation accuracy of 91.04% and test accuracy of 91.27%.

---

<details>
  <summary>Linear SVC Hyperparameter Optimization</summary>
  <script src="https://gist.github.com/SuyashLakhotia/48235748948bdaa986172b4976d466ba.js"></script>
</details>

<details>
  <summary>Graph CNN Hyperparameter Grid Search</summary>
  <script src="https://gist.github.com/SuyashLakhotia/145e3d1709dcee455b30dfc72d951a10.js"></script>
</details>
