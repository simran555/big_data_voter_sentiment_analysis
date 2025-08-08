<b>#### Project Title: Voter Sentiment Analysis and Big Data</b>

This project focuses on leveraging big data for real-time voter sentiment analysis and voter analysis. The goal is to understand public opinion and identify trends by analyzing unstructured data from social media.

<b>#### The Problem</b>
Traditional analysis methods struggle with the vast amount of unstructured data available, leading to slow processing and a lack of scalability. This can result in missed opportunities to detect real-time sentiment shifts and inaccurate insights that hinder effective alignment with voter concerns. The project addresses these challenges by automating the analysis process to handle large datasets efficiently.

<b>#### Methodology</b>
The project followed a five-step methodology:

<b>Data Collection and Cleaning:</b> Data was collected from Reddit and preprocessed to remove noise, such as URLs, special characters, and stopwords.

<b>Hadoop Configuration:</b> The Hadoop client and HDFS (Hadoop Distributed File System) were configured for storing and retrieving the cleaned data.
<img width="956" height="350" alt="image" src="https://github.com/user-attachments/assets/86afb73a-3142-4f75-84ad-fdb62b6db179" />


<b>Training Data Preparation:</b> A training dataset was prepared for sentiment analysis.

<b>Model Testing:</b> Both Naïve Bayes and BERT models were tested on the cleaned Reddit dataset.

<b>Evaluation and Insights:</b> The models were evaluated, and key insights were derived from the results.

<b>#### Models Used</b>

<b>Naïve Bayes</b>
This model was chosen for its strengths in text classification, handling sparse data, and quick training and implementation. 
<img width="712" height="630" alt="image" src="https://github.com/user-attachments/assets/e1b36124-ecb4-4139-be19-dfba10746b9a" />

The implementation used Complement Naïve Bayes instead of Multinomial Naïve Bayes, and featured enhancements such as:

<b>VADER Sentiment Scoring:</b> Used SentimentIntensityAnalyzer from NLTK to detect positive, negative, and neutral sentiments.

<b>Feature Engineering:</b> Employed TF-IDF vectorization and N-grams to convert text into numerical data and capture word importance.

<b>Feature Selection:</b> Used SelectKBest and chi2 to optimize feature selection.

<b>Data Balancing:</b> Oversampling was used to balance the training data, specifically the minority positive and negative classes.

<b>Results:</b> The Naïve Bayes model's accuracy was improved from 18% to approximately 33% after these adjustments.


<b>BERT Model</b>
The BERT (Bidirectional Encoder Representations from Transformers) model was used for its state-of-the-art performance and contextual understanding. 
<img width="655" height="284" alt="image" src="https://github.com/user-attachments/assets/63e43f7f-3639-4237-a6a1-3fde38b9fea0" />
The implementation involved:

<b>BERT Tokenizer:</b> Converted text into tokens for model understanding.

<b>BERT Model for Sequence Classification:</b> A pre-trained model was fine-tuned for sentiment classification.

<b>Training:</b> The model was trained using a custom Trainer instance with defined TrainingArguments.

<b>Prediction:</b> Sentiments were predicted on the test data, and numeric labels were mapped back to sentiment text.

<b>Results:</b> The BERT model achieved an accuracy of 29.69%. It showed high precision in identifying positive sentiment but struggled with negative and neutral sentiments.

<b>#### Analysis and Insights</b>
The sentiment analysis was applied to data related to two political figures, Kamala Harris and Donald Trump. The analysis showed that:

<b>Kamala Harris-related data</b> had a sentiment distribution of 22.6% positive, 31.7% negative, and 45.7% neutral.

<b>Donald Trump-related data</b> had a distribution of 19.6% positive, 33.7% negative, and 46.6% neutral.

<b>#### Challenges and Limitations</b>
Several challenges were encountered during the project:

<b>Data Handling:</b> Configuration and authorization issues with PRAW for Reddit data extraction.

<b>Hadoop:</b> Permissions and user privilege issues with the HDFS root user, which prevented service startup.

<b>BERT Training:</b> Training and fine-tuning the BERT model was time-consuming, taking approximately 5 hours.

<b>Data Quality:</b> The training dataset from Kaggle had issues with sentiment labels.
