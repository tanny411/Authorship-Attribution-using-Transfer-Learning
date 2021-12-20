## Model Checkpoints

Several models were trained and fine-tuned to perform classification for Authorship Attribution in Bangla Literature. This folder and readme help keep track of all these model checkpoints. Especially the checkpoints from training models with news corpus and bn.wikipedia.org dumps serve as pre-trained language models for any Bangla downstream tasks.

Basically:
1. A langauge model is trained on a large text corpora. This can be either the News corpus, or the Wikipedia dumps.
2. For each of these pre-trained models, the language models are fine-tuned in a authorship attribution datase (BAAD6 or BAAD16). This langauge model's checkpoint is available as the whole model (suffixed with `body`), or only the `encoder`. Encoder is the entire model without the final classification layer. This encoder can be loaded to perform authorship attribution classification in other datasets as well.
3. Finally the classification model's checkpoint for each authorship attribution dataset is provided. These models can be loaded to perform classification as required.


The list below gives a breakdown of all the model checkpoints. All model checkpoints can be found here: [Drive Link](https://drive.google.com/drive/folders/13UcUV4csh_klU2po-UZQeiKEcQQAlEiS?usp=sharing)

- Pre-training on **News Corpus**
    - Word level tokenization
        - Word tokenized language model pre-trained on News corpus. This model can be used for down-stream tasks.
        - Authorship Attribution
            - BAAD6
                - Model fine-tuned on BAAD6 dataset (body and encoder)
                - Final classification model checkpoint of BAAD6 dataset. Can be used to perform Authorship Attribution in Bangla.
            - BAAD16
                - Model fine-tuned on BAAD16 dataset (body and encoder)
                - Final classification model checkpoint of BAAD16 dataset. Can be used to perform Authorship Attribution in Bangla.
    - Sub-word level tokenization
        - Sub-word tokenized language model pre-trained on News corpus. This model can be used for down-stream tasks.
        - Authorship Attribution
            - BAAD6
                - Model fine-tuned on BAAD6 dataset (body and encoder)
                - Final classification model checkpoint of BAAD6 dataset. Can be used to perform Authorship Attribution in Bangla.
            - BAAD16
                - Model fine-tuned on BAAD16 dataset (body and encoder)
                - Final classification model checkpoint of BAAD16 dataset. Can be used to perform Authorship Attribution in Bangla.
    - Character level tokenization
        - Character tokenized language model pre-trained on News corpus. This model can be used for down-stream tasks.
        - Authorship Attribution
            - BAAD6
                - Model fine-tuned on BAAD6 dataset (body and encoder)
                - Final classification model checkpoint of BAAD6 dataset. Can be used to perform Authorship Attribution in Bangla.
            - BAAD16
                - Model fine-tuned on BAAD16 dataset (body and encoder)
                - Final classification model checkpoint of BAAD16 dataset. Can be used to perform Authorship Attribution in Bangla.
- Pre-training on **Bangla Wikipedia Corpus**
    - Word level tokenization
        - Word tokenized language model pre-trained on Bangla Wikipedia corpus. This model can be used for down-stream tasks.
        - Authorship Attribution
            - BAAD6
                - Model fine-tuned on BAAD6 dataset (body and encoder)
                - Final classification model checkpoint of BAAD6 dataset. Can be used to perform Authorship Attribution in Bangla.
            - BAAD16
                - Model fine-tuned on BAAD16 dataset (body and encoder)
                - Final classification model checkpoint of BAAD16 dataset. Can be used to perform Authorship Attribution in Bangla.
    - Sub-word level tokenization
        - Sub-word tokenized language model pre-trained on Bangla Wikipedia corpus. This model can be used for down-stream tasks.
        - Authorship Attribution
            - BAAD6
                - Model fine-tuned on BAAD6 dataset (body and encoder)
                - Final classification model checkpoint of BAAD6 dataset. Can be used to perform Authorship Attribution in Bangla.
            - BAAD16
                - Model fine-tuned on BAAD16 dataset (body and encoder)
                - Final classification model checkpoint of BAAD16 dataset. Can be used to perform Authorship Attribution in Bangla.
    - Character level tokenization
        - Character tokenized language model pre-trained on Bangla Wikipedia corpus. This model can be used for down-stream tasks.
        - Authorship Attribution
            - BAAD6
                - Model fine-tuned on BAAD6 dataset (body and encoder)
                - Final classification model checkpoint of BAAD6 dataset. Can be used to perform Authorship Attribution in Bangla.
            - BAAD16
                - Model fine-tuned on BAAD16 dataset (body and encoder)
                - Final classification model checkpoint of BAAD16 dataset. Can be used to perform Authorship Attribution in Bangla.
    
