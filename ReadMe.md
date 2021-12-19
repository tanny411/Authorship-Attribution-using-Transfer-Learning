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
- In this paper and repository, we introduce the largest and most varied dataset for AABL with long text samples of 16 authors in an imbalanced manner, imitating real-world scenarios more closely.
- We present an intuitively simple but computationally effective transfer learning approach that is pre-trained on a large corpus, fine-tuned with the target dataset, and later the classifier is trained with labeled data for Authorship Attribution in Bangla Literature (AABL). To the best of our knowledge, no work has been done to leverage the power of transfer learning for AABL, which can immensely reduce manual labor and enhance model re-usability manifold. Experimental results show that the proposed model considerably outperforms the existing models and achieves state-of-the-art performance, efficiently solving the limitations of the previous works. 
- The various language models trained in this work can be used as pre-trained models for many downstream tasks in the  Bangla language. All of these pre-trained models, along with the code and dataset of this paper, have been released for public use.

**All models, along with the datasets have been released in this repository.**

Our academic paper on Authorship Attribution in Bangla language can be found [here](to be updated).

## Paper Abstract
Authorship Attribution is the task of creating appropriate characterization of texts that captures the authors' writing style to identify the original author of a given piece of text. With increased anonymity on the internet, this task has become increasingly crucial in various fields of security and plagiarism detection. Despite significant advancements in other languages such as English, Spanish, and Chinese; Bangla lacks comprehensive research in this field due to its complex linguistic feature and sentence structure. Moreover, existing systems are not scalable with increasing number of authors, and performance drops with small number of samples per author. In this paper, we propose the use of Average-Stochastic Gradient Descent Weight-Dropped Long Short-Term Memory (AWD-LSTM) architecture and an effective transfer learning approach that addresses the problem of complex linguistic feature extraction and scalability for authorship attribution in Bangla Literature (AABL). We analyze the effect of different tokenization, such as word, sub-word, and character level tokenization, and demonstrate the effectiveness of these tokenizations in the proposed model. Moreover, we introduce the publicly available Bangla Authorship Attribution Dataset of 16 authors (BAAD16) containing 17,966 sample texts and 13.4+ million words to solve the standard dataset scarcity problem and release six variations pre-trained language models for use in any Bangla NLP downstream task. For evaluation, we used our developed BAAD16 dataset as well as other publicly available datasets. Empirically, our proposed model outperformed state-of-the-art models and achieved 99.8% accuracy in the BAAD16 dataset. Furthermore, we showed that the proposed system scales much better with increasing number of authors, and the performance remains steady even with small number of samples.

## Code
This repository is structured in the following way:
- **Model**: Contains all the model training and testing code for the proposed method of the paper. Further subdivided into folders containing 3 types of tokenization.
    - Character-level starter code: [character news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Character-level/.ipynb), [character news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Character-level/.ipynb) 
    - Subword-level starter code: [subword news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Subword-level/.ipynb), [subword wiki](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Subword-level/.ipynb)
    - Word-level starter code: [word_news](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Word-level/.ipynb), [word_wiki](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model/Word-level/.ipynb)
- **Others Models**: Contains tests on previously published models for comparison.

## Datasets
#### Pre-training datasets:
- [News dataset](https://data.mendeley.com/datasets/xp92jxr8wn/1?fbclid=IwAR09nbvU3G4tNoI6zuLoL3FMhvggdE6RuLFOyKMHubrHd7PivLGJeCTch9k): A corpus on Bangla newspaper articles created using a custom web crawler containing 12 different topics. [Paper reference](https://link.springer.com/chapter/10.1007/978-981-15-3607-6_31)
- [Wikipedia corpus](https://data.mendeley.com/datasets/3ph3n78fp7/1?fbclid=IwAR2qOFI27mVQoEMdJBUinL0k_zCjzEMpnFk74cKANhil7oKGSgbT_6E8keI): The Bangla Wikipedia dump collected on 10th June, 2019. Cleaned and arranged into samples in csv.

#### Authorship Attribution datasets:
- BAAD16: The published dataset with sample Bangla texts from 16 authors in an unbalanced manner to mimic real world scenarios closely and test model robustness. Equally partitioned with each document having 750 words.
    - [In Huggingface](https://huggingface.co/datasets/Aisha/BAAD16)
    - [In Mendeley](https://data.mendeley.com/datasets/6d9jrkgtvv/4)
- BAAD6: A dataset consisting of text samples from 6 authors with 350 samples per author. [Paper reference](https://ieeexplore.ieee.org/document/8631977).
    - [In Huggingface](https://huggingface.co/datasets/Aisha/BAAD6)
    - [In Mendeley](https://data.mendeley.com/datasets/w9wkd7g43f/5)

## Trained Models
All trained model checkpoints are provided in the folder [Model Checkpoints](https://github.com/tanny411/Authorship-Attribution-using-Transfer-Learning/blob/master/Model%20Checkpoints). The language models have been trained on Bangla news corpus and Wikipedia dumps. Further, there are 3 variations to each. Word, Subword and Character level tokenized, making a total of 6 pre-trained language models.

### Reproducibility
To reproduce the pre-training, fine-tuning, or classification of these models:
- Clone the repository
- Download relevant files/checkpoints from [this drive link]() and put them inside `Model Checkpoints` folder. Maintain the folder structure as in the drive folder.
- Make sure you have Python3.x
- Install requirements.txt. `pip install requirements.txt`
- Run the python notebooks (extra dependencies are installed in the notebook)

## Future Work:
- Assessing application of pure-Bangla tansformer based pre-trained models.
- CNN architecture based transfer learning for authorship attribution.
- Cross-lingual authorship attribution.
