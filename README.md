# 🧠 BERT Fine-Tuning for Named Entity Recognition (NER) on CoNLL-2003

This repository contains a Colab-based implementation of **fine-tuning BERT** for the **Named Entity Recognition (NER)** task using the **CoNLL-2003** dataset. The goal is to identify entities like `PER`, `ORG`, `LOC`, and `MISC` in raw text.

---

## 📌 Highlights

- ✅ Fine-tunes `bert-base-cased` on CoNLL-2003 using HuggingFace Transformers
- 📄 Supports standard BIO tagging scheme
- 📈 Achieves **F1 Score ~ 0.89**, **Accuracy ~ 97.15%**
- 🧪 Evaluation using `seqeval`
- 💡 Inference-ready pipeline to extract entities from raw text

---

## 📁 Files in this Repository

| File | Description |
|------|-------------|
| `bert_ner_finetuning.ipynb` | Main Colab notebook with all steps: preprocessing, training, evaluation, and inference |
validation, and testing (upload in Colab session) |
| `README.md` | You're here! Project overview and usage guide |

---
Dataset link:
https://www.kaggle.com/datasets/juliangarratt/conll2003-dataset?resource=download

---

## ⚙️ How to Run

> You can run everything on **Google Colab** with GPU support — no local setup required!

### ▶️ [Open in Colab](https://colab.research.google.com/github/Mlakshay01/BERT-NER-FINE-TUNED/blob/main/bert_ner_finetuning.ipynb)

1. Upload the CoNLL-2003 dataset files (`eng.train`, `eng.testa`, `eng.testb`)
2. Run the notebook cells in order
3. Optional: Download the fine-tuned model for inference or deployment

---

## 🧠 Model Details

- **Base Model**: `bert-base-cased`
- **Task**: Token Classification (NER)
- **Loss Function**: CrossEntropyLoss
- **Evaluation**: Precision, Recall, F1 Score using `seqeval`

---

## 🔍 Example Inference Output

```python
Input: "Barack Obama was born in Hawaii."

Output:
[
  {'entity_group': 'PER', 'word': 'Barack Obama', 'score': 0.999},
  {'entity_group': 'LOC', 'word': 'Hawaii', 'score': 0.998}
]

📈 Results
| Metric       | Score    |
| ------------ | -------- |
| **F1 Score** | \~0.89   |
| **Accuracy** | \~97.15% |

📚 Dataset: CoNLL-2003
4 Named Entity Types: PER, LOC, ORG, MISC

BIO tagging format (B-PER, I-ORG, O, etc.)

Format: One word per line with tag, separated by empty lines between sentences

📦 Dependencies
pip install transformers datasets seqeval

**Or let Colab handle it via built-in cells.

📜 License
This project is licensed under the MIT License.
Use it freely for research, learning, or extensions.

👤 Author
Developed by Lakshay Malik
For questions, collaborations, or feedback — feel free to connect!

🙌 Acknowledgments
https://huggingface.co/transformers/
https://github.com/chakki-works/seqeval
[CoNLL-2003 dataset contributors](https://www.kaggle.com/datasets/juliangarratt/conll2003-dataset?resource=download)
