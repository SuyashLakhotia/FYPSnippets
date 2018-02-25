---
layout: post
title: "#26: Week of 19 February"
---

- Ran experiments on `gcnn_chebyshev` with the RCV1 dataset to study the effect of vocabulary size, filter size & number of features on the performance of the model. Increasing the vocabulary size allowed for 1 - 2% increase in performance, however, the other two hyperparameters had little effect. Results from the experiments can be found in this [gist](https://gist.github.com/SuyashLakhotia/4e6416b03fe571d34274fdd8fd66641b) (also embedded below).
- Worked on the demo web application for the models trained on the Rotten Tomatoes dataset (for now).
  - Finished writing the front-end code for the application.
  - Currently still building the pipeline on the back-end to take a piece of text and convert it into the necessary representation(s) to pass to the model(s) for inference.
  - The codebase can be found on [GitHub](https://github.com/SuyashLakhotia/TextCategorization-Demo).

---

<details>
  <summary>Experiments on Vocabulary Size, Filter Size & No. of Features</summary>
  <script src="https://gist.github.com/SuyashLakhotia/4e6416b03fe571d34274fdd8fd66641b.js"></script>
</details>
