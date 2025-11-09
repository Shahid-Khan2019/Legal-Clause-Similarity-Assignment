# 🧾 Legal Clause Similarity — Deep Learning Assignment

## 📘 Overview
This repository contains the implementation and analysis for the **Legal Clause Similarity** task.  
The objective of this assignment was to build and compare baseline deep learning models that identify whether two legal clauses convey the same meaning.

Both the **code file** and **report** are included here:
- `Code.ipynb` → Complete code for preprocessing, model training, and evaluation.
- `22I-2019_ShahidUllah.pdf` → Detailed report with architecture explanation, metrics, graphs, and examples.

---

## 🧩 Task Objective
The goal of this project was to develop a **legal clause similarity system** capable of:
- Understanding semantic similarity between legal sentences.
- Evaluating performance across multiple baselines.
- Discussing domain-relevant evaluation metrics for real-world deployment.

---

## 🧠 Model Architectures

Two models were developed and compared:

### 1. **BiLSTM**
- Embedding Layer (trainable word embeddings)
- Bidirectional LSTM for contextual representation
- Max and average pooling
- Fully connected layers for classification
- Sigmoid output for binary similarity

### 2. **Attention-Based BiLSTM**
- Same as above, with an added **attention layer** to weigh contextually important words.
- Improved interpretability and accuracy on complex clauses.

---

## ⚙️ **Training Configuration**
| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Loss Function | Binary Cross-Entropy |
| Batch Size | 64 |
| Epochs | 10 |
| Mixed Precision | Enabled (torch.cuda.amp) |
| Early Stopping | Based on validation loss |
| Device | GPU (CUDA) |

---

## 📊 **Performance Comparison**

| **Model** | **Train Accuracy** | **Validation Accuracy** | **Train Loss** | **Validation Loss** | **Test Accuracy** | **Precision** | **Recall** | **F1-Score** | **ROC-AUC** | **PR-AUC** |
|------------|-------------------:|------------------------:|---------------:|--------------------:|-----------------:|--------------:|-----------:|-------------:|------------:|-----------:|
| **BiLSTM** | 0.9916 | 0.9643 | 0.0294 | 0.1384 | 0.9645 | 0.9370 | 0.996 | 0.9656 | 0.9949 | 0.9929 |
| **Attention-BiLSTM** | 0.9942 | 0.9826 | 0.0197 | 0.0582 | 0.9825 | 0.9689 | 0.997 | 0.9828 | 0.9952 | 0.9918 |

---

## 📈 **Training Results**
- Loss decreased steadily across epochs.
- Validation accuracy increased and stabilized around 98%.
- Early stopping prevented overfitting.

Both models achieved excellent generalization, with **Attention-BiLSTM** outperforming slightly due to better contextual focus.

---

## 🧮 **Evaluation Metrics**
Metrics used include **Accuracy**, **Precision**, **Recall**, **F1-score**, **ROC-AUC**, and **PR-AUC**.

For real-world deployment (“in the wild”), **Precision** and **ROC-AUC** are prioritized to ensure minimal false matches in legal contexts.

---

## ✅ **Example Clause Pairs**

### ✔ Correctly Matched
- “This agreement shall be governed by the laws of the State of New York.”  
  ↔ “The contract shall be interpreted under New York State law.”
  
- “Each party agrees to maintain confidentiality of all shared data.”  
  ↔ “Both parties must ensure confidentiality of exchanged information.”

### ❌ Incorrectly Matched
- “The supplier shall deliver goods within thirty days.”  
  ↔ “Either party may terminate this agreement upon breach.”

---

## 📄 **File Naming Convention**
Submitted as per requirement:  
`i232038_LegalClauseSimilarity_Report.pdf`

---

## 🧑‍💻 **Author**
**Name:** Shahid Khan  
**Roll No:** 22I-2019  
**Course:** Deep Learning    
**Institution:** FAST-NUCES  

---

## 🏁 **Conclusion**
This assignment successfully demonstrates semantic similarity detection in the legal domain using deep learning.  
The **Attention-based BiLSTM** model achieved the highest performance with superior interpretability and reliability, making it suitable for real-world legal clause analysis systems.

---

## 📎 Repository Contents

---

## 🔗 **Submission**
This repository is submitted as part of the **Deep Learning Course Assignment** for evaluation purposes.
