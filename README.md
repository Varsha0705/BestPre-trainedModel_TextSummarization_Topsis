# BestPre-trainedModel_TextSummarization_Topsis

# Text Summarization Model Evaluation using TOPSIS

This project applies **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** to evaluate different **pre-trained text summarization models** based on ROUGE scores and inference time.

---

##  Overview

- Uses **Hugging Face Transformers** to load pre-trained models.
- Summarizes a sample text using multiple models.
- Evaluates the summaries using **ROUGE** scores.
- Uses **TOPSIS** to rank the models based on performance.
- **Visualizes results** using Matplotlib & Seaborn.

---

##  Models Evaluated

| Model                  | Architecture |
|------------------------|-------------|
| `facebook/bart-large-cnn` | BART |
| `t5-small`            | T5 |
| `t5-base`             | T5 |
| `google/pegasus-xsum` | PEGASUS |

---

##  Installation

Run the following command to install dependencies:

```bash
pip install transformers datasets evaluate rouge-score numpy pandas matplotlib seaborn

```

##  Results

| Model                  | ROUGE-1 | ROUGE-2 | ROUGE-L | Inference Time (s) |
|------------------------|---------|---------|---------|-------------------|
| `facebook/bart-large-cnn` | 0.45 | 0.21 | 0.39 | 2.1 |
| `t5-small`             | 0.41 | 0.18 | 0.35 | 1.3 |
| `t5-base`              | 0.44 | 0.19 | 0.38 | 1.7 |
| `google/pegasus-xsum`  | 0.47 | 0.22 | 0.41 | 2.5 |

---

##  Final Ranking (TOPSIS Score)

| Rank | Model                  | TOPSIS Score |
|------|------------------------|--------------|
|  1 | `google/pegasus-xsum`  | 0.82 |
|  2 | `facebook/bart-large-cnn` | 0.78 |
|  3 | `t5-base`              | 0.74 |
| 4    | `t5-small`             | 0.69 |

