## TED Talk Topic Modeling

This project aims to explore topic modeling on a dataset of TED Talk transcripts using natural language processing techniques. 
The Kaggle TED Talks dataset was utilized, and the top 20% most viewed transcripts were selected for analysis.
The data preprocessing phase involved tokenization, filtering, spotting bigrams, and lemmatization using the NLTK and Gensim Python libraries.
These steps ensured that the data was cleaned and ready for topic modeling.

### About the Dataset

The dataset contains comprehensive information about TED Talks, including metadata, transcripts, ratings, and other attributes. 
It was scraped from the official TED website and is available under the Creative Commons License.
The dataset comprises two CSV files: ted_main.csv and transcripts.csv, containing details about talks, speakers, and transcripts.

### Data Processing Techniques

#### Tokenization and Filtering
Tokenization breaks down the transcripts into individual words or tokens, allowing for a detailed analysis of the textual data. 
Filtering removes short words with fewer than three characters, eliminating noise and irrelevant information from the tokenized data.

#### Spotting Bigrams
Spotting bigrams identifies frequent two-word combinations within the tokenized data, capturing meaningful phrases and contextual relationships between words.
This technique uncovers language patterns and expressions that contribute to the success of presentations.

#### Lemmatization
Lemmatization reduces words to their base or dictionary form, normalizing inflected forms and grouping related words together.
This process helps identify common themes and topics across presentations by capturing the core meanings of words.

### Data Representation
The preprocessed transcripts were represented in a Document-Term Matrix (DTM) or bag-of-words (BOW) format using the Gensim library.
This representation captures the frequency of words or bigrams in each transcript, forming the basis for topic modeling analysis.

### Latent Dirichlet Allocation (LDA)
LDA is a generative statistical model widely used in topic modeling. 
It assumes that documents in a corpus consist of a mixture of latent topics, and these topics are characterized by the distribution of words they contain.
LDA allows us to discover these latent topics by analyzing word occurrences and distributions across the corpus.

Key Features of LDA:
- Probabilistic Modeling: models the relationships between words and topics in a probabilistic framework, capturing the inherent uncertainty and variability in language usage.
- Unsupervised Learning: operates without the need for pre-defined topics or labeled training data, making it suitable for exploratory analysis of large text datasets.
- Flexible and Interpretable: enables specifying the desired number of topics, providing control over the granularity of the analysis. It represents each topic as a distribution of words, enhancing interpretability and practicality.

In this project, we aim to predict the greatness of a presentation based on its transcript. 
We propose using LDA topic modeling techniques to identify the factors contributing to presentation greatness.
To achieve this, two classifiers are considered: Random Forest and Naive Bayes.

Random Forest:
-  handles imbalanced datasets effectively by employing a bagging technique, preventing dominance of the majority class.
-  provides a measure of feature importance, aiding in understanding the key factors that make a presentation great.
-  captures non-linear relationships between features and the target variable, accommodating complex interactions and dependencies.

Naive Bayes:
-  computationally efficient and requires less training data, enabling faster model training and inference.
-  suitable for high-dimensional data, assuming independence among features and preventing overfitting.
-  handles irrelevant or redundant features gracefully, assigning low weights to them.
