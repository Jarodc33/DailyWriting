Natural language processing is a recent field in machine learning that is able to be used for math, prediction and many other things. One simple thing that it can be used for is classifying bodies of text. This can easily be done in scikit-learn after a bit of preprocessing.
First certain words should be taken out because they are too common or don't give information about the actual content. These words are commonly called stopwords and can be accesed in the nltk library in python ```python set(nltk.corpus.stopwords.words('english'))```. once these words are removed you can also choose to cut words down to their base, this is called stemming or lemmatization. Once all the preprocessing is done sklearn can be used to vectorize the text and a classification model can be used on the text.