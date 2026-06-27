# 🐞 BugClassiNet: Semantic Bug Report Classification

A multi-stage deep learning framework for automatic software bug report classification using state-of-the-art Natural Language Processing (NLP). BugClassiNet combines semantic embeddings with deep learning architectures to accurately identify, categorize, and prioritize bug reports from large-scale software repositories.

---

## 🚀 Features

* 🧠 **Semantic Bug Understanding** – Fine-tuned **Sentence-BERT (SBERT)** generates domain-specific semantic embeddings that capture the contextual meaning of bug reports beyond keyword matching.
* 🏗️ **Hierarchical Classification Pipeline** – Multi-stage framework for classifying reports into **Bug/Non-Bug**, **Bohrbug/Mandelbug**, and **ARB/NAM** categories.
* ⚡ **Hybrid Deep Learning Models** – Combines lightweight **1D CNN** classifiers with Transformer-based semantic representations for high accuracy and efficient inference.
* 🔬 **Domain-Specific Data Processing** – Advanced preprocessing, metadata integration, and hard-negative sampling improve robustness on real-world software engineering datasets.
* 📊 **High Performance** – Achieves an **F1-Score of 0.9644** on highly imbalanced bug report datasets.
* 🔌 **Modular Design** – Easily extendable for new datasets, bug taxonomies, and software engineering research tasks.

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/shreyash18g/BugClassiNet.git
cd BugClassiNet
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🛠️ Usage

### Train the Semantic Embedding Model

```bash
python train_semantic_model.py \
    --data_path /path/to/dataset \
    --output_dir models/semantic_model
```

### Run Bug vs. Non-Bug Classification

```bash
python run_classification.py \
    --model_type cnn \
    --data_path /path/to/linux_dataset.csv \
    --semantic_model models/semantic_model
```

### Run Hierarchical Classification

```bash
python run_classification.py \
    --model_type transformer \
    --data_path /path/to/linux_dataset.csv \
    --semantic_model models/semantic_model
```

---

## 📂 Repository Structure

```text
BugClassiNet/
│
├── LinuxData/              # Linux bug report datasets
├── ModelTraining/          # Training notebooks and model implementations
├── preprocessing/          # Data preprocessing scripts
├── results/                # Experimental results and evaluation
│
├── app.py                  # Application entry point
├── README.md               # Project documentation
└── requirements.txt        # Project dependencies
```

---

## 📈 Performance

| Task                           | Metric                       |
| ------------------------------ | ---------------------------- |
| Bug vs. Non-Bug Classification | F1-Score: **96.44%**         |
| Semantic Representation        | Fine-tuned Sentence-BERT     |
| Architecture                   | SBERT + 1D CNN + Transformer |

---

## 🧰 Tech Stack

* Python
* PyTorch
* Sentence-BERT (SBERT)
* Transformers
* Scikit-learn
* Pandas
* NumPy
* Jupyter Notebook

---

## 👨‍💻 Author

**Shreyash Gupta**

* GitHub: https://github.com/shreyash18g
* LinkedIn: https://linkedin.com/in/shreyash2004

---

## 📄 License

This project is intended for academic and research purposes.
