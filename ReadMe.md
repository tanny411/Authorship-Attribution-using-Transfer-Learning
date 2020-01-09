# Authorship Attribution using Transfer Learning

## Table of contents
- [Overview](#Overview)
- [Paper Abstract](#Paper-Abstract)
- [Datasets](#Datasets)
- [Trained Models](#Trained-Models)
- [Future Work](#Future-Work)
## Overview 

## Paper Abstract
Authorship Attribution deals with the task of creating an appropriate characterization of texts that captures the writing style of authors for accurate classification. With increased anonymity on the internet, this task has become increasingly crucial in various fields of security and plagiarism detection. Despite a few strands of work recently, Bangla lacks comprehensive research in this field mainly due to the scarcity of resources. In this paper, we propose an approach for authorship attribution in Bangla based on AWD-LSTM architecture and transfer learning from language models in three steps. Comparison of three variations of the proposed models are shown, with the major difference being in tokenization - word, sub-word and character level tokenization. We also compare some previous state-of-the-art models and show that the transfer learning approach using sub-word tokenization pre-trained on News dataset performs better than other approaches. Specifically an increase of 18\% and 6\% on accuracy for the final target datasets is observed.
## Datasets
#### Pre-training datasets:
- [News dataset](https://data.mendeley.com/datasets/xp92jxr8wn/1?fbclid=IwAR09nbvU3G4tNoI6zuLoL3FMhvggdE6RuLFOyKMHubrHd7PivLGJeCTch9k): A corpus on Bangla newspaper articles created using a custom web crawler containing 12 different topics. [Paper reference](https://arxiv.org/abs/1911.07613)
- [Wikipedia corpus](https://data.mendeley.com/datasets/3ph3n78fp7/1?fbclid=IwAR2qOFI27mVQoEMdJBUinL0k_zCjzEMpnFk74cKANhil7oKGSgbT_6E8keI): The Bangla Wikipedia dump collected on 10th June, 2019. Cleaned and arranged into samples in csv.

#### Authorship Attribution datasets:
- [Dataset1](https://data.mendeley.com/datasets/6d9jrkgtvv/1?fbclid=IwAR09nbvU3G4tNoI6zuLoL3FMhvggdE6RuLFOyKMHubrHd7PivLGJeCTch9k): A dataset with sample Bangla texts from 16 authors. Equally partitioned with each document having 750 words. [Paper reference]
- [Dataset2](https://data.mendeley.com/datasets/w9wkd7g43f/2?fbclid=IwAR1dHxYWLGGkSTLMncPMXxzkNSTKpOJrtJJTGlufeYeTnLTfevo3RzM-uG4): A dataset consisting of text samples from 6 authors with 350 samples per author. [Paper reference](https://ieeexplore.ieee.org/document/8631977).

## Trained Models
Links to all the pre-trained models are provided in the [doc file](https://docs.google.com/document/d/1S3pVPXNVy_F5wP_TLKSQuideKx8EesjbBT5XHlItJM0/edit?usp=sharing). The language models have been trained on Bangla news and Wikipedia corpus. Further, there are 3 variations to each. Word, Subword and Character level tokenized, making a total of 6 pre-trained language models.
*All access requests will be granted within 24-hours.*

## Future Work:
- CNN architecture based transfer learning for authorship attribution
- Comparsion with Transformer based architectures such as BERT, XLNet etc
- Cross-lingual authorship attribution
