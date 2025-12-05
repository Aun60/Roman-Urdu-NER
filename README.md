
# Roman-Urdu Named Entity Recognition (NER)
### A Comparative Study of CRF, mBERT, and XLM-RoBERTa

This repository contains the dataset, training code, inference scripts, and research paper for a comprehensive study on Named Entity Recognition for Roman-Urdu text.
We evaluate and compare three NER models:

CRF (baseline)

mBERT (BERT-base-multilingual-cased)

XLM-RoBERTa (xlm-roberta-base)

This work includes the largest synthetic Roman-Urdu NER dataset to date (5,500 sentences) and is the first systematic comparison of CRF, mBERT, and XLM-R on this language.
---

## ⭐ Key Contributions

-Construction of a 5,500-sentence Roman-Urdu NER training dataset + 300-sentence dev and test sets
-Seven entity categories: PER, LOC, ORG, EVENT, PRODUCT, DATE, MISC
-Extensive evaluation of CRF, mBERT, and XLM-R
-Demonstration that XLM-R achieves the highest F1, while mBERT provides more stable inference on noisy inputs
-Complete research paper (PDF + DOCX)

Interactive NER inference script for real-time testing
---

## 📁 Repository Structure

```
Roman-Urdu-NER/
│
├── data/
│   ├── roman_train_5500.csv
│   ├── roman_dev_300.csv
│   ├── roman_test_300.csv
│
├── models/
│   ├── crf_model.joblib
│   ├── mbert_model/
│   ├── xlmr_model/
│
├── notebooks/
│   ├── Roman_Urdu_NER_Experiments.ipynb
│
├── paper/
│   ├── Roman_Urdu_NER_Paper.pdf
│   ├── Roman_Urdu_NER_Paper.docx
│
└── README.md

```

---

## 📚 Dataset Overview

| Entity Type | Description |
|-------------|-------------|
| PER | Person names |
| LOC | Locations |
| ORG | Organizations |
| EVENT | Events & occasions |
| PRODUCT | Products & branded items |
| DATE | Dates |
| MISC | Miscellaneous |

The dataset includes intentional noise to simulate real conversational Roman-Urdu:
-casing variation
-typos and spelling drift
-mixed Urdu–English phrasing
-multi-token entities
-irregular spacing

---

## 🚀 Models & Results

### **CRF Baseline**
- F1 (Weighted): 0.84
-Performs well with PER and LOC, struggles with ORG and EVENT

### **mBERT**
(4 Epochs)
-DEV F1: 0.865
-TEST F1: 0.871

### **XLM-RoBERTa**
(4 Epochs — Best Model)
-DEV F1: 0.929
-TEST F1: 0.919

Strengths:

Highest overall precision + recall

Best on multi-token entities and rare words
---

## 🧠 Why XLM-R Outperforms mBERT (Quantitatively)

-Larger multilingual vocabulary

-Better subword segmentation for noisy Roman script

-Stronger cross-lingual representations

Handles multi-token entities more effectively

---

Why mBERT Was Used for Real-Sentence Testing
-
-Even though XLM-R produced the highest F1, qualitative testing revealed:
-mBERT is more stable on noisy, conversational Roman-Urdu
-It handles inconsistent casing and spelling better
-It avoids over-segmentation of Roman tokens
-It is more predictable during interactive inference

Therefore, mBERT was selected for demonstration and deployment-level testing.

## 📄 Research Paper

Full paper is available inside `/paper/`:

- Roman_Urdu_NER_Paper.pdf  
- Roman_Urdu_NER_Paper.docx  

Contains:
- Dataset design  
- Experimental results  
- Multi-epoch XLM-R analysis  
- Discussion & conclusion  

---

## 👤 Author

- **Aun Ali Kazi** 

---

## 📬 Contact  
Open an issue or pull request for improvements or extensions.
