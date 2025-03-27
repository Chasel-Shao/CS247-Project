# 🎬 CS247 Project — Movie Recommendation System Using Transformers

Final project for **UCLA CS247: Advanced Data Mining**  

This project explores how to enhance transformer-based movie recommendation models using the MovieLens-1M dataset. We extend the BERT4Rec architecture with user profile embeddings, clustering, and hybrid collaborative filtering.

---

## 📁 Project Structure

```
.  
├── ml-1m/                                      # MovieLens-1M dataset  
├── BERT4Rec-vanilla.ipynb                      # Baseline BERT4Rec model  
├── BERT4Rec-V2.ipynb                           # Enhanced model with embedding and tuning  
├── BERT4Rec-UP-V2.ipynb                        # Model with User Profile Embeddings  
├── BERT4Rec-Compare.ipynb                      # Notebook for model comparison  
├── BERT4Rec_vanilla_time.ipynb                 # Adds time-based features to vanilla BERT4Rec  
├── CF.ipynb                                    # Collaborative Filtering baseline  
├── HybridModel_cf_bert.ipynb                   # Hybrid CF + Transformer model  
├── Ratings_Embeddings_Subset_Model.ipynb       # Embedding subset experiments  
├── Transformer Baseline & Title Word Embedding.ipynb  # Title word embedding  
├── COM_SCI_247_Final_Project_Proposal_.pdf     # Project write-up  
├── README.md                                   # This file  
├── .gitignore
```

---

## 🚀 How to Run

### 1. Clone the repo

```bash
git clone https://github.com/Chasel-Shao/CS247-Project.git
cd CS247-Project
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing:

```bash
pip install transformers pandas numpy torch scikit-learn matplotlib surprise tqdm
```

### 3. Run Notebooks

Recommended order:

- `BERT4Rec-vanilla.ipynb`  
- `BERT4Rec-V2.ipynb`  
- `BERT4Rec-UP-V2.ipynb`  
- `HybridModel_cf_bert.ipynb`  
- `BERT4Rec-Compare.ipynb`  

---

## ✨ Features

- Transformer-based sequential recommendation (BERT4Rec)
- User-aware modeling:
  - User profile embeddings (age, gender, occupation)
  - User activity-level encoding (recency, frequency)
  - User clustering with K-Means
- Hybrid recommender: Collaborative Filtering + Transformer
- Evaluation metrics:
  - Recall@10
  - NDCG@10

---

## 📊 Results (MovieLens-1M)

| Model               | Recall@10  | NDCG@10    |
| ------------------- | ---------- | ---------- |
| BERT4Rec (Baseline) | **0.9941** | 0.6467     |
| BERT4Rec-UP         | 0.9376     | **0.9376** |
| BERT4Rec-UPC        | 0.9428     | 0.9428     |
| BERT4Rec-UPCA       | 0.9452     | 0.9452     |

> - **UP**: User Profile embedding  
> - **UPC**: + K-Means Clustering  
> - **UPCA**: + User Activity features  

---

## 📚 References

- BERT4Rec: Sequential Recommendation with Bidirectional Encoder Representations (SIGIR 2019)
- MovieLens 1M Dataset
- COM SCI 247 Final Project Report

---

_Project submitted for CS247 Advanced Data Mining — Winter 2025, UCLA_
