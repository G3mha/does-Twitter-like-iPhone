# Tweet Sentiment Classifier: iPhone User Sentiment Analysis

![iPhone](https://images.unsplash.com/photo-1510557880182-3d4d3cba35a5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80)

## Overview

This project implements a Naive Bayes classifier to analyze Twitter sentiment regarding iPhones. By automatically categorizing tweets based on their relevance and sentiment, this tool helps understand public opinion and identify tweets that might require marketing attention.

## Features

- Twitter API integration for data collection
- Natural Language Processing for tweet cleaning and preparation
- Naive Bayes classifier implementation with Laplace smoothing
- Multi-category sentiment classification
- Performance testing with randomized training/test splits
- Comprehensive accuracy metrics

## Classification Categories

Tweets are classified into the following categories:

| Code | Category | Description | Example |
|------|----------|-------------|---------|
| 0 | Very Irrelevant | Off-topic or meaningless tweets | Just a hashtag with no content |
| 1 | Irrelevant | Sales promotions, unrelated mentions | "Buy iPhones at discount now!" |
| 2 | Neutral | Jokes, puns, or neutral mentions | "iPhone is like a mini Corsa lol" |
| 3 | Relevant | Indirect comments related to iPhone | "My science teacher spent 30 min talking about his new iPhone" |
| 4 | Very Relevant | Direct opinions, questions, purchase intent | "iPhone 13 will have to wait until I save enough money" |

## Technical Details

### Data Processing Pipeline

1. **Data Collection**: Using Tweepy library to fetch tweets containing the keyword "iPhone"
2. **Text Preprocessing**:
   - URL and username removal
   - Punctuation removal
   - Tokenization
   - Stemming
3. **Classification**: Implementation of a Naive Bayes classifier with Laplace smoothing
4. **Evaluation**: Calculation of accuracy, precision, recall, and confusion matrices

### Implementation Highlights

- Custom tweet cleaning function handling URLs, usernames, and special characters
- Preservation of emojis to maintain sentiment information
- Implementation of the Naive Bayes algorithm from scratch
- Monte Carlo simulation to evaluate classifier stability

## Performance

The classifier achieved approximately 42% accuracy across the five-category classification task. Through Monte Carlo simulation with 100 different training/test splits, we observed:

- Mean accuracy: 42.6%
- Minimum accuracy: 34.4%
- Maximum accuracy: 49.2%
- Standard deviation: 2.4%

Performance varied by category, with "Very Relevant" and "Very Irrelevant" classifications being most reliable.

## Project Structure

```
.
├── README.md
├── tweets_classifier.ipynb     # Main classifier implementation
├── tweets_collector.ipynb      # Twitter data collection script
├── iphone.xlsx                 # Dataset with labeled tweets
└── .gitignore                  # Git ignore file (excludes auth keys)
```

## Limitations & Future Work

The current implementation has some limitations:

- Difficulty handling irony, sarcasm, or double negations
- Moderate performance due to the simple Naive Bayes approach
- Dataset size limitations

Future improvements could include:

- Integration with more advanced NLP techniques like word embeddings
- Implementation of more sophisticated models (LSTM, BERT)
- Expansion to multiple products for comparative analysis
- Real-time monitoring and classification system

## Dependencies

- Python 3.8+
- Pandas
- NumPy
- NLTK
- Tweepy
- Matplotlib

## References

- [Naive Bayes and Text Classification](https://arxiv.org/pdf/1410.5329.pdf) - In-depth explanation
- [A practical explanation of a Naive Bayes Classifier](https://monkeylearn.com/blog/practical-explanation-naive-bayes-classifier/) - Simplified approach
- [3Blue1Brown: Bayes Theorem](https://www.youtube.com/watch?v=HZGCoVF3YvM) - Visual explanation
- [Veritasium: The Bayesian Trap](https://www.youtube.com/watch?v=R13BD8qKeTg) - Conceptual overview

---

## Authors

Developed by Enricco Gemha, Rafael Coca Leventhal, and Marcelo Rabello Barranco.
