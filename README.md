# Sentiment Analysis with BERT Fine-Tuning

Fine-tuned DistilBERT for 3-class sentiment classification (positive / neutral / negative).

## Results

| Model | Accuracy |
| :--- | :--- |
| Baseline (TF-IDF + Logistic Regression) | 64% 
| **Fine-tuned BERT (This Project)** | **64%** |

**Training:** 2000 samples, 2 Epochs
**Eval Loss:** 0.84

## What I Learned
- Model improves from 51% (Epoch 1) to 64% (Epoch 2), loss decreases from 1.00 to 0.80
- Model is confident on clear positive examples (e.g. "I love this movie" -> positive, 76%)
- Model confuses neutral vs negative on ambiguous text (e.g. "It was okay" -> predicted negative with only 49% confidence)
- This shows more data and more epochs are needed for neutral class.

## How to Run
1. Open `Sentiment-finetune.ipynb`
2. Run all cells
3. Test with your own sentence using pipeline

## Files
- `Sentiment-baseline.ipynb` - Baseline model
- `Sentiment-finetune.ipynb` - BERT Fine-tuning
