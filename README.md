## Toxic Comment Classification
Our project is heavily isnpired by the <a href="https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge">Jigsaw Toxic Comment Classification challenge</a> on Kaggle.

## Dependencies

We assume you have python 3.5+ installed. Follow the instructions below to set up your conda environment(we have provided the .yaml file) and finally, download all of nltk's packages by using the following steps on a python command line.
2. `import nltk`
3. `nltk.download()`

Before you run our LSTM implementation, you also need to download the GloVe embeddings, which are about 5.4gb unzipped. Here is the <a href="https://nlp.stanford.edu/projects/glove/">link</a>. Download the file for the Common Crawl 840b embeddings, 300 dimensions.

## Pipeline
Our entire process consists of three steps. At the first step, we preprocess the data, by exploring different techniques of removing stopwords, lemmatization, etc. The best performing one goes to our next step, which is word embeddings. At this step, we explore different techniques such as count-based vectorizers, tf-idf vectorizers and word2vec. Again, the best performing technique is used in many different classifiers.

## Comparison of human performance

We also compared our algorithms performance with an average human's performance over 1000 test samples. We found that most of our algorithms with tuned parameters outperform a human at the same task.

## How to use our code
Since we are using python, the best way to test out code will be using a virtual environment. We recommend installing <a href="https://www.anaconda.com/"> anaconda </a>first.

Once you are done with that, open a command line console and type the following. (Make sure Anaconda is in your path!)
`conda env create -f toxic-comments.yaml`

This will create a new environment, named "toxic-comments" which you can then activate before running our code. To activate an environment, go to a command line and type:
`source activate toxic-comments` on Mac/Linux
`activate toxic-comments` on Windows

Now you can run any of our programs!

1. Conversion from kaggle data to a binary class problem is done by a file inside the data folder -> Raw_data -> data_from_kaggle.ipynb

2. Preprocessing the data is done by the notebook in preprocessed data folder.

3. The variety of feature extraction techniques are in the feature extraction folder.

4. The various techniques that we tried are in the model folder.

5. Our human benchmark is in the human performance folder.

Acknowledgements:
Our LSTM implementation has been adapted from this kaggle kernel:https://www.kaggle.com/qqgeogor/keras-lstm-attention-glove840b-lb-0-043/comments. All other work is largely our own. The notebook has a few mistakes but talks a lot about LSTMs with attention, therefore please use our version which is fixed.
