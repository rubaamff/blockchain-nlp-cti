## Environment Setup

To reproduce the results of this study, please follow these steps to set up your environment:

### System Requirements

- **Operating System**: Ubuntu 22.04 (or a compatible Linux distribution)
- **Python**: Version 3.11.0rc1
- **Memory**: At least 8GB RAM (16GB recommended for larger datasets)
- **Disk Space**: At least 20GB free disk space
- **Internet Connection**: Required for downloading datasets and Python packages.

### Installation Steps

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/your-repo/your-project.git
    cd your-project
    ```
    *(Note: Replace `https://github.com/your-repo/your-project.git` with the actual repository URL once it's available.)*

2.  **Create a Virtual Environment (Recommended)**:
    ```bash
    python3.11 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Dependencies**:
    Install the required Python packages using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download SpaCy Model**:
    The project uses the `en_core_web_sm` SpaCy model. Download it using:
    ```bash
    python -m spacy download en_core_web_sm
    ```

5.  **Dataset Setup**:
    The project utilizes a subset of the CICIDS2017 dataset, specifically `Wednesday-workingHours.pcap_ISCX.csv`. Please download this file and place it in the designated data directory (e.g., `/content/drive/MyDrive/` as indicated in the provided Python script, or adjust the `DATASET_PATH` variable in `blockchainnlpcticopy.py` to your local path).

    *(Note: Ensure the dataset path in `blockchainnlpcticopy.py` matches the location where you save the dataset.)*

### Verifying Setup

After completing these steps, your environment should be ready. You can verify the setup by running the main script:

```bash
python blockchainnlpcticopy.py
```

This will execute the threat intelligence framework, including data preprocessing, model training, and visualization generation.

