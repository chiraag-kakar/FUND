# Fake Unreliable News Detection (FUND)
FUND is a system to identify unreliable news articles and accurately classify each piece of news as Real or Fake.

A type of yellow journalism, fake news encapsulates pieces of news that may be hoaxes and is generally spread through social media and other online media. 
This is often done to further or impose certain ideas and is often achieved with political agendas. 
Such news items may contain false and/or exaggerated claims, and may end up being viralized by algorithms, and users may end up in a filter bubble.

# Data
The dataset [news.csv](https://github.com/chiraag-kakar/FUND/blob/master/news.csv) is political in nature , has a shape of 7796 x 4.
The first column identifies the news, the second and third are the title and text, and the fourth column has labels denoting whether the news is REAL or FAKE.

While the actual [Kaggle Data](https://www.kaggle.com/c/fake-news/data) has the following description:

#### train.csv : A full training dataset with the following attributes:

* id: unique id for a news article
* title: the title of a news article
* author: author of the news article
* text: the text of the article; could be incomplete
* label: a label that marks the article as potentially unreliable
         * * 1: unreliable
         * * 0: reliable

#### test.csv : A testing training dataset with all the same attributes at train.csv without the label.

## Prerequisites :
To get the copy of the project up and running on the local machine for development and testing purposes following python libraries need to be installed : 
numpy , pandas and sklearn.


```shell
pip install numpy pandas sklearn

```

## Dependencies Explained:

**TfidfVectorizer**


**TF** (Term Frequency): The number of times a word appears in a document is its Term Frequency. A higher value means a term appears more often than others, and so, the document is a good match when the term is part of the search terms.

**IDF** (Inverse Document Frequency): Words that occur many times a document, but also occur many times in many others, may be irrelevant. IDF is a measure of how significant a term is in the entire corpus.

---
The TfidfVectorizer converts a collection of raw documents into a matrix of TF-IDF features.


**PassiveAggressiveClassifier**
Passive Aggressive algorithms are online learning algorithms. 
Such an algorithm remains passive for a correct classification outcome, and turns aggressive in the event of a miscalculation, updating and adjusting. 
Unlike most other algorithms, it does not converge. 
Its purpose is to make updates that correct the loss, causing very little change in the norm of the weight vector.

# Implementation Overview:
A Tfidfvectorizer is built on the dataset, then a Passive Agressive Classifier is initialized.
We will then fit our model and end up obtaining an accuracy of 92.66% in magnitude.


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Kaggle



