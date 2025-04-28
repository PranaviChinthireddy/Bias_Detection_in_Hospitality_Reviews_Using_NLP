# Bias Detection in Hospitality Reviews Using NLP

# Overview
This project focuses on detecting potential bias, discrimination, and unfair treatment within hospitality reviews (such as those for hotels, restaurants, and spas) using Natural Language Processing (NLP) techniques. Analyzing customer reviews' sentiment and identifying specific biased or discriminatory terms aims to uncover patterns of unfairness in customer experiences that could impact access, knowledge, or reputation. This project leverages various text analysis techniques, including sentiment analysis, n-gram and TF-IDF analysis, and topic modeling, to detect bias signals and uncover trends across different cities and business types.

# Objective
The primary goal of this project is to develop a framework that detects signs of bias, unfairness, or systemic issues in hospitality reviews. The task includes:

Identifying biased or discriminatory terms within customer feedback.

Analyzing sentiment to understand the nature of bias in the reviews.

Using text analysis techniques to uncover recurring themes or topics related to bias or unfair treatment.

Presenting actionable insights to help improve fairness in the hospitality sector.

# Approach
# 1. Data Collection and Preprocessing
The dataset includes Yelp's open-source hospitality reviews. Data from businesses categorized as "hotels," "restaurants," "spas," and others were extracted using keyword-based filtering, focusing on high-volume cities such as Philadelphia, Tucson, Tampa, and others. Reviews were filtered for low-star ratings (1-3 stars) and preprocessed by:

- Merging business and review data.

- Removing missing values.

- Normalizing the text for further analysis.

# 2. Bias Detection
A custom list of bias-related keywords was defined, and reviews were flagged based on the occurrence of these keywords combined with sentiment analysis. The keywords were carefully chosen based on research rather than assumptions, ensuring a data-driven approach to bias detection. These keywords included terms related to unfair treatment, such as "rude," "disrespectful," and "unwelcoming."

# 3. Text Analysis Techniques
N-Grams and TF-IDF Analysis: These techniques were used to analyze common phrases and terms in biased reviews. N-grams (bi-grams and tri-grams) helped identify recurring patterns in customer complaints, while TF-IDF identified the most critical terms in the context of biased reviews.

Sentiment Analysis: Sentiment polarity scores were computed using TextBlob to classify reviews as positive, neutral, or negative. Negative sentiment reviews were further analyzed for bias indicators.

BERTopic: A transformer-based topic modeling approach was employed to uncover hidden topics within reviews. This helped in detecting potential themes related to unfair treatment and systemic bias.

# 4. Word Cloud for Negative Reviews
A word cloud was generated to visualize the most frequent terms appearing in negative reviews, particularly those flagged for bias. This helped in identifying key themes in customer complaints related to unfair experiences.

# 5. Visualizations and Insights
Multiple visualizations were created to provide insights into bias distribution across various business types and cities. Some key visualizations include:

Bias Rate Comparison: Comparing the bias rate between major hotel chains and other businesses.

City-wise Bias Rate: Analyzing the bias rate for major hotel chains across different cities.

Bias Rate by Business Type: A heatmap showing the business type and city bias rate.

Flagged Reviews per Major Hotel Chain: A bar plot showing the number of flagged reviews per major hotel chain.

Bias Density per 1000 Reviews: Showing the bias density across cities for major hotel chains.

# 6. Automation Pipeline
An automation pipeline was developed to flag biased reviews based on predefined keywords and sentiment analysis. The pipeline assigns a bias risk score based on the sentiment and star rating of the review, categorizing them into high, medium, or low risk.

# Technologies Used
Python: The primary programming language.

Libraries: Pandas, Matplotlib, Seaborn, NLTK, TextBlob, BERTopic, Scikit-learn.

Jupyter Notebooks: For data analysis and visualization.

# Key Insights
Bias Detection: The project successfully flagged reviews containing bias-related keywords and identified significant differences in bias rates across major hotel chains and other businesses.

Sentiment Analysis: Negative sentiment in reviews was strongly correlated with bias flags, revealing that customers with negative experiences often mention bias or unfair treatment.

Business Type and City Variations: The analysis highlighted variations in bias rates across different cities and types of hospitality businesses, which could inform future strategies for improving customer experiences in those areas.

# Future Work and Enhancements
Improved Bias Detection: Further enhancement of the bias keyword list by including more diverse and contextual terms, possibly using advanced techniques like Named Entity Recognition (NER) to capture bias at a deeper level.

Ethical Considerations: It is essential to continually refine the bias detection methodology, ensuring that data does not stereotype back assumptions about bias.

Automation and Real-Time Monitoring: Building a real-time bias detection system using NLP models, which can automatically flag and analyze reviews as they come in.

Expansion of Analysis: The analysis will cover more cities, business categories, and a larger dataset, including international hospitality businesses.

# Conclusion
This project provides a practical framework for detecting bias and unfair treatment in hospitality reviews, with the potential to be expanded and refined further. By combining traditional text analysis methods with state-of-the-art NLP models, the framework offers a practical approach to addressing systemic bias in customer feedback and contributing to the broader mission of creating fairer experiences in the hospitality industry.

## Dataset

- Source: [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/)
- Cities Analyzed: Philadelphia, Tucson, Tampa, Indianapolis, New Orleans, Edmonton
- Hospitality Reviews Processed: \~2.3M
