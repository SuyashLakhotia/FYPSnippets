---
layout: post
title: "#25: Week of 12 February"
---

- Finished writing the code needed to extract and preprocess the RCV1 dataset.
- Started running experiments on the RCV1 dataset using a similar train/test split as the one described in M. Henaff, 2015 (or [N. Srivastava, 2014](http://jmlr.org/papers/volume15/srivastava14a.old/srivastava14a.pdf)). Comprehensive results can be found [here](https://github.com/SuyashLakhotia/TextCategorization/blob/master/results.csv). A summary is given below (training time & epochs till 85% test accuracy are approximate values):

| Model           | Test Accuracy | Parameters | Training Time <sup>†</sup>  | Epochs till 85% |
|:---------------:|:-------------:|:----------:|:---------------------------:|:---------------:|
| Linear SVC      | 0.882898531   | N/A        | 51.48s *                    | N/A             |
| Softmax         | 0.898617073   | 104,052    | 29.22s                      | 7.61            |
| FC2000-FC1000   | 0.902019664   | 6,055,052  | 655.46s                     | 0.30            |
| GC5_32 [Cheby]  | 0.896903872   | 3,328,244  | 547.44s                     | 0.46            |
| GC5_32 [Spline] | 0.898712250   | 3,328,244  | 615.08s                     | 0.67            |

<!--
| 1518605241 |
| 1518542234 |
| 1518842040 |
| 1518603526 |
| 1518708077 |
-->

<small><sup>†</sup> Time taken per training epoch.</small>
<small>\* Total time taken for complete training of model.</small>

- Ran experiments with count vectors on 20 Newsgroups. Since count vectors were originally used in the M. Defferrard et al. paper, it is important to identify whether the increase in performance of my models is solely because of the use of tf-idf vectors (or changes to the model architecture also contribute to the same).
- Improved the data preprocessing pipeline such that it pickles the preprocessed train/test datasets for particular vocabulary sizes and sequence lengths (i.e. the default options) for accelerated loading in future experiments. This is especially important for the large RCV1 dataset.
- Skimmed through a couple blog posts ([Huszar, 2016](http://www.inference.vc/how-powerful-are-graph-convolutions-review-of-kipf-welling-2016-2/) and [Kipf, 2016](https://tkipf.github.io/graph-convolutional-networks/)) on graph convolutional neural networks (primarily about [T. Kipf et al., 2016](https://arxiv.org/abs/1609.02907))
