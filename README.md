# 🐞 BugClassiNet: Semantic Bug Report Classification

A multi-stage deep learning framework to automatically classify software bug reports with high accuracy using state-of-the-art NLP.

---

## 🚀 Features

-   🧠 **State-of-the-Art Semantic Understanding** — Utilizes a fine-tuned **Sentence-BERT (SBERT)** model to understand the true meaning of bug reports, not just keywords.
-   🏗️ **Specialized Dual-Model Architecture** — Employs a lightweight **1D CNN** for fast initial triage and a powerful **Transformer** for deep, nuanced analysis.
-   💡 **Innovative Data Augmentation** — Introduces **domain-specific hard-negative sampling** to create a robust model that isn't fooled by technical jargon.
-   🔬 **Multi-Level Classification** — Categorizes reports by **Existence** (Bug/Non-Bug), **Complexity** (Bohrbug/Mandelbug), and **Root Cause** (ARB/NAM).
-   📊 **Proven High Performance** — Achieves an **F1-Score of 0.9644** on highly imbalanced, real-world data where traditional methods fail.
-   🔌 **Modular & Extensible** — Designed to be easily integrated into existing bug tracking workflows and extended for other software engineering tasks.

---

## 📦 Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/patelkanak23/BugClassiNet.git](https://github.com/patelkanak23/BugClassiNet.git)
    cd BugClassiNet
    ```

2.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

---

## 🛠️ How to Use

*(This is a template. You should update this with your actual script names and arguments.)*

1.  **Train the semantic model:**
    ```bash
    python train_semantic_model.py --data_path /path/to/your/data --output_dir /models/sem_model_4
    ```

2.  **Run the Bug vs. Non-Bug classification:**
    ```bash
    python run_classification.py --model_type cnn --data_path /path/to/linux_dataset.csv --semantic_model /models/sem_model_4
    ```

3.  **Run the advanced classification:**
    ```bash
    python run_classification.py --model_type transformer --data_path /path/to/curated_linux.xlsx --semantic_model /models/sem_model_4
    ```


## 📂 Repository Structure

```
BugClassiNet/
│
├── data/                     # Folder for datasets (e.g., Linux, GCC, LLVM)
├── models/                   # Folder to save trained models and embeddings
├── notebooks/                # Jupyter notebooks for exploration and analysis
├── src/                      # Source code for the project
│   ├── preprocessing.py      # Data cleaning and augmentation scripts
│   ├── models.py             # Definitions for the CNN and Transformer architectures
│   ├── train.py              # Script for training the models
│   └── evaluate.py           # Script for evaluating model performance
│
├── requirements.txt          # List of Python dependencies
└── README.md                 # This file
```

---


