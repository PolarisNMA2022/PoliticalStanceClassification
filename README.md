# PoliticalStanceClassification

## Introduction

This is a repository collecting all the codes and data of the project done by Team "Polaris" at NMA 2022 Deep Learning Boot Camp. We use logistic regressions and neural networks applied to articles of news data from [BIGNEWS](https://github.com/launchnlp/POLITICS) to make classification of its political stance, among left, center, and right.

Specifically, we make a prediction on the political stance of the article based on the whole article (logistic regression) or first 512 words (BERT) or 1000 words (Longformer) of the article.

This is intended as a demonstrate of the applications on this data set.

## BIGNEWS Dataset

The [POLITICS project](https://github.com/launchnlp/POLITICS) provides the BIGNEWS data set, collecting 3,689,229 English news articles on politics, gathered from 11 United States (US) media outlets covering a broad ideological spectrum, with its political orientation was classified based on their media outlets.

We focus on randomly sampled 255,000 articles, consisting of three chunks containing 85,000 articles from left, center, and right respectively. Our dataset can be obtained via [this link](https://drive.google.com/drive/folders/1HVmXj-dzE0WfLxuOiT4dCcuKpd7ujOOo?usp=sharing)

## Getting Started

We assume that your machine has a python with packages as below. Try below commands.

```
!pip install numpy 
!pip install pandas 
!pip install torch
!pip install tqdm
!pip install scikit-learn
!pip install scikit-plot
```

## Project Structure

The work here is divided across four notebooks:

- [Notebook 1: Logistic Regression]()
  - We adopt the logistic regression as a baseline model for predicting political stance. It has a final test accuracy of 67%.
- [Notebook 2: Multi-Layer perceptron (MLP) using pretrained FastText Embeddings]()
  - We use context-insensitive MLP using pretrained FastText Embeddings. It has final test accuracy of 64%.
- [Notebook 3: Neural network with pretraiend BERT Layer](notebooks/Political_stance_classification_using_BERT.ipynb)
  - We made a neual network with 4 layers to classify political stance using first 512 words of the articles with BERT Language model. It has a final accuracy of 85% after training 5 epochs.
- [Notebook 4: Neural network with pretraiend Longformer Layer]()
  - We made a neual network with 4 layers to classify political stance using first 1000 words of the articles with Longformer Language model. It has a final accuracy of 91% after training 2 epochs.

Notes the except the Notebook1, other notebooks above are saved with [dummy data](). The link of binary files of the neural network models trained by the original 204,000 articles can be found in the notebook below.

- [Classify your text's political orientation]() 
  - Using the link of pretrained models in this notebook, you can test your own text's political orientation.

## Documentation

[Abstract](https://docs.google.com/document/d/1uBWZooerQSk8PmtrDBZtR850WxHowzmCEZ_pSW9FasQ/edit?usp=sharing)

[Presentation slide](https://docs.google.com/presentation/d/1iYPFpMIYJ0tZMFMXth1qcTFEZ7nMG3BIJcqPQ_7nJvU/edit?usp=sharing).

## Authors

- Aahana Bajracharya
- Tessa Rusch 
- Jacob Elder
- Zehan (Allen) Zhao
- Israel Gonzalez-Brooks
- Byeongsu Yu

## License

Since we are allowed to use the data as an educational purpose only. Please do not use the data with other purpose.
