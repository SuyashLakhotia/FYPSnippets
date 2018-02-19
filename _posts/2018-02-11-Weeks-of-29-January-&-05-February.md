---
layout: post
title: "#23 & #24: Weeks of 29 Jan & 5 Feb 2018"
---

- Started work on a REST API and client-side web application for models trained on the RT Polarity dataset.
- Worked on preparing the RCV1 dataset from the raw data dump since the document vectors provided by scikit-learn don't provide enough information for experiments with the different models.
  - Read the [RCV1 paper](http://www.jmlr.org/papers/volume5/lewis04a/lewis04a.pdf) and accompanying [online appendices](http://www.ai.mit.edu/projects/jmlr/papers/volume5/lewis04a/lyrl2004_rcv1v2_README.htm) to understand the raw files provided and other necessary details of the dataset.
  - Wrote a Python [script](https://github.com/SuyashLakhotia/TextCategorization/blob/master/process_rcv1.py) to extract relevant information from the RCV1 data dump (large collection of XML files) into Python pickles.
  - Each RCV1 document is a concatenation of its `<headline>` and `<text>` elements (as in the original paper) and the classes are assigned according to the file described in Online Appendix 8.
- Added an option to run the models on count vectors in addition to tf-idf vectors in order to compare their relative performance.
