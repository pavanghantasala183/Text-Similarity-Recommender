# Text-Similarity-Recommender
# Business Problem  

Craigslist is an open platform used for posting classified advertisements. These advertisements can be related to products, properties, skills, jobs or even discussions. One such scope of work covered on Craigslist is Job advertisement and Resumé advertisement.   

Job seekers post their resumés and job providers post the advertisements on the platform. Currently, there is no mechanism to connect seekers and providers.   

The effort an advertiser spends on searching for relevant job advertisement or searching for the right candidate is high as they need to go through several postings to find the perfect match.  

An automated process would reduce this effort and increase advertiser interaction and user-friendliness of Craigslist.  

# Identified Solution/Improvement  

Through this project, we aim to build a recommendation system on Craigslist website which can suggest relevant job postings to job seekers and potential candidates to job advertisers through similarity measurement of the text in these advertisements. Each jobseeker will be notified of the best matching advertisements and similarly each advertiser will be notified of the best matching candidates. This reduces the time-consuming effort spent in searching and filtering.  

This enhancement will assist employers in reaching out to relevant candidates much faster. Hence, we aim to improve the user experience by finding the best match of job profiles with job advertisements.   

# Methodology 

This improvement has been implemented as follows -  

Scraped 700 job descriptions data of major cities such as Seattle, Chicago, New York, New Jersey, Boston, Austin from the Craigslist website using python modules such as Selenium, BeautifulSoup and URLlib.  

Scraped 680 resumé descriptions data of same cities from the Craigslist website.  

Cleaned the data by removing stop-words, punctuations, html tags etc.  

Tokenized both the job description documents as well as the resumé description documents. 

Normalized the tokens through lemmatization.  

Vectorized the above cleansed descriptions by document embedding techniques such as Bag-of-Words, TF-IDF (Min document frequency 6 and n-grams 1-5) 

Applied classic, unsupervised, and supervised models for calculating text similarity and matching relevant documents. Used Bert model for word embedding and Word2Vec model for supervised modelling. 

# Model Design: 

Given a collection of documents D = {d1, d2,.….., dn} and a source document s ∈ D, the goal is to quantify a score that would allow us to rank all the other documents in D according to their semantic similarity with the source documents. This problem has two key components, which are Document Embedding and Similarity Metric. 

Document Embedding is converting text in the document to a vector form. Semantic Textual Similarity is a task in the area of Natural Language Processing (NLP) that scores the relationship between texts or documents using a defined metric. Semantic Similarity has various applications such as information retrieval, text summarization, sentiment analysis, etc. 

There have been a lot of approaches for Semantic Similarity. The most straightforward and effective method now is to use a powerful model to encode sentences and get their embeddings and then use a similarity metric (e.g., cosine similarity) to compute their similarity score. The similarity score indicates whether two texts have similar or more different meanings.  

# Model description:  

To model the textual data and map two texts together, order information is important. Naive approaches like Bag of Words may not accurately represent the differences between documents. Various numeric representations like TF-IDF (Term frequency and Inverse document Frequency), One-hot Encoding and Word Embeddings were used to capture both the content and the order information. Word embeddings are the current best representations for training advanced models like LSTM, and Deep Neural Networks. They reduce the dimensionality by mapping sentences or documents of varied lengths to pre-determined vectors of less dimensions. Based on performance requirements for the model, various word embedding techniques such as Glove, Word2Vec can be applied and similarity of the job posting, and the resumé description is calculated. Following approaches have been taken to model text similarity: 

Approach 1: Similarity measure using Cosine distance

Approach 2a: K means clustering (a descriptive model using Euclidean distance) 

Approach 2b: Agglomerative clustering 

Approach 3: Sentence Transformers (S-BERT) 


Approach 4:  Siamese Bi-LSTM Model 
 

# Value addition to the Craigslist: 

For craigslist users, both employers and job seekers, this recommendation system would be indispensable in matching the job listings with the potential candidates. They can send recommendations of job postings tailored to the resumé descriptions and potential hire information to the employers based on the content of their openings. User engagement and customer satisfaction will be increased with improved and more relevant recommendations. 

