
# Roman-Urdu Named Entity Recognition (NER)
### A Comparative Study of CRF, mBERT, and XLM-RoBERTa

This repository contains the dataset, code, and research paper for our study on **Named Entity Recognition for Roman-Urdu text**, comparing:

- **CRF (baseline model)**
- **mBERT (BERT-base-multilingual-cased)**
- **XLM-RoBERTa (xlm-roberta-base)** with multi-epoch evaluation (3, 5, 10)

This is the **first documented comparative analysis** on Roman-Urdu NER using these three models.

---

## ⭐ Key Contributions

- Creation of a **2,000-sentence Roman-Urdu NER dataset**
- Seven annotated entity categories: `PER`, `LOC`, `ORG`, `EVENT`, `PRODUCT`, `DATE`, `MISC`
- Evaluation of CRF, mBERT, and XLM-R
- Detailed multi-epoch experiments for XLM-R showing **overfitting beyond 3 epochs**
- Full research paper included (DOCX + PDF)

---

## 📁 Repository Structure

```
Roman-Urdu-NER/
│
├── data/
│   ├── train.csv
│   ├── dev.csv
│   ├── test.csv
│
├── notebooks/
│   ├── Roman_Urdu_NER_Experiments.ipynb
│
├── paper/
│   ├── Roman_Urdu_NER_Paper.docx
│   ├── Roman_Urdu_NER_Paper.pdf
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

Dataset includes structured noise:
- casing variations  
- typos  
- distractor tokens  
- multi-token entities  

---

## 🚀 Models & Results

### **CRF Baseline**
- F1 Score: **0.88**

### **mBERT**
- F1 Score: **0.9525**  
- Best overall model

### **XLM-RoBERTa**
Epoch | F1 Score | Notes  
------|----------|-------  
3 | 0.9496 | Optimal before overfitting  
5 | 0.9532 | Minor improvement  
10 | 0.9534 | Marginal, signs of overfitting  

---

## 🧠 Why mBERT Outperforms XLM-R

- Roman script aligns better with mBERT’s English-heavy vocabulary  
- Dataset is too small for XLM-R’s 550M parameters  
- XLM-R over-segmented Roman tokens  
- mBERT generalizes better on low-resource Roman-Urdu  

---

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
