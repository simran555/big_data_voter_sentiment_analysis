# LEVERAGING BIG DATA IN TIME SENTIMENT ANALYSIS AND VOTER ANALYSIS FOR US Election 2024
This project examines big data technologies to analyze voter sentiment during recent elections. It decodes millions of Reddit conversations using HDFS for data storage and NLP models like Naïve Bayes and BERT.
It provides useful information for researchers, campaign teams, and policymakers by shedding light on the distribution of sentiment and polarization in political discourse

METHODOLOGY:
Our methodology for voter sentiment analysis involves a comprehensive approach leveraging big data technologies and advanced machine learning models. The process consists of three key steps:

A.	Data Collection and Cleaning
	We used data from Reddit, a site full of user-generated debates, as the basis for our Sentiment Analysis and Voter Insights for the 2024 Election project. Election-related posts and comments were our focus since they offer important insights into the attitudes and viewpoints of the general population. A strong data collecting and cleaning pipeline was put in place to guarantee that the data gathered was of the highest calibre, dependable, and prepared for analysis.
 
 B.	HDFS Configuration and Data Storage
To store and retrieve the Reddit data efficiently, we set up the Hadoop Distributed File System (HDFS). The Hadoop Distributed File System (HDFS) was used to store and administer the Reddit data that was gathered. 

C.	Sentiment Analysis Model Training

This project uses Naïve Bayes for voter sentiment analysis on Reddit data, leveraging its efficiency in text classification. To address class imbalance, Complement Naïve Bayes (CNB) is applied, reducing the dominance of majority classes. Techniques like SentimentIntensityAnalyzer, WordNetLemmatizer, TfidfVectorizer, and SelectKBest enhance accuracy by refining feature selection and capturing nuanced sentiment.

This project uses BERT for voter sentiment analysis on Reddit, leveraging its bidirectional context understanding and pre-training on large datasets for accurate interpretation of complex political language. BERT’s ability to handle idioms, slang, and intricate grammar enhances accuracy. Components like BertTokenizer, BertForSequenceClassification, and Trainer optimize the model for sentiment prediction.
