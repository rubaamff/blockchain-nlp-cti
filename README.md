# Blockchain-NLP-CTI

### BERT–spaCy Hybrid NLP and Blockchain-Enhanced Adaptive CTI for IOC Extraction and Threat Prediction

**Authors:**  
Shailendra Mishra, Ruba Ahmed Alfahidah, Fayez Al Harbi  
Majmaah University, Saudi Arabia  

---

### 📘 Overview

This repository implements a **hybrid Cyber Threat Intelligence (CTI)** framework that integrates:
- **Natural Language Processing (BERT + spaCy)** for IOC extraction  
- **Machine Learning** for adaptive classification  
- **Blockchain-inspired immutable ledger** for tamper-proof intelligence sharing  

The system achieves **95% accuracy**, **95.7% F1-score**, and **55% latency reduction** (120 ms → 54 ms for 200 reports).  
It is validated on **CIC-IDS2017** and **UNSW-NB15** datasets, with a **Cross-Dataset Robustness Index (CRI)** of 0.999.

---

### 🧩 Key Components
| Component | Description |
|------------|-------------|
| NLP (BERT + spaCy) | Extracts IOCs such as IPs, domains, malware names |
| ML Classifier | Confidence-weighted ensemble (Naïve Bayes, LSTM, BERT) |
| Blockchain Ledger | SHA-256 immutable chain for verified CTI logging |
| Adaptive Learning | Continuously retrains models with new threat data |
| Similarity Detector | Uses TF-IDF + cosine similarity for report clustering |

---

### ⚙️ Installation

```bash
git clone https://github.com/rubaamff/blockchain-nlp-cti.git
cd blockchain-nlp-cti
pip install -r requirements.txt
```

---

### ▶️ Running the Framework

```bash
python main.py
```

---

### 📊 Results Summary

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|-----------|------------|---------|-----------|
| BERT | 0.95 | 0.97 | 0.95 | 0.957 |
| LSTM | 0.90 | 0.96 | 0.90 | 0.921 |
| SVM | 0.66 | 0.95 | 0.66 | 0.757 |
| Naïve Bayes | 0.89 | 0.88 | 0.89 | 0.887 |

**Response Time Improvement:**  
120 ms → 54 ms (55% faster)

**Blockchain Integrity:**  
All 20 blocks verified (tamper-proof).

---

### 📘 Citation

If you use this repository, please cite:

> Mishra, S., Alfahidah, R. A., & Al Harbi, F. (2025).  
> *BERT–spaCy Hybrid NLP and Blockchain-Enhanced Adaptive CTI for IOC Extraction and Threat Prediction.*

---
