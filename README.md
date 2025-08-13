# NLP Disaster Tweets – KaggleProject

This repository contains my Mini‑project for the **Kaggle "Natural Language Processing with Disaster Tweets"** competition.  
The goal is to build a neural model that predicts whether a short tweet is about a **real disaster** or **not**.

## Project Overview
- **Task:** Binary classification of tweets (`disaster` vs `non-disaster`)
- **Dataset:** Kaggle-provided tweets with `text`, `keyword`, and `location`
- **Model:** Bidirectional LSTM and GRU with learned embeddings
- **Metric:** F1 score (primary), AUC and Accuracy for diagnostics

## Key Steps
1. **EDA:** Class balance, tweet lengths, feature sparsity.
2. **Minimal cleaning:** lowercase; replace URLs→`<URL>`, mentions→`<USER>`; keep hashtag words; normalize punctuation.
3. **Modeling:** Neural-only pipeline; tokenization/padding inside the model.
4. **Evaluation:** Tune threshold on validation to maximize F1.

## Results (Sanity Run)
- **Val F1:** ~0.775 @ threshold 0.369  
- **Val AUC:** ~0.868  
- **Val Accuracy:** ~0.800  

## Structure
- `Disaster_Tweets_Week4_BiLSTM_Report.ipynb` — Main notebook
- `data/` — Dataset (ignored in `.gitignore`)
- `submissions/` — Kaggle submissions (ignored)
- `ssh_keys/` — Local SSH keys (ignored)

## License
MIT License — see [LICENSE](LICENSE).

## Author
Thomas Fey-Grytnes
