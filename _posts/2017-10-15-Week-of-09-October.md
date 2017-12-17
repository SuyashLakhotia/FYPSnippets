---
layout: post
title: "#7: Week of 09 October 2017"
---

- Finished reading Y. Zhang & B. C. Wallace's paper, which dives deeper into Y. Kim's model and explores the effect of the hyperparameters involved. Wrote some notes [here](https://gist.github.com/SuyashLakhotia/d6fb338cd529af0181d78b00a3436e29) (also embedded below).
- Worked on improving the Rotten Tomatoes model based on results from Y. Kim's original paper.
  - `Model v2`: Implemented a version of the model that uses pre-trained word2vec vectors trained on a corpus of ~100 billion words from Google News ([Link](https://code.google.com/archive/p/word2vec/)). This increased model performance by ~5%.
  - `Model v2.1`: Implemented a slightly different version that uses the same pre-trained word2vec vectors but also fine-tunes them for the task at hand.
  - Documented all results and uploaded the code to the [GitHub repo](https://github.com/SuyashLakhotia/RottenTomatoesCNN).

---

<details>
  <summary>Notes on Y. Zhang's Paper</summary>
  <script src="https://gist.github.com/SuyashLakhotia/d6fb338cd529af0181d78b00a3436e29.js"></script>
</details>
