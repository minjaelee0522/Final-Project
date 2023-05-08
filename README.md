# Sentiment Analysis of Amazon’s deteriorated Product Ratings

## Introduction

Sentiment Analysis, also known as opinion mining is a sub of Natural Language Processing that helps businesses to understand the brand and product sentiments of a consumer. It helps enterprises to gauge customers’ opinions through analysis of reviews, blogs, social media, news, etc. to conduct market research and predict the market trends to cater products accordingly. Sentiment-bearing phrases are identified from broken down texts collected through different sources and a sentiment score is assigned. In more sophisticated models, multiple layer scores are combined for analysis. For this project, I have performed a sentiment analysis of amazon’s beauty product that dropped its rating from 2014 to 2021. A starter data set containing product features including ratings and reviews from 2014 is used for comparison with newly scraped reviews and ratings of the same product. The project is divided into four parts. Data Scraping, Data Cleaning, Exploratory Data Analysis, and Sentiment Analysis. This is unsupervised Machine Learning as there is no target variable.

## Data Scraping

The first step was data collection. The majority of time on this project was spent cleaning and scraping data. Raw text data for amazon’s beauty products containing 9 features and 12101 unique asins was downloaded from the UCSD repository which is shared with the public for research purposes. Fig 1 shows the 9 features downloaded from the repository. The unique asin numbers were put on a list for future scrapping using selenium and beautiful soup. 7 features were extracted from 2021 of 4242 unique asins for the products that are still available in 2021.

## Data Cleaning

The two datasets were merged on unique asin numbers. Unwanted columns were removed and 12 features were retained for analysis. The dataset was stored in pandas data frame and data cleaning was done using regular expression and nltk libraries. nltk is a text preprocessing library that is frequently used in NLP. The reviews from 2014 and 2021 were prepared for further analysis by converting all texts to lower case, formatting empty space, expanding contractions (eg mgmt. to management), filtering punctuation and stop words (like have, has), and finally lemmatization (the process of extracting root words, eg. better: lemma good). 12 features were used for further analysis.

## Exploratory Data Analysis

The old and scraped data was visualized for any trend in buying habits within each category. Plot 1 shows the top 10 categories in terms of count within the given dataset of amazon’s beauty products. It can be seen that most products are listed within skincare, haircare and makeup categories. The product features from these 3 groups are separated for further exploratory analysis.It can be seen that hair products have the highest range of prices.

### Skincare Products:

Skincare products comprises the majority of amazon’s beauty and health product within the dataset. For this project, number of product ratings is considered an estimation of number of sales. The distribution of number of products within each price range and its microscopic view showing the number of ratings (which in turn is an estimate of number of sales) for each price range in skincare products were plotted. It can be seen that maximum products are listed between $10–$20 and that’s about the range which attracts highest number of customers.

### Haircare Products:

Haircare products are the second-highest number after skincare products from this dataset. It was seen that customers usually spend more money online on hair products than skincare or makeup products. On the contrary, there is comparatively lesser number of products listed in the range of $30-$50, and based on the given buying pattern, more products in this range can be listed.

### Makeup Products:

Makeup products are the third-largest number sold in beauty and health category from the dataset. There is a trend of people spending the least on makeup products. Most products are listed in the range of $0–10 and also the maximum reviews (sales) is seen in the same range.

The difference of rating for each product in the three groups from 2014–2021 was calculated and top 10 products with highest drop were analyzed.The top 10 products in each categry with the highest drop were plotted. The sentiment analysis for these products will be done to understand the trend and change in opinion for each of these product categories.

## Sentiment Analysis

Since the sentiment analysis was done on the deteriorated product ratings, the polarity was assumed to be negative. Word cloud and N-gram was used for Natural Language Processing. For this project, the reviews of all 10 products in each category were concatenated to observe if anything stood out. Ideally, comparison of word cloud for each brand should be done to understand the sentiment towards the brand but since the number of reviews scraped for each product was between five to eight, all reviews were concatenated for a better understanding.

## Findings and Recommendations

### Skincare Products:
For skincare category of amazon’s beauty products,

1. There are more reviews with words like can not, not really, not work, not know in 2021 compared to 2014 implying quality of products have gone down
2. The phrase side effects has been used frequently in 2021 and from sellers’ point of view, contents of the product can be reevaluated for any side effect causing factor
3. Words like soft, smooth were more frequent in 2014 but hard, dry is seen more in 2021, change in ingredients could be tracked
4. not really was used frequently in 2014 too indicating sign of complaints in 2014 and could be inspected back then
5. word cloud for reviews each of the 10 products can give a much better picture about how the sentiment of customers changed over 6 year

### Haircare Products:
For haircare products,

1. Phrases like can not, not work, not really have increased in the reviews of 2021
2. shampoo conditioner 2 in 1 appears frequently which could be possible reason for reduced quality
3. Word related to smell like coconut smell appears in 2014 reviews and old smell in 2021. This can be further analyzed
4. spray nozzle appears a lot in 2021 and not in 2014, which could be a possible trend
5. kid hair, tear free appeared more frequently in 2014, implying possible change in ingredients by 2021

### Makup Products:
For makeup products,

1. not work, would not are the most appeared phrases in 2021 reviews implying drop in popularity from 2014
2. Lot of discussion around the word color, like hot pink, purple lipstick, black lipstick in 2021 compared to just pink in 2014 implying possible change in taste
3. 100% Pure has been used a lot in 2021, which could be possible concern about ingredients in the product


## Conclusion and Future Work

Sentiment Analysis can be used in e-commerce industry to understand the trend and improve brand value. In this project word cloud was used to analyze the changing trend and figure out customer concerns through reviews. This work can be further extended by scraping more reviews for each product and studying the changing sentiment and factors effecting the drop in popularity of each product.

