# Sentiment Analysis on Financial News Headlines

## NLP Using Neural Networks and Other Machine Learning Techniques

The purpose of this project is to start building a neural network model that can determine the sentiment of financial news headlines.  The users of this model would be investment firms who want to keep track of the market sentiment of a set of various products, companies, or industries.
With proper web scraping and feeding of new headlines, a firm would be able to keep track of various topics to make better informed investing decisions.  For example, one could feasibly keep track of terms that are rising rapidly in terms of positive sentiment in order to invest in them.

The data is collected from Kaggle through this [link](https://www.kaggle.com/ankurzing/sentiment-analysis-for-financial-news).  It's a collection of 4,837 unique news headlines from various financial news sources. The headlines are split into three categories:
- __Positive__
- __Neutral__
- __Negative__

An example of a positive headline would be "With the new production plant the company would increase its capacity to meet the expected increase in demand and would improve the use of raw materials and therefore increase the production profitability."


While an example of a negative headline would be "The international electronic industry company Elcoteq has laid off tens of employees from its Tallinn facility ; contrary to earlier layoffs the company contracted the ranks of its office workers , the daily Postimees reported."


It's an interesting challenge that requires quite a bit of data manipulation to get the dataset to feed into a neural network.  By the end of this project, I hope to have a neural network that can not only correctly classify examples from the test set, but also work on a stream of new headlines streamed in from other sources.  

## Text Cleaning and Exploration:


To start, it was necessary to clean the headlines by removing so-called 'stop words' like 'and', 'I', 'or', etc. . . 
This changed the headlines from looking like this. . . 
![Imgur](https://i.imgur.com/nuLcp34.png)
. . . to looking like this:<br>
![Imgur](https://i.imgur.com/CyS96as.png)
Lastly, I used a process called lemmatization to further break down the words into simpler forms.  Lemmatization will change a word like 'Running' into 'run'.  This simplification of the words makes it possible for the neural network later on to treat 'Running', 'run', 'ran', and 'runs' exactly the same, for example.  You lose some nuance in the sentance as you'll soon see, but it makes it much easier for the model to learn in the end.  Here are some headlines after lemmatization:<br>
![Imgur](https://i.imgur.com/6LZ8qtv.png)


## Exploratory Data Analysis:

While exploring the data, I created a wordcloud of the most common words in the series of headlines.  Here is the cloud for the negative headlines:<br>
![Imgur](https://i.imgur.com/8ArewsH.png)
While it may not be at all obvious that this is bad news, that's where the beauty of machine learning comes in.  It's possible for the algorithm to pick up on seemingly harmless words or patterns that may show up more often in negative headlines.

## Neural Network Model:
For my neural network model, I chose to use an embedding layer as my first layer in order to generate word embeddings.  This is a common approach to NLP problems as it groups similar words together.  Another advantage to this is that I was able to use the TensorFlow projector to display the embeddings my model created in three dimensional space.

Here is a projection of the word embeddings my model created from the training headlines:  

![gif_to_show](https://github.com/thomaskbrown18/financial_news_nlp/blob/master/gifs/embed_gif_ii.gif)

As you can see, there is some overlap, but there are two very distinct groups of words!  One set is most commonly associated with positive headlines, while the other is associated with negative headlines.  Neutral headlines will have a healthy mix from both blobs.

## Further Work To Do:

There's still a lot we can do with this modeling.  In the future, I'd like to complete the following analysis:
- A web application that collects and analyzes headlines from various financial news sources.
- Application of different neural network architecture types.
- New types of sentiment analysis, such as breaking news vs unimportant or opinion pieces vs fact.


# Conclusion:





This is currently a work in progress.  Please check back soon.

-TB
