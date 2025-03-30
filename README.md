# 📌 GRASP: Graph-Based Hybrid Recommender Analyzing Sentiment Patterns

Welcome to **GRASP**, an advanced recommendation system designed to deliver highly personalized and precise item suggestions for **Rent the Runway (RTR)**. Utilizing state-of-the-art deep learning methodologies, GRASP enhances customer satisfaction by accurately predicting user preferences through collaborative filtering, content-based filtering, and sentiment analysis. 🚀

---

## 🌟 Detailed Overview

GRASP integrates three sophisticated deep learning techniques:

- **Neural Graph Collaborative Filtering (NGCF)**: Employs Graph Neural Networks (GNNs) to model intricate user-item interaction patterns, capturing both direct relationships and multi-hop interactions. This method effectively maps user preferences and item features into an embedding space, facilitating nuanced recommendations.

- **Content-Based Recommendations**: Utilizes TF-IDF (Term Frequency-Inverse Document Frequency) vectorization to numerically represent item attributes and efficiently compute similarity scores. Integrated with **Spotify’s Annoy Index** for rapid and scalable similarity search, this method ensures fast, accurate recommendations based on content characteristics.

- **Sentiment Analysis using BERT (Bidirectional Encoder Representations from Transformers)**: Incorporates a fine-tuned transformer-based model, **BERT**, to perform deep sentiment classification on user-generated reviews. Enhanced by keyword extraction, this technique accurately identifies nuanced customer feedback, enabling more refined recommendations.

---

## 📚 In-Depth Technical Breakdown

### 🧠 Neural Graph Collaborative Filtering (NGCF)

- Implements advanced GNN architectures to propagate user-item interaction signals through graph structures.
- Uses multiple layers of **message passing** to encode higher-order relationships into user and item embeddings.
- Employs **LeakyReLU activations** and **dropout regularization** to enhance learning efficiency and prevent overfitting.

### 📝 Content-Based Filtering

- **TF-IDF vectorization** captures textual and categorical item data, converting complex product descriptions into structured numerical formats.
- Spotify’s Annoy Index leverages approximate nearest neighbor search algorithms, significantly improving search speed and scalability over traditional methods.
- Adjusts hyperparameters, including the number of trees in the Annoy Index, to optimize performance trade-offs between speed and recommendation accuracy.

### 🗣️ Sentiment Analysis with BERT

- Fine-tunes pre-trained BERT model specifically for sentiment classification tasks on RTR customer reviews.
- Implements keyword-weighted sentiment scoring to enhance prediction precision, addressing potential sentiment ambiguities.
- Incorporates **sentiment scores** into hybrid recommendations to reflect user feedback directly in recommendation rankings.

---

## ⚖️ Hybrid Recommendation Model

- Combines NGCF (**weighted at 65%**) and content-based recommendations (**weighted at 35%**) into a unified scoring mechanism.
- Effectively addresses **cold-start problems** by providing content-based fallback recommendations for users or items lacking sufficient interaction data.
- Dynamically adapts recommendation weights based on real-time feedback, refining future predictions.

---

## 📊 Comprehensive Performance Metrics

| Metric                            | Result  |
|-----------------------------------|---------|
| Root Mean Squared Error (RMSE)    | 1.50    |
| Mean Absolute Error (MAE)         | 1.24    |
| Net Promoter Score (NPS)          | 42.7    |
| Customer Satisfaction Score (CSAT)| 71.6%   |

---

## 🔮 Interactive Insightful Analytics

Interactive **WordCloud** visualizations effectively highlight prevalent feedback themes, such as fitting accuracy and garment quality, enabling actionable insights to significantly refine recommendation strategies.
```
