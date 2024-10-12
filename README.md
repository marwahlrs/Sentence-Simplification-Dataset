This repository contains a sentence simplification dataset that adopts methods from the paper [An Unsupervised Method for Building Sentence Simplification Corpora in Multiple Languages](https://aclanthology.org/2021.findings-emnlp.22)
, with adaptations for the Indonesian language. 

We use the News En-Id parallel corpus from the paper [Benchmarking Multidomain English-Indonesian Machine Translation](https://aclanthology.org/2020.bucc-1.6). In this setup, the Indonesian sentence represents  the complex sentence, while the English sentence is used as a bridge language. The English sentence is then translated back into Indonesian to generate a simplified version.

To filter and select sentence pairs for the simplification process, we apply two key metrics:
- BLEU: This metric assesses the quality of paraphrasing by comparing the similarity between the original (complex) and simplified sentences.
- Flesch Reading Ease Score (FRES): This metric measures readability, with higher scores indicating easier-to-read sentences. A FRES score difference threshold of 10 is used, which corresponds to approximately one grade level of simplification between the original and simplified sentences.

The dataset contains two columns Id_Complex and Id_Simple with 1,306 sentence pairs in the training set, 199 in the validation set, and 194 in the test set.
