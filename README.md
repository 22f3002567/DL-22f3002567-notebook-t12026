# DL GenAI Project - Messy Mashup (Roll: 22f3002567)

## Problem
Noisy music genre classification - 10 genres, 3020 test mashups.
Metric: Macro F1 Score. Target: ≥ 0.80

## Models
| Model | Type | Expected F1 |
|-------|------|-------------|
| XGBoost | Classical ML on MFCCs | ~0.60 |
| CNN (scratch) | Mel-spectrogram CNN | ~0.72 |
| AST fine-tune | HuggingFace Transformer | ~0.85 |

## Strategy
Train/test gap: stems (clean, 44100Hz) vs mashups (noisy, 22050Hz).
Solution: augmentation pipeline - cross-song stem mixing + ESC-50 noise injection.

## W&B Project
Project: `22f3002567-t12026`

## Kaggle Notebook
https://www.kaggle.com/code/siddharthsahu42/dl-22f3002567-notebook-t12026