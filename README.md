<b># Project Title: Voter Sentiment Analysis and Big Data</b>

This project focuses on leveraging big data for real-time voter sentiment analysis and voter analysis. The goal is to understand public opinion and identify trends by analyzing unstructured data from social media.

<b>The Problem</b>
Traditional analysis methods struggle with the vast amount of unstructured data available, leading to slow processing and a lack of scalability. This can result in missed opportunities to detect real-time sentiment shifts and inaccurate insights that hinder effective alignment with voter concerns. The project addresses these challenges by automating the analysis process to handle large datasets efficiently.

<b>Methodology</b>
The project followed a five-step methodology:

1. Data Collection and Cleaning: Data was collected from Reddit and preprocessed to remove noise, such as URLs, special characters, and stopwords.

2. Hadoop Configuration: The Hadoop client and HDFS (Hadoop Distributed File System) were configured for storing and retrieving the cleaned data.
<img width="956" height="350" alt="image" src="https://github.com/user-attachments/assets/86afb73a-3142-4f75-84ad-fdb62b6db179" />

3. Training Data Preparation: A training dataset was prepared for sentiment analysis.

4. Model Testing:Both Naïve Bayes and BERT models were tested on the cleaned Reddit dataset.

5. Evaluation and Insights: The models were evaluated, and key insights were derived from the results.

<b>Models Used</b>

<b>1. Naïve Bayes</b>
This model was chosen for its strengths in text classification, handling sparse data, and quick training and implementation. 

<img width="712" height="630" alt="image" src="https://github.com/user-attachments/assets/e1b36124-ecb4-4139-be19-dfba10746b9a" />

The implementation used Complement Naïve Bayes instead of Multinomial Naïve Bayes, and featured enhancements such as:

* VADER Sentiment Scoring: Used SentimentIntensityAnalyzer from NLTK to detect positive, negative, and neutral sentiments.

* Feature Engineering: Employed TF-IDF vectorization and N-grams to convert text into numerical data and capture word importance.

* Feature Selection:</b> Used SelectKBest and chi2 to optimize feature selection.

* Data Balancing:</b> Oversampling was used to balance the training data, specifically the minority positive and negative classes.

* Results:</b> The Naïve Bayes model's accuracy was improved from 18% to approximately 33% after these adjustments.


<b>2. BERT Model</b>
The BERT (Bidirectional Encoder Representations from Transformers) model was used for its state-of-the-art performance and contextual understanding. 
<img width="655" height="284" alt="image" src="https://github.com/user-attachments/assets/63e43f7f-3639-4237-a6a1-3fde38b9fea0" />
The implementation involved:

* BERT Tokenizer: Converted text into tokens for model understanding.

* BERT Model for Sequence Classification: A pre-trained model was fine-tuned for sentiment classification.

* Training: The model was trained using a custom Trainer instance with defined TrainingArguments.

* Prediction: Sentiments were predicted on the test data, and numeric labels were mapped back to sentiment text.

* Results: The BERT model achieved an accuracy of 29.69%. It showed high precision in identifying positive sentiment but struggled with negative and neutral sentiments.

<b>Analysis and Insights</b>
The sentiment analysis was applied to data related to two political figures, Kamala Harris and Donald Trump. The analysis showed that:

<b>Kamala Harris-related data</b> had a sentiment distribution of 22.6% positive, 31.7% negative, and 45.7% neutral.

<b>Donald Trump-related data</b> had a distribution of 19.6% positive, 33.7% negative, and 46.6% neutral.

<b>Challenges and Limitations</b>
Several challenges were encountered during the project:

* Data Handling: Configuration and authorization issues with PRAW for Reddit data extraction.

* Hadoop: Permissions and user privilege issues with the HDFS root user, which prevented service startup.

* BERT Training: Training and fine-tuning the BERT model was time-consuming, taking approximately 5 hours.

* Data Quality: The training dataset from Kaggle had issues with sentiment labels.
