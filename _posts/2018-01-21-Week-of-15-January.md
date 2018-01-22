---
layout: post
title: "#21: Week of 15 January 2018"
---

- After a discussion with Prof. Bresson about the convergence issue with the fully-connected layers, I experimented with his suggestions to 1) change the weight initialization and 2) add batch normalization.
  - Read up on the effect of weight initialization ([Stanford CS231n](http://cs231n.github.io/neural-networks-2/#init), [Blog Post](https://intoli.com/blog/neural-network-initialization/)).
  - Read up on Xavier initialization, in particular ([Blog Post 1](http://andyljones.tumblr.com/post/110998971763/an-explanation-of-xavier-initialization), [Blog Post 2](https://prateekvjoshi.com/2016/03/29/understanding-xavier-initialization-in-deep-neural-networks/)).
  - Read up on batch normalization ([S. Ioffe & C. Szegedy, 2015](https://arxiv.org/abs/1502.03167), [Blog Post 1](https://medium.com/deeper-learning/glossary-of-deep-learning-batch-normalisation-8266dcd2fa82), [Blog Post 2](https://gab41.lab41.org/batch-normalization-what-the-hey-d480039a9e3b), [Blog Post 3](http://ruishu.io/2016/12/27/batchnorm/)).
  - Experimented with different weight initializations, dropout rates and batch normalization. My notes and detailed results can be found [here](https://gist.github.com/SuyashLakhotia/a354c37842aef758bc57673d14a4ff6f) (also embedded below). The results of the experiments support adding batch normalization and keeping weight initialization & dropout as before (i.e. Xavier & 0.5 respectively).
  - Added batch normalization to the fully-connected layers of the network using [TensorFlow's implementation](https://www.tensorflow.org/api_docs/python/tf/layers/batch_normalization).
- Looked into incorporating a decay rate (for a dynamic learning rate) in order to bump the performance of the models. However, since I'm currently using the Adam optimizer ([TF Docs](https://www.tensorflow.org/api_docs/python/tf/train/AdamOptimizer), [Blog Post](https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/)), which already incorporates momentum for per-parameter learning rates, incorporating a decay rate will not cause a significant increase in performance. Nonetheless, I will revisit this at a later time for empirical results.

---

<details>
  <summary>Experiments on Weight Initialization, Dropout & Batch Normalization</summary>
  <script src="https://gist.github.com/SuyashLakhotia/a354c37842aef758bc57673d14a4ff6f.js"></script>
</details>
