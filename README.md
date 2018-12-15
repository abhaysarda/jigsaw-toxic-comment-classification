## Toxic Comment Classification
Our project is heavily based on the kaggle competition organized by Jigsaw. Link: https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge

## Dependencies

We assume you have python 3.5+ installed. Follow the instructions to set up your conda environment, and finally download all of nlkt's packages by using the following steps.
1. Go to a python command line
2. `import nltk`
3. `nltk.download()`

Before you run our LSTM implementation, you need to download the GloVe embeddings, which are about 5.4gb unzipped. The link is: https://nlp.stanford.edu/projects/glove/ 840b embeddings to 300 dimensions.
## Pipeline
Our entire process consists of three steps. At the first step, we preprocess the data, by exploring different techniques of removing stopwords, lemmatization, etc. The best performing one goes to our next step, which is word embeddings. At this step, we explore different techniques such as count-based vectorizers, tf-idf vectorizers and word2vec. Again, the best performing technique is used in many different classifiers. All of which are in the Classifiers folder.

## Comparison of human performance

We also compared our algorithms performance with an average human's performance over 1000 test samples. We found that most of our algorithms with tuned parameters outperform a human at the same task.

## How to use our code
Since we are using python, the best way to test out code will be using a virtual environment. We recommend installing anaconda first, using their webpage. https://www.anaconda.com/

Once you are done with that, open a command line console and type the following:
`conda env create -f toxic-comments.yaml`

This will create a new environment, named "toxic-comments" which you can then activate before running our code. To activate an environment, go to a command line and type:
`source activate toxic-comments` on MAC/Linux
`activate toxic-comments` on Windows

Now you can run any of our programs!

1. Conversion from kaggle data to a binary class problem is done by a file inside the data folder -> Raw_data -> data_from_kaggle.ipynb

2. Preprocessing the data is done by the notebook in /data/preproccesed_data called preprocessed.ipynb

3. The different word2vec implementations are in the word2vec folder in the root directory.

4. The many different classifiers are in the classifiers folder.

5. Our human benchmark is in the human_performance folder in the root directory

Acknowledgements:
Our LSTM implementation has been largely adapted from this kaggle kernel:https://www.kaggle.com/qqgeogor/keras-lstm-attention-glove840b-lb-0-043/comments. All other work is our own. The notebook has a few mistakes but talks a lot about LSTMs with attention, therefore please use our version which is fixed.
