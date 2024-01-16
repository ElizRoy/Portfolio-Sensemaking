# Portfolio-Sensemaking

Region and Country Programme documents will be used to mine for data on projects,policies, partnerships, risks, results etc. These documents are available on the UNDP regional webpages.  

Using webcrawling, these documents are extracted, the text is parsed, tokenized and vectorized for NLP natural language processing models. Topic Modeling and Word embedding of the text data is performed to get insights and get answers to the research questions. 

Before any information can be extracted from the text, the data is preprocessed and cleaned using the python libraries, NLTK and Inflect. The texts are converted to tokens or words and converted to lowercase. Numbers are converted into words. Whitespaces, Stopwords and punctuations from the texts are removed. Word roots are found by stemming and lemmatization.  

The parts of speech of words are extracted and a part of speech tag is attached to each word. CC for a coordinating conjunction; RB for adverbs; IN for a preposition; NN for a noun and JJ for an adjective.  

To get information on the relationships between the different entities, Named Entity Recognition classifier is used to tag words that are Named entities as NE; and others as PERSON, DATE, LOCATION, TIME, MONEY, PERCENT, FACILITY, ORGANIZATION, and GPE (geo political entities such as city, state, place, country). 
Methodology 
The texts from the documents are split into tokens after cleaning. These tokens are analyzed using unsupervised learning techniques.  
# Models  
Clustering and topic modeling techniques have been used on the words/topics of the documents to analyze and create NLP models. 
Topic Modeling: LDA (Latent Dirichlet Allocation) topic modeling is done using an LDA Mallet Model. This module, collapsed gibbs sampling from MALLET, allows LDA model estimation from a training corpus and inference of topic distribution. The syntax of that wrapper is gensim.models.wrappers.LdaMallet. 
Clustering: K-means clustering model and Dendogram based hierarchical clustering models are trained on the tokenized data. 

# Features 
2 Word Embedding methods were used to extract features. 
TF-IDF was implemented to extract the vectorized measure of originality of the words in the documents. 
Word2Vec was implemented to extract training model with vectors of words with more than 5 occurrences. Semantic is given importance in this method. 

# Model Training 
Topic Modeling: The corpus, dictionary and number of topics is fed to the LDAmalletmodel. 
To examine the produced topics and the associated keywords, we use pyLDAvis package's interactive chart. 
Topic distribution across documents, dominant topic in each document and the most representative document for each topic are determined and explored. 
Clustering: Application of K means clustering with 5 clusters gives 10 documents forming a cluster and 9 forming another cluster. The remaining 5 documents are spread between 3 clusters.  
Hierarchical document clustering is done using the cosine distance and reveals 7 clusters.  

# Model Evaluation  
The performance of the LDA Mallet model is evaluated using the coherence score. 
For 10 topics, the model performed with a coherence score of 0.76.  
