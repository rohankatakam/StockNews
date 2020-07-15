# [StockNews](https://github.com/rohankatakam/StockNews/blob/master/StockNews.ipynb)

### Background
I previously experimented with a sentiment/morality lexicon created by researchers at my university by creating a simple [sentiment analyzer](https://github.com/rohankatakam/SentimentAnalyzer/blob/master/sentiment_analyzer.ipynb). I borrowed the core functionality from that project to help me analyze stock news. 

### Core Functionality
The program collects a number of news articles for a given stock ticker, parses each article and derives the positive and negative sentiment percentages. The difference in the mean of the positive and negative percentages of all the articles are taken to find a net sentiment value.


### High Points
I have found that the algorithm, yet simple, is quite effective and produces relatively accurate results when I look at how stocks are performing over time periods (in reality) and comparing this to what my algorithm produces over these respective periods. Further down, I will show you examples of this testing.

### Drawbacks
The running time is quite slow. I am looking into ways how to speed it up, however I don't believe that it is possible to make it much faster. The running time is completely dependent on what your `limit` parameter is in the `getNews()` function. `limit` essentially specifies how many articles you want to include in your calculation. Of course, parsing more articles will take more time. However, gathering more artiucles will produce higher accuracy. When I am calling `getNews()` from other functions, I am setting `limit=5` because I feel that that provides the best balance between speed and accuracy. 


### Future
I plan on integrating NLTK VADER to provide even more accurate results. My goal is to implement this sentiment analysis in a stock trading program eventually.
