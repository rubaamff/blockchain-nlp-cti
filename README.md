# **BERT–spaCy Hybrid NLP and Blockchain‑Enhanced Adaptive CTI for IOC Extraction and Threat Prediction**




**Authors:**  
Shailendra Mishra, Ruba Ahmed Alfahidah, Fayez Al Harbi  
Majmaah University, Saudi Arabia

---

## Abstract
This project presents an integrated framework for **Cyber Threat Intelligence (CTI)** that combines **Natural Language Processing (NLP)** using **BERT and spaCy**, **adaptive machine learning**, and a **blockchain-inspired immutable ledger** for secure, tamper‑proof intelligence sharing.  
The main goal is to extract **Indicators of Compromise (IOCs)** from unstructured threat reports, classify cyber incidents intelligently, and ensure integrity and traceability of shared intelligence.  
The proposed hybrid system achieved **95% accuracy**, **95.7% F1-score**, and reduced response latency by **55%** (from 120ms to 54ms for 200 reports).  
Experiments were conducted on **CIC‑IDS2017** and **UNSW‑NB15** datasets, yielding a **Cross‑Dataset Robustness Index (CRI)** of **0.999**, proving strong generalization and adaptability.

---

## Motivation
- Modern networks produce large volumes of **unstructured security data** (blogs, dark web posts, reports, threat feeds). Manual IOC extraction is inefficient.  
- Traditional CTI systems relying on **signatures or static rules** fail to adapt to evolving attack tactics.  
- **Data sharing** across organizations suffers from trust and data tampering issues.  
- The proposed hybrid solution integrates **linguistic understanding (BERT)** and **pattern-based detection (Regex + spaCy)** while ensuring **immutability and provenance** using a blockchain-like ledger.

---

## Contributions
1. **Hybrid IOC Extraction Pipeline:**  
   Combines Regex for structural patterns (IPs, hashes, URLs), spaCy NER for named entities, and BERT for semantic IOC recognition in dynamic text.  
2. **Adaptive Threat Classification:**  
   A confidence‑weighted ensemble (BERT, LSTM, Naïve Bayes) improves contextual accuracy and self‑updates through incremental training.  
3. **Blockchain‑Inspired Immutable Ledger:**  
   SHA‑256 hashed audit chain that records CTI entries and prevents tampering during inter‑organizational sharing.  
4. **Statistical Evaluation Framework:**  
   Employs bootstrap and Monte Carlo‑based t‑tests for robust statistical significance.  
5. **Cross‑Dataset Robustness Index (CRI):**  
   Quantifies model generalization across CIC‑IDS2017 and UNSW‑NB15 datasets.

---

## Methodology

### 1. Data Collection and Preprocessing
- Datasets: **CIC‑IDS2017**, **UNSW‑NB15**, and unstructured CTI reports from open sources.  
- Preprocessing: text normalization, HTML cleaning, tokenization, lemmatization via spaCy.  
- Feature extraction: TF‑IDF and BERT contextual embeddings.

### 2. IOC Extraction
- **Regex:** Identifies IPs, hashes, URLs.  
- **spaCy NER:** Extracts malware names, domains, and organizations.  
- **BERT:** Detects semantically implied IOCs not captured by rules.  
- Aggregation logic merges results with weighted scoring based on occurrence and context.

### 3. Threat Classification
- Baseline: Multinomial Naïve Bayes + TF‑IDF (lightweight for runtime).  
- Advanced: LSTM and BERT models integrated through weighted voting.  
- Handles data imbalance with SMOTE and adaptive incremental retraining.  
- Ensemble outputs refined labels (“Malicious”, “Benign”, “Suspicious”) with probability thresholds.

### 4. Blockchain‑Inspired Ledger
- Lightweight chain implementation using **SHA‑256** hash of each record plus reference to the previous one.  
- Each entry: timestamp, content summary, previous hash, and computed signature.  
- Enables full ledger verification (`audit_trail`) to detect tampering.  
- Ensures authenticity of CTI logs shared between organizations.

### 5. Evaluation and Statistical Testing
- Metrics: Accuracy, Precision, Recall, F1‑Score, Detection Rate, False Positive Rate.  
- Tests: paired t‑test, bootstrap BCa, HC4, and Monte Carlo (10,000 simulations) for statistical robustness.  
- CRI computed to measure performance stability across datasets.

---

## Key Results
| Metric | BERT Ensemble | LSTM | Naïve Bayes | SVM |
|--------|----------------|------|--------------|------|
| Accuracy | **0.95** | 0.90 | 0.89 | 0.66 |
| Precision | **0.97** | 0.96 | 0.88 | 0.95 |
| Recall | **0.95** | 0.90 | 0.89 | 0.66 |
| F1‑Score | **0.957** | 0.921 | 0.887 | 0.757 |

**Latency Reduction:** 120ms → 54ms (≈55% improvement)  
**CRI (BERT):** 0.999 (cross‑dataset robustness)  
**t‑statistic:** 3.45 (p < 0.001) — strong statistical significance  
**Cohen’s d:** 0.76–1.12 — large effect size

---

## Project Structure
```
blockchain-nlp-cti/
├── README.md                # Research explanation (this file)
├── requirements.txt         # Dependencies
├── main.py                  # Example execution
├── src/
│   ├── ioc_extraction.py
│   ├── threat_classification.py
│   ├── blockchain_ledger.py
│   ├── similarity_detection.py
│   └── adaptive_learning.py
└── data/
    └── sample_reports.txt
```

---

## Usage
1. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
2. Download the spaCy model:  
   ```bash
   python -m spacy download en_core_web_sm
   ```
3. Run example pipeline:  
   ```bash
   python main.py
   ```
4. Extend training using larger datasets (CIC‑IDS2017 / UNSW‑NB15) and fine‑tune parameters for production deployment.

---

## Limitations and Future Work
- Current blockchain ledger runs in a single‑node simulated environment; distributed multi‑agent deployment remains to be tested.  
- IOC extraction for complex multi‑stage tactics can be improved using hybrid **neural‑symbolic reasoning** integrated with MITRE ATT&CK ontology.  
- Privacy and compliance enhancements (e.g., **differential privacy**, **secure multi‑party computation**) for safe CTI sharing.  
- Further evaluation on real SOC (Security Operations Center) environments for scalability and latency validation.

---

## File Descriptions
- `src/ioc_extraction.py`: Extracts IPs, domains, malware names using Regex + spaCy.  
- `src/threat_classification.py`: Naïve Bayes TF‑IDF classifier with adaptive learning.  
- `src/blockchain_ledger.py`: Blockchain‑style immutable log for CTI entries.  
- `main.py`: Demonstration script showing the full workflow.  

---
