# Bias Detection in Hospitality Reviews Using NLP

## Problem Statement

Customer reviews are rich with feedback — not just about quality, but also fairness. In the hospitality sector, where interpersonal experiences are central, reviews can reveal systemic patterns of unfair treatment, exclusion, or biased service. This project analyzes hospitality reviews from Yelp to uncover signals of bias, using keyword detection, sentiment scoring, and risk classification.


## Objective

To analyze hospitality reviews and identify potential signs of unfair treatment or biased behavior based on linguistic cues and sentiment mismatches. The focus is on:

- Reviews from restaurants, hotels, and spas
- Specific interest in major hotel chains (e.g., Hilton, Marriott)
- Fairness indicators in language (e.g., “rude”, “disrespectful”, “ignored”)


## Process Overview

1. **Filtered Yelp’s business data** for hospitality-related categories in selected cities.
2. **Extracted reviews** for those businesses and flagged texts with fairness-related keywords.
3. **Scored sentiment polarity** using TextBlob and aligned it with star ratings.
4. **Tagged reviews with risk levels** based on low ratings and negative language.
5. **Compared bias signals** across cities, business types, and major hotel chains.
6. **Visualized insights** through heatmaps, bar plots, and word clouds.
7. **Prototyped an automation function** for detecting bias risks in real-time review feeds.
8. **Saved output artifacts** including figures and a CSV of flagged major chain reviews.


## Key Insights

1. **Systemic Behavior by Type:** Restaurants had the highest count of flagged reviews, but hotels and spas showed higher risk levels due to increased negative sentiment.

2. **Major Hotel Chain Analysis:** Several prominent hotel brands showed measurable levels of flagged reviews. A separate analysis of flagged reviews within these brands (e.g., Hilton, Hyatt) was conducted and exported.

3. **Geographic Trends:** Bias rate in major hotel chains varies significantly by city, suggesting localized customer service disparities.

## Sample Visuals

- **Figure 1: Bias Rate by Business Type and Chain** — Visualizes whether flagged reviews are more prevalent in major chains vs. smaller businesses.
- **Figure 2: Heatmap by Business Type and City** — Reveals concentration of flagged reviews by category and city.
- **Figure 3: Flagged Reviews by Major Hotel Chain** — Highlights how often reviews were flagged for bias within individual hotel brands.


## Bonus: Automation Function

A review detection function was created to:

- Identify fairness-related keywords
- Score sentiment
- Tag reviews with "high", "medium", or "low" risk levels

### Sample Output

```json
{
  "bias_flag": true,
  "sentiment_score": -0.3,
  "bias_risk_score": "high"
}
```

This framework supports scalable moderation, flagging reviews for manual review or alerting teams to location-level risks.


## Ethical Reflections

While keyword-based detection is efficient, it may produce false positives. Real-time systems must combine sentiment, context, and human oversight. As fairness standards evolve, this system should be iteratively retrained to reflect societal shifts.


## Technologies Used

- **Python**
- **Pandas, Matplotlib, Seaborn** for analysis and visualization
- **TextBlob** for sentiment scoring
- **Regex/NLP filtering** for bias keyword detection


## Dataset

- Source: [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/)
- Cities Analyzed: Philadelphia, Tucson, Tampa, Indianapolis, New Orleans, Edmonton
- Hospitality Reviews Processed: \~2.3M


## Directory Structure
.
├── Fairness_Review_Analysis.ipynb      # Main analysis notebook
├── figures/                            # Folder for saved graphs
├── flagged_major_chains.csv            # CSV of reviews flagged from major hotel chains
└── README.md                           # This file
```


## Next Steps

- Incorporate Named Entity Recognition (NER) to refine bias categorization.
- Expand to include more cities or international markets.
- Develop a dashboard or alert system for businesses to monitor fairness signals in near real-time.
