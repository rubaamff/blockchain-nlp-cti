### Associated Data
To ensure transparency and reproducibility, all source code, processed datasets, and experimental scripts used in this study are publicly available at [GitHub/Zenodo DOI link: https://zenodo.org/record/XXXXXXX]. The repository includes:

- **Source Code**: Python scripts and Jupyter notebooks for data preprocessing, IOC extraction, classifier training, blockchain-inspired logging, and evaluation metrics. This includes the implementation of `identify_artifacts` for IOC extraction, `ThreatAnalyzer` for machine learning-based threat classification, and the `DigitalRecord` and `ImmutableTrail` classes for blockchain-inspired data integrity. The core code also encompasses functions for data loading, preprocessing (scaling, SMOTE), and the training and evaluation of various machine learning models (Naive Bayes, SVM, LSTM, and a  BERT model).

- **Dataset**: A subset of the CICIDS2017 dataset (specifically `Wednesday-workingHours.pcap_ISCX.csv`) used for experiments, along with preprocessing scripts and annotated threat reports. The dataset is utilized for training and evaluating the threat detection models.

- **Environment**: A `requirements.txt` file specifying Python package versions for replication, ensuring that the exact environment used for the research can be recreated. This includes dependencies such as `pandas`, `numpy`, `scikit-learn`, `imbalanced-learn`, `matplotlib`, `seaborn`, `spacy`, and `tensorflow`.

- **Documentation**: A README file detailing steps to reproduce results, system requirements, and file descriptions. This documentation will guide users through setting up the environment, running the code, and understanding the project structure.

This link has been included under the “Associated Data” section in the manuscript.

