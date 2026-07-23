# Project Plan — Detecting AI-Generated Text

**Team:** Aditi & Victoria
**Course:** SEA 820 — NLP Final Project

## Goal
Build, evaluate, and compare a classic ML baseline and a fine-tuned Transformer
for classifying text as human-written (0) vs. AI-generated (1) on the Kaggle
*AI vs. Human Text* dataset.

## Timeline & ownership

### Week 1 — Foundations & baseline
- [x] Repo + Colab setup, shared dataset access — *Aditi*
- [x] Exploratory data analysis (`01_eda.ipynb`): class balance, length, quality
      filters, vocabulary — *Aditi*
- [x] Classic baseline (`02_baseline_tfidf.ipynb`): TF-IDF + Logistic Regression,
      Naive Bayes, Linear SVM; full metrics — *Victoria*
- [ ] This project plan — *both*

### Week 2 — Transformer
- [x] Tokenization + `datasets` pipeline on the shared split — *Victoria*
- [x] Fine-tune DistilBERT with `Trainer`; log ≥2 hyperparameter configs — *Victoria*
- [ ] Baseline-vs-Transformer comparison table — *both*

### Week 3 — Analysis, report, presentation
- [ ] Error analysis: inspect false positives / negatives, form hypotheses — *both*
- [ ] Ethical discussion (bias against non-native writers, dataset artifacts) — *Aditi*
- [ ] Final report (PDF) — *both*
- [ ] Presentation slides (5–7 min, PDF) — *both*
- [x] Code cleanup, README, reproducibility check — *Victoria*

## Design decisions (from EDA)
- Report precision / recall / F1 (not just accuracy) due to ~63/37 imbalance.
- Stratified 80/20 split, `random_state=42`, reused across all notebooks.
- Remove texts < 20 words (junk, all AI) and exact duplicates.
- Watch for dataset artifacts (anonymisation tokens) that leak the label.

## Deliverables
Source code (GitHub) · Final report (PDF) · Presentation slides (PDF).
