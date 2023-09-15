# Twitter Sentiment Analysis Project
![image](https://github.com/valarythairu/Sentiment-Analysis/assets/132980723/f6358118-4a2f-495b-a9e7-1b89af612e0f)


### 1. Business Understanding
I have been tasked with undertaking a sentiment analysis project for a company. This project aimed to analyze the emotion expressed in customer-generated text data, which in this case are tweets from the social media platform, Twitter, regarding specific brands and products. These tweets were rated by human raters who expressed their opinions on the tweets and identified them as either positive, negative, or other emotions. The objective of this project was to build a model that can rate the feeling of a tweet based on its content just like the human raters.

#### 2. Data Understanding
The dataset provided had three real-time columns:

i) Tweet_text: These were texts that in the form of tweets shared the emotions and opinions of customers on the company's products via Twitter.

ii) Emotion_in_tweet_directed_at: These were the products that customers tweeted expressing how they felt about them and after reviewing the dataset there were many different emotions directed at these products expressed by customers.

iii) is_there_an_emotion_directed_at_a_brand_or_product: These are the emotions that human raters gave as their opinion regarding tweets that customers posted directed towards the company's products.

### 3. Main Objective
- The main aim of this project was to build a model that determines whether the sentiment of a tweet about the company's products is positive or negative or any other emotion based on the content of the tweet.

### 4. Specific Objectives
- Binary Classifier: By first quantifying tweets that expressed negative and positive only, building a model that classifies only two emotions/sentiments first limits analysis to positive and negative tweets only.

- Multi-class Classfier: Building a model that includes any other tweets apart from positive and negative tweets such as neutral tweets hence building a model that classifies more than two emotions/sentiments.

### 5. Exploratory Data Analysis
- The dataset contained the company's products and the emotion that tweeters expressed which I visualized in the diagram below and was able to establish the products that had drawn more attention to customers than others.
  ![image](https://github.com/valarythairu/Sentiment-Analysis/assets/132980723/ffc13506-4b43-41be-8b8d-7485b38539f7)

- I also visualized the different emotions that were expressed in the tweets to identify the different emotions that human raters recorded.
  ![image](https://github.com/valarythairu/Sentiment-Analysis/assets/132980723/832a26f4-eb8e-4bfa-bcf8-f6761e850461)

### 6.
### i)Modelling -> Building a Binary Classifier
- I tokenized the tweets in the dataset and converted them into a sequence of tokens.
- I applied Word Embeddings as the Vectorization strategy.
- I narrowed down to negative and positive tweets and built a model to only predict these two types of tweets.
- I built a Binary Classifier with the Long Short Term Memory Cells(LSTM) Network that is part of Recurrent Neural Networks(RNN) and applied the Early Stopping Regularization Technique.
- I obtained results as such; an accuracy of `0.823` and a loss of `1.82`.
- Loss -> Measures how far off the predicted emotions by the model are from the actual emotions.
- Accuracy -> Measures how accurate the model is at predicting emotions in tweets.

### ii) Modelling -> Building a Multi-class Classifier
- I built a Multi-class Classifier with the Long Short Term Memory Cells(LSTM) Network that is part of Recurrent Neural Networks(RNN) and applied Dropout and L2 regularization techniques.
-  I applied Word Embeddings as the Vectorization strategy in the LSTM Network.
- I also built a Multi-class Classifier with Logistic Regression, Support Vector Machines, and a Random Forest Classifier and applied the TF-IDF Vectorization Strategy for each model.
- As displayed in the notebook among all the machine learning models run in the entirety of the notebook, `Logistic Regression model` had the best accuracy score for our Multi-class Classifier.
- The model had an `accuracy score` of `0.676`, `the highest accuracy obtained`.
  
- In addition to the steps mentioned above, the following data preprocessing steps were performed:

i) Special characters were removed.

ii) Stopwords were removed.

iii) Tokenization was performed.

iv) Lemmatization was used to reduce words to their common root form

####  7. Conclusions
1. The dataset had tweets with different sentiments expressed with the highest sentiment expressed to be Negative emotion as shown below:

    i) Percentage of Negative emotion: 59.27%

    ii) Percentage of Positive emotion: 32.75%

    iii) Percentage of No emotion toward brand or product: 6.27%

    iv) Percentage of I can't tell: 1.72%

- This was a bad review in itself as it meant they had higher negative reviews than positive reviews about their products.


2. The analysis of sentiments directed towards the company's products varied from one product to the other, despite negative tweets having the highest percentage in the dataset products combined, on visualizing the products separately I was able to discover that each product had higher positive sentiments than negative, neutral and unknown sentiments directed towards them starting with:

    i)  iPad had the highest number of positive tweets, but it also had the highest number of negative tweets.

    ii) iPhone had the second highest number of negative tweets about it.

    iii) Apple products had the second highest number of positive tweets about it but also had the third highest negative tweets about it.


    iv) Android, Android apps, and other Apple products or Services had the lowest positive tweets about them.

    v) Google products had the fourth lowest negative tweets about it.

3. By visualizing the products and emotions directed towards them, I concluded that to achieve much more success, the focus should be positive and negative sentiments which gave much more valuable insight than neutral sentiments(No emotion toward brand or product) and unknown sentiments (I can't tell).

#### 8. Recommendations

1. Despite the model with the highest accuracy being the Logistic Regression model with an `accuracy score` of `0.676`, I would recommend the LSTM Network part of the RNN(Recurrent Neutral Architecture) architecture to the company as the model to use to rate the sentiments in the tweets about their products as it is able to capture as much information as possible effectively without having difficulty learning long-term dependencies. 

2. I would recommend the company to specifically focus on improving all their products and to be particular:

    i) Focus on marketing Android, Android app, and other Apple products or Services much more as they had the least number of tweets about them, meaning customers really do not have much of an opinion towards them which would mean they are not using them.

    ii) Despite the iPad being the product with the highest tweets it also had the highest negative tweets, the company should direct resources on finding out why it had the highest negative tweets.
    
    iii) Apple and iPhone had the third and second highest negative tweets respectively, the company should also find out why is that.

3. The products from these companies all had higher positive tweets about them than negative tweets, this was a great achievement and it should also direct resources into reducing the negative tweets about them starting with looking into iPad products and why they had the highest positive and taking into consideration what got it the highest positive tweets.




  
