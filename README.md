# NLP Disaster Tweets – Kaggle Mini-Project

This repository contains my mini-project for the **Kaggle "Natural Language Processing with Disaster Tweets"** competition.  
The task is to build an NLP model that predicts whether a tweet refers to a **real disaster**.

## Project Overview
- **Task:** Binary text classification (`disaster` vs `non-disaster`)
- **Dataset:** Kaggle-provided tweets with `text`, `keyword`, and `location`
- **Model:** Bidirectional LSTM with pretrained word embeddings (GloVe)
- **Primary Metric:** F1 score (threshold-tuned)
- **Secondary Metrics:** AUC, Accuracy

## Approach
1. **EDA:** Checked class balance, tweet length distribution, and keyword/location sparsity.
2. **Minimal Cleaning:** Lowercased text; replaced URLs→`<URL>`, mentions→`<USER>`; stripped `#` from hashtags but kept the word; normalized punctuation.
3. **Modeling:** Pretrained GloVe embeddings + Keras Tokenizer; sequences padded to fixed length; Bidirectional LSTM for context from both directions.
4. **Evaluation:** Validation threshold tuned to maximize F1; AUC and Accuracy tracked for diagnostics.

## Results
- **Val F1:** ~0.775 @ threshold 0.369  
- **Val AUC:** ~0.868  
- **Val Accuracy:** ~0.800  

## Repository Structure
- `Disaster_Tweets_Week4_BiLSTM_Report.ipynb` — Main notebook
- `data/` — Dataset (ignored in `.gitignore`)
- `submissions/` — Kaggle submissions (ignored)
- `ssh_keys/` — Local SSH keys (ignored)

## License
MIT License — see [LICENSE](LICENSE)

## Author
Thomas Fey-Grytnes
