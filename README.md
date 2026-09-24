# NLP Topic Modelling of Customer Reviews

A natural language processing project exploring customer reviews to identify key themes, customer emotions, operational issues, and actionable business insights using topic modelling, emotion analysis, and large language models.

## Overview

The objective of this project was to analyse customer reviews and identify recurring themes, sentiment patterns, and key drivers of negative customer experiences.

The analysis combines reviews from **Google and Trustpilot** and applies multiple NLP techniques to uncover patterns within customer feedback.

The project explores:

- Word frequency analysis
- Word cloud visualisation
- Negative review analysis
- Topic modelling with BERTopic
- Emotion classification using BERT
- LLM-assisted topic extraction using Falcon-7B-Instruct
- Topic modelling using Gensim LDA
- Business insights and recommendations

## Dataset

The analysis uses two datasets containing customer reviews from:

- Google
- Trustpilot

The datasets cover a 12-month period and include review text, ratings, and location information.

The data was used to compare customer feedback across platforms and identify recurring issues across different locations.

## Methodology

The analysis followed a structured NLP workflow:

- Data cleaning and preprocessing
- Missing value handling
- Duplicate removal
- Location matching
- Text normalisation
- Stopword removal
- Tokenisation
- Word frequency analysis
- Word cloud visualisation
- Negative review filtering
- Topic modelling
- Emotion classification
- LLM-assisted topic extraction
- Topic interpretation
- Business insight generation

Text preprocessing included converting text to lowercase, removing numbers and punctuation, removing stopwords, and tokenising the reviews using NLTK.

## Exploratory Text Analysis

Word frequency analysis and word clouds were used to identify common terms across the review datasets.

Across the reviews, recurring themes included:

- Equipment
- Staff
- Machines
- People
- Time
- Membership
- Facilities

Negative reviews were analysed separately to focus on the main drivers of customer dissatisfaction.

## Negative Review Analysis

Reviews with ratings below 3 were classified as negative reviews.

The analysis showed recurring issues related to:

- Equipment availability and maintenance
- Staff behaviour and professionalism
- Cleanliness and hygiene
- Overcrowding
- Shower facilities
- Membership and access systems
- WiFi and connectivity
- General gym environment

The analysis also compared Google and Trustpilot reviews to identify platform-specific differences.

Trustpilot reviews showed greater emphasis on membership, billing, and account-related issues, while equipment and staff-related complaints appeared consistently across platforms.

## Topic Modelling with BERTopic

BERTopic was used to identify semantic topics within negative reviews.

The first BERTopic analysis focused on negative reviews from locations common to both Google and Trustpilot, allowing cross-platform comparison.

The model identified topics including:

- Equipment & General Gym Experience
- Shower Facilities & Temperature
- Access & Membership Systems
- Toilets & Cleanliness
- Broken or Poor Equipment
- Staff Behaviour & Professionalism
- WiFi & Connectivity Issues
- Gym Environment & Disruptions
- Overcrowding & Capacity
- General / Informal Complaints

A second BERTopic analysis focused on the **top 30 locations with the highest number of negative reviews**.

This produced a more concentrated set of themes, with equipment, staff, and parking becoming more prominent.

A third BERTopic analysis was then applied specifically to reviews classified as expressing anger.

This helped identify the issues most strongly associated with intense negative experiences.

## Emotion Analysis

A pre-trained BERT-based emotion classification model was used to classify emotions within negative reviews.

The model used was:

`bhadresh-savani/bert-base-uncased-emotion`

The analysis considered emotions including:

- Anger
- Fear
- Sadness
- Joy

**Anger** was the dominant emotion across the negative reviews, followed by sadness.

BERTopic was then applied specifically to reviews classified as expressing anger to identify the main issues associated with strong negative emotions.

## LLM-Assisted Topic Modelling

Falcon-7B-Instruct was used to extract the three main topics from a sample of negative customer reviews.

The extracted topics were then passed into BERTopic to identify broader semantic themes.

Compared with the earlier keyword-based topic modelling approaches, the LLM-assisted approach produced more structured and interpretable themes, including:

- Customer service
- Cleanliness
- Pricing
- Equipment
- Service delivery

The LLM-generated topics were then used as the basis for generating actionable business recommendations.

## Business Insights

The analysis produced five main areas for potential improvement:

### 1. Improve Customer Service and Communication

Enhance staff training and professionalism while improving communication around membership, billing, and policies.

### 2. Upgrade Equipment and Maintain Facilities

Improve equipment maintenance and upgrades while maintaining high standards of cleanliness across toilets, showers, and changing areas.

### 3. Enhance the Overall Gym Experience

Address overcrowding, scheduling flexibility, temperature, noise, and other environmental factors affecting the customer experience.

### 4. Expand and Personalise Offerings

Consider a wider variety of classes, workouts, and personalised fitness plans to better meet different customer needs.

### 5. Simplify Membership and Increase Perceived Value

Improve pricing transparency and consider incentives, rewards, or promotions to improve perceived value and customer retention.

## Topic Modelling with LDA

Gensim's Latent Dirichlet Allocation (LDA) was also applied to the negative reviews.

The model generated **10 topics** based on word co-occurrence.

Key themes included:

- Equipment
- Machines
- Staff
- Service
- Cleaning
- Hygiene
- Membership
- Classes
- Showers
- Overcrowding

The results were visualised using **pyLDAvis**.

Compared with BERTopic, LDA produced broader and less distinct topics, but the main themes remained consistent across both approaches.

## Key Findings

- Equipment problems were one of the most consistent themes across the review datasets.
- Staff-related complaints were also prominent across platforms.
- Overcrowding and general gym experience were recurring concerns.
- Trustpilot reviews showed greater emphasis on membership and administrative issues.
- Negative reviews were strongly associated with anger and sadness.
- BERTopic provided more distinct semantic topic clusters than LDA.
- LLM-assisted topic extraction produced more interpretable and actionable themes.
- Different NLP approaches consistently identified equipment, staff, cleanliness, membership, and overcrowding as important areas of customer dissatisfaction.
- Combining multiple NLP techniques provided a broader understanding of customer feedback than relying on a single modelling approach.

## Technologies & Techniques

### Programming

- Python
- Pandas
- NumPy

### Natural Language Processing

- NLTK
- Tokenisation
- Stopword Removal
- Text Preprocessing
- Word Frequency Analysis
- Word Clouds

### Topic Modelling

- BERTopic
- Gensim
- Latent Dirichlet Allocation (LDA)
- CountVectorizer
- pyLDAvis

### Machine Learning & AI

- BERT
- Falcon-7B-Instruct
- Hugging Face Transformers

### Visualisation

- Matplotlib
- WordCloud
- BERTopic Visualisations
- pyLDAvis

## Project Files

**Notebook:** Contains the complete NLP workflow, including data preprocessing, exploratory text analysis, topic modelling, emotion classification, LLM-assisted topic extraction, LDA modelling, visualisation, and analysis.

**Report:** Provides the written analysis, methodology, topic interpretations, emotion analysis, LLM analysis, business insights, and recommendations.

## Project Structure

```
nlp-topic-modelling-customer-reviews/
│
├── README.md
├── nlp_topic_modelling_customer_reviews.ipynb
└── nlp_topic_modelling_customer_reviews_report.pdf
```

## Author

**Jovan Surya**

Data Science, Machine Learning & AI
