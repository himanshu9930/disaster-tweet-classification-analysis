# 🌪️ Disaster Tweet Classification using NLP & BERT

This project tackles the real-world challenge of distinguishing disaster-related tweets from irrelevant content during emergencies. It was developed as part of the **MGMT 590 – Machine Learning** course at Purdue University.

## 📍 Project Goal

To build an effective Natural Language Processing (NLP) pipeline capable of classifying tweets as disaster-related or not, using state-of-the-art deep learning techniques. The best-performing model achieved an **F1 score of 0.844** and ranked **22nd on the Kaggle leaderboard**.

## 📊 Dataset

- Source: [Kaggle - Real or Not? NLP with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started)
- Contains 10,000+ tweets labeled as `1` (disaster) or `0` (non-disaster)
- No significant class imbalance detected

## 🔍 Key Techniques

### 🧪 Exploratory Data Analysis
- Disaster tweets contain slightly more words on average
- Clear difference in vocabulary between classes
- No need for resampling due to balanced target variable

### 🛠️ Preprocessing
- Standard NLP steps: lowercasing, tokenization, punctuation & stopword removal
- Multiple embedding strategies evaluated: GloVe + LSTM, BERT, GCN-based embeddings

### 🤖 Models Used
- **GloVe + LSTM** – F1 Score: 0.795
- **GCN Embedding + Classifier** – F1 Score: 0.797
- **BERT (bert-large-uncased)** – F1 Score: **0.844**

> 📌 **Winner**: BERT with bi-directional embeddings and subword tokenization delivered the best performance.

## 🧠 Why BERT?
- Pre-trained contextual understanding
- Bi-directional, non-static embeddings
- Robust performance with fewer epochs
- Best suited for sentence-level classification in short texts like tweets

## ⚙️ Technologies Used

- Python (Transformers, PyTorch, Scikit-learn)
- HuggingFace `transformers` library for BERT
- Pandas, Seaborn, Matplotlib for EDA
- Jupyter Notebooks

## 🚧 Challenges Faced

- BERT’s large model size required significant compute power
- Hyperparameter tuning risked overfitting
- Graph-based embeddings were experimental and harder to tune

## 📈 Final Results

| Model                | F1 Score | Kaggle Rank |
|---------------------|----------|-------------|
| GloVe + LSTM        | 0.795    | –           |
| GCN Embeddings      | 0.797    | –           |
| **BERT (final model)** | **0.844** | **22**        |

## 👥 Contributors

- **Tushar Malankar**  
- **Himanshu Sharma**

## 📬 Contact

Feel free to connect for collaboration or discussion:

- ✉️ [tmalanka@purdue.edu](mailto:tmalanka@purdue.edu)
- 🔗 [LinkedIn – Tushar Malankar](https://www.linkedin.com/in/tushar-malankar)

