# Authorship Attribution using Transfer Learning

## Table of contents
- [Introduction](#Introduction)
- [Contributions](#Contributions)
- [Paper Abstract](#Paper-Abstract)
- [Code](#code)
- [Datasets](#Datasets)
- [Trained Models](#Trained-Models)
- [Future Work](#Future-Work)

## Introduction

Authorship attribution is a type of classification task concerned with detecting the author of a piece of writing by analyzing its stylometric and linguistic features within a set of probable authors. Anonymity is very common in recent times, especially due to widespread use of internet the use and misuse of anonymity has become an important factor to consider. The plethora of anonymous digital footprints makes authorship attribution indispensable in various fields.
In this work we perform transfer learning for authorship attribution based on a language modeling objective. Unsupervised training of a language model teaches a model the working and structure of Bangla language, followed by authorship attribution specific fine-tuning and classification. Effects of various tokenization on this model are analyzed in terms of performance. The results demonstrate a clear superiority of the transfer learning based approach against the other traditional models.

## Contributions
- Release of a large long-text 16 author dataset for authorship attribution in Bangla literature which closely mimics real world scenarios.
- Achieving state-of-the art performance on authorship attribution with a robust transfer learning approach using AWD-LSTM architecture. The proposed system scales much better with an increasing number of authors, and the performance remains steady even with a small number of samples
- Release of pre-trained language models for use in any Bangla NLP downstream tasks. We release 6 variations, in terms of tokenizations and pre-training dataset.

**All models, along with the datasets have been released in this repository.**

Our academic paper on Authorship Attribution in Bangla language can be found [here](to be updated).

## Paper Abstract
Authorship Attribution deals with the task of creating an appropriate characterization of texts that captures the writing style of authors for accurate classification. With increased anonymity on the internet, this task has become increasingly crucial in various fields of security and plagiarism detection. Despite significant advancements in English, Bangla lacks comprehensive research in this field mainly due to the scarcity of resources. Moreover, existing systems are not scalable with an increasing number of authors and do not perform well with a small number of samples per author. In this paper, we propose an approach for authorship attribution in Bangla based on AWD-LSTM architecture and transfer learning from language models. Comparison among three variations of the proposed models are shown, with the major difference being in tokenization - word, sub-word, and character level tokenization. For this purpose, a large dataset of 16 authors is built containing 17,966 sample texts and 13.4+ million words in total. We compare some previous state-of-the-art models and show that (i) our best model performs better than other approaches reaching an accuracy of 95.3\% ad 99.8\% on two target datasets respectively, (ii) the proposed system scales much better with an increasing number of authors, (iii) performance remains steady even with a small number of samples.

## Code
This repository is structured in the following way:
- **Model**: Contains all the model training and testing code for the proposed method of the paper. Further subdivided into folders containing 3 types of tokeization.
    - Character-level starter code: [character news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Character-level/character%20news.ipynb), [character news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Character-level/character%20wiki.ipynb) 
    - Subword-level starter code: [subword news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Subword-level/subword%20news.ipynb), [subword wiki](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Subword-level/subword%20wiki.ipynb)
    - Word-level starter code: [word_news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Word-level/word_news.ipynb), [word_wiki](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Word-level/word_wiki.ipynb)
- **Others Models**: Contains tests on previously published models for comparison.

## Datasets
#### Pre-training datasets:
- [News dataset](https://data.mendeley.com/datasets/xp92jxr8wn/1?fbclid=IwAR09nbvU3G4tNoI6zuLoL3FMhvggdE6RuLFOyKMHubrHd7PivLGJeCTch9k): A corpus on Bangla newspaper articles created using a custom web crawler containing 12 different topics. [Paper reference](https://link.springer.com/chapter/10.1007/978-981-15-3607-6_31)
- [Wikipedia corpus](https://data.mendeley.com/datasets/3ph3n78fp7/1?fbclid=IwAR2qOFI27mVQoEMdJBUinL0k_zCjzEMpnFk74cKANhil7oKGSgbT_6E8keI): The Bangla Wikipedia dump collected on 10th June, 2019. Cleaned and arranged into samples in csv.

#### Authorship Attribution datasets:
- [BAAD16](https://data.mendeley.com/datasets/6d9jrkgtvv/4): The published dataset with sample Bangla texts from 16 authors in an unbalanced manner to mimic real world scenarios closely and test model robustness. Equally partitioned with each document having 750 words.
- [BAAD6](https://data.mendeley.com/datasets/w9wkd7g43f/5): A dataset consisting of text samples from 6 authors with 350 samples per author. [Paper reference](https://ieeexplore.ieee.org/document/8631977).

## Trained Models
Links to all the pre-trained models are provided in the [doc file](https://docs.google.com/document/d/1S3pVPXNVy_F5wP_TLKSQuideKx8EesjbBT5XHlItJM0/edit?usp=sharing). The language models have been trained on Bangla news and Wikipedia corpus. Further, there are 3 variations to each. Word, Subword and Character level tokenized, making a total of 6 pre-trained language models.
*All access requests will be granted within 24-hours.*

## Future Work:
- Assessing application of pure-Bangla tansformer based pre-trained models.
- CNN architecture based transfer learning for authorship attribution.
- Cross-lingual authorship attribution.
