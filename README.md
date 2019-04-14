# Jigsaw-Unintended-Bias-in-Toxicity-Classification
Kaggle Competition on NLP: Detect toxicity across a diverse range of conversations. Here is the link: [Jigsaw Unintended Bias in Toxicity Classification](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/overview)

Here’s the background: When the Conversation AI team first built toxicity models, they found that the models [incorrectly learned to associate](https://medium.com/the-false-positive/unintended-bias-and-names-of-frequently-targeted-groups-8e0b81f80a23) the names of frequently attacked identities with toxicity. Models predicted a high likelihood of toxicity for comments containing those identities (e.g. "gay"), even when those comments were not actually toxic (such as "I am a gay woman"). This happens because training data was pulled from available sources where unfortunately, certain identities are overwhelmingly referred to in offensive ways. Training a model from data with these imbalances risks simply mirroring those biases back to users.

In this competition, we're challenged to build a model that recognizes toxicity and minimizes this type of unintended bias with respect to mentions of identities. We'll be using a dataset labeled for identity mentions and optimizing a metric designed to measure unintended bias. Develop strategies to reduce unintended bias in machine learning models, and we'll help the Conversation AI team, and the entire industry, build models that work well for a wide range of conversations.


## Step 1: Clean the data
[Code: Jupyter Notebook](I didn't post the notebook yet.)
1. Replace punctuations such as “(),!?@\'\`\"\_\n]” to space
2. Convert all characters to lowercase, in order to treat words such as “hey”, “HEY”, and “Hey” the same (But I may lose the emotion feeling like yelling through all captial words.)
3. Consider combining misspelled or alternately spelled words to a single representation (e.g.“hey”/”heyyyy”)
4. Consider lemmatization (reduce words such as “am/are/is” to a common form such as “be”)
5. Tokenize text by separating it into individual words
6. Save as [clean_data.csv]. (I did not post the csv yet)


## Step 2: Build up Models -> check classification by t-SNE
1. One-hot encoding (Bag of Words) 
2. Logistic Regression
3. TF-IDF
4. Word2Vec
5. LSTM


## Reference
[How to solve 90% of NLP problems: a step-by-step guide](https://blog.insightdatascience.com/how-to-solve-90-of-nlp-problems-a-step-by-step-guide-fda605278e4e)

