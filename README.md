# A Blockchain-Driven NLP and ML Framework for Adaptive and Explainable Cyber Threat Intelligence Systems

This repository contains the source code, datasets, and documentation for the research paper titled "A Blockchain-Driven NLP and ML Framework for Adaptive and Explainable Cyber Threat Intelligence Systems." The project demonstrates a novel framework for enhancing cyber threat intelligence (CTI) by integrating Natural Language Processing (NLP), Machine Learning (ML), and a blockchain-inspired logging mechanism.

## Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Running the Framework](#running-the-framework)
  - [Expected Output](#expected-output)
- [Reproducibility](#reproducibility)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Project Overview

The framework is designed to automate the analysis of cyber threat reports, extract Indicators of Compromise (IOCs), classify threats, and maintain an immutable log of all processed intelligence. Key features include:

- **IOC Extraction**: Utilizes `spaCy` and regular expressions to identify artifacts such as IP addresses, domain names, and malware signatures from unstructured text.
- **Threat Classification**: Employs a `scikit-learn` based `MultinomialNB` classifier with adaptive learning capabilities to distinguish between benign and malicious reports.
- **Blockchain-Inspired Logging**: Implements a custom `ImmutableTrail` to create a tamper-resistant ledger of all CTI records, ensuring data integrity and provenance.
- **Comprehensive Evaluation**: Includes a suite of ML models (Naive Bayes, SVM, LSTM, and a simulated BERT) for performance comparison and robust evaluation.
- **Data Visualization**: Generates insightful plots to visualize model performance, threat detection accuracy over time, blockchain integrity, and other key metrics.

## Repository Structure

```
.
├── blockchainnlpcti.py
├── requirements.txt
├── environment_setup.md
├── associated_data_insert.md
├── README.md
├── data/
│   └── Wednesday-workingHours.pcap_ISCX.csv (to be added by user)
└── output/
    ├── Naive_Bayes_confusion_matrix.png
    ├── SVM_confusion_matrix.png
    ├── LSTM_confusion_matrix.png
    ├── BERT_confusion_matrix.png
    ├── model_comparison_plots.png
    ├── model_comparison_results.csv
    ├── Threat Detection Accuracy Over Time.png
    ├── Blockchain Data Integrity.png
    ├── Threat Detection Response Time.png
    └── Extraction Performance (NLP Components).png
```

### File Descriptions

- **`blockchainnlpcti.py`**: The main Python script containing the entire framework, including data preprocessing, model training, blockchain implementation, and visualization functions.
- **`requirements.txt`**: A list of all Python dependencies required to run the project.
- **`environment_setup.md`**: Detailed instructions on how to set up the environment for reproducibility.
- **`associated_data_insert.md`**: The suggested text for the "Associated Data" section of the manuscript.
- **`README.md`**: This file, providing an overview and instructions for the project.
- **`data/`**: A directory to store the dataset. The user needs to download the `Wednesday-workingHours.pcap_ISCX.csv` file and place it here.
- **`output/`**: A directory where all generated plots and results will be saved.

## Getting Started

### Prerequisites

- Python 3.11+
- `pip` and `venv`

### Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd <repository-name>
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download the spaCy model:**
    ```bash
    python -m spacy download en_core_web_sm
    ```

5.  **Download the dataset:**
    Download the `Wednesday-workingHours.pcap_ISCX.csv` file from the [CICIDS2017 dataset](https://www.unb.ca/cic/datasets/ids-2017.html) and place it in the `data/` directory. You will need to create this directory.

## Usage

### Running the Framework

To run the entire pipeline, execute the main script from the root of the project directory:

```bash
python blockchainnlpcticopy.py
```

### Expected Output

The script will perform the following actions:

1.  Load and preprocess the CICIDS2017 dataset.
2.  Train and evaluate the Naive Bayes, SVM, LSTM, and simulated BERT models.
3.  Print the classification reports and model comparison results to the console.
4.  Save the confusion matrices and other performance plots to the `output/` directory.
5.  Demonstrate the blockchain-inspired logging of threat intelligence.

## Reproducibility

To ensure full reproducibility, we have provided all the necessary code, dependencies, and instructions. Please follow the steps in the [Getting Started](#getting-started) section carefully. The `environment_setup.md` file contains more detailed information on setting up the environment.

## Troubleshooting

- **`FileNotFoundError` for the dataset:** Ensure that you have downloaded the `Wednesday-workingHours.pcap_ISCX.csv` file and placed it in the correct directory. You may also need to adjust the `DATASET_PATH` variable in `blockchainnlpcticopy.py` to point to the correct location.
- **`ModuleNotFoundError`:** Make sure you have activated the virtual environment and installed all the packages from `requirements.txt`.
- **Issues with TensorFlow/Keras:** The provided `requirements.txt` file should specify compatible versions. If you encounter issues, please ensure you are using a compatible version of Python and that the installation was successful.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
