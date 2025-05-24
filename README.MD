# Gojek App Review Sentiment Analysis

![Gojek Logo](https://lelogama.go-jek.com/prime/upload/image/gojek-horizontal-logo.svg)

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://gojeksentimentanalyze.streamlit.app/)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview

This project performs sentiment analysis on Gojek app reviews to categorize them as positive, neutral, or negative. The analysis helps understand customer satisfaction, identify pain points, and monitor the app's reception over time.

🔗 **Live Demo**: [Gojek Sentiment Analysis App](https://gojeksentimentanalyze.streamlit.app/)

## 🎯 Features

- **Preprocessing**: Robust text cleaning pipeline for Indonesian language
- **Sentiment Classification**: Multiple models to categorize reviews as positive, neutral, or negative
- **Interactive Dashboard**: Visualize sentiment distribution and insightful metrics
- **Real-time Prediction**: Enter any review text to get instant sentiment prediction
- **Performance Comparison**: Compare different machine learning and deep learning models

## 🧠 Models Implemented

The project compares the performance of several machine learning and deep learning models:

### Traditional Machine Learning Models

1. **Naive Bayes with TF-IDF** - Fast model using probabilistic classification
2. **Linear SVM with TF-IDF** - High-performance model for text classification
3. **Random Forest with FastText** - Ensemble model using word embeddings

### Deep Learning Models

4. **Bidirectional LSTM with FastText Embeddings** - Advanced neural network architecture for capturing context in both directions

## 📊 Model Performance

| Model                    | Accuracy | Precision | Recall | F1 Score |
| ------------------------ | -------- | --------- | ------ | -------- |
| Naive Bayes (TF-IDF)     | ~85%     | ~84%      | ~85%   | ~84%     |
| Linear SVM (TF-IDF)      | ~89%     | ~89%      | ~89%   | ~89%     |
| Random Forest (FastText) | ~86%     | ~86%      | ~86%   | ~86%     |
| BiLSTM (FastText)        | ~90%     | ~90%      | ~90%   | ~90%     |

_Note: Exact metrics may vary slightly with different random seeds or data splits._

## 📋 Data Processing Pipeline

The project implements a comprehensive data processing pipeline for Indonesian text reviews:

1. **Text Cleaning**: Remove URLs, emojis, punctuation, and numbers
2. **Normalization**: Convert informal Indonesian words to their standard form
3. **Tokenization**: Split text into individual words
4. **Stopword Removal**: Remove common Indonesian words that don't add meaningful context
5. **Stemming**: Reduce words to their root form using Sastrawi (Indonesian stemmer)

## 🔍 Feature Engineering

Three different feature extraction methods were explored:

1. **TF-IDF Vectorization**: Capturing importance of terms relative to the corpus
2. **Bag of Words**: Simple term frequency representation
3. **FastText Word Embeddings**: Dense vector representations trained on Indonesian text

## 📈 Key Visualizations

The project includes several insightful visualizations:

- Sentiment distribution across reviews
- Rating distribution and its relationship with sentiment
- Word clouds for positive, neutral, and negative reviews
- Top words by sentiment category
- Review length distribution by sentiment
- Sentiment trends over time

## 🚀 Getting Started

### Prerequisites

```bash
python -m pip install -r requirements.txt
```

### Running Locally

1. Clone this repository
2. Install dependencies from `requirements.txt`
3. Run the Streamlit app:

```bash
streamlit run app.py
```

## 🗂️ Project Structure

```
├── app.py                # Streamlit application
├── main.ipynb            # Main model training and evaluation notebook
├── preprocessing_dataset.ipynb  # Data preprocessing notebook
├── requirements.txt      # Project dependencies
├── data/
│   ├── GojekAppReview_1.csv           # Raw dataset
│   └── GojekAppReview_Processed.csv   # Processed dataset
└── models/
    ├── svm_tfidf_model.pkl    # Trained SVM model
    ├── tfidf_vectorizer.pkl   # TF-IDF vectorizer
    ├── bilstm_model.keras     # Deep learning model
    ├── tokenizer.pkl          # Text tokenizer
    └── label_encoder.pkl      # Label encoder
```

## 📊 Insights and Findings

### Word Usage by Sentiment

- **Positive reviews** frequently contain words related to convenience, service quality, and appreciation
- **Neutral reviews** often discuss functionality without strong opinions
- **Negative reviews** commonly mention issues with technical problems, pricing, or customer service responsiveness

### Rating vs. Sentiment Correlation

- Reviews with 4-5 stars strongly correlate with positive sentiment
- 3-star reviews typically express neutral sentiment
- 1-2 star reviews overwhelmingly contain negative sentiment
- Some exceptions exist where high ratings contain negative text feedback or vice versa

### Text Length Analysis

- Negative reviews tend to be longer as users explain their issues in detail
- Positive reviews are often shorter, expressing satisfaction concisely
- Length distributions provide insight into how different sentiment groups express their opinions

## 🔮 Future Work

- Implement aspect-based sentiment analysis to identify specific features mentioned in reviews
- Incorporate time series analysis to track sentiment trends over app version updates
- Add multi-language support for reviews in languages other than Indonesian
- Deploy a feedback loop system that can automatically categorize and prioritize issues for the development team

## 📚 Resources

- [FastText Pre-trained Indonesian Word Vectors](https://fasttext.cc/docs/en/crawl-vectors.html)
- [Sastrawi Indonesian Stemming Library](https://github.com/sastrawi/sastrawi)
- [NLTK Documentation](https://www.nltk.org/)
- [Streamlit Documentation](https://docs.streamlit.io/)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- [Gojek](https://www.gojek.com/) for their innovative super app platform
- [Streamlit](https://streamlit.io/) for the excellent web application framework
- All contributors to the open-source libraries used in this project
