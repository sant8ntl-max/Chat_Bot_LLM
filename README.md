# 🏦 Retail Banking Chatbot using FLAN-T5

This project builds an intelligent customer service chatbot for the **Retail Banking** sector using a fine-tuned version of Google's **FLAN-T5-small** large language model.

The chatbot can answer real-world banking queries such as balance checks, card activation, ATM location, loan inquiries, and more. It's trained on a publicly available dataset of prompt–response pairs and deployed using a Gradio web interface for interactive use.

---

## 🔍 Project Overview

- **Industry:** Retail Banking / Financial Services  
- **Model Used:** `google/flan-t5-small`  
- **Dataset:** Bitext Retail Banking LLM Chatbot Training Dataset  
- **Frameworks:** Hugging Face Transformers, Datasets, Gradio  
- **Goal:** Train and deploy a chatbot that simulates professional customer support

---

## 📁 Dataset Details

- Format: CSV  
- Columns:
  - `instruction`: Customer's question (prompt)
  - `response`: Ideal assistant reply (completion)
- Cleaned: Removed blanks, duplicates, and irrelevant entries  
- Size: ~24,000 prompt–response pairs

---

## 🧠 Model Training

- Model: `FLAN-T5-small` from Hugging Face
- Preprocessing: Tokenized with truncation and padding
- Fine-tuning: 3 epochs on 90% of data
- Loss Function: CrossEntropyLoss (default)
- Optimizer: AdamW

---

## 💬 Features

- Handles common banking queries:
  - Card services (activation, loss, recovery)
  - Account management
  - ATM/branch locator
  - Loan inquiries
- Polite, context-aware responses
- Instruction-following behavior
- Deployed using Gradio for testing

---

## 🚀 How to Run

### Requirements
```bash
pip install transformers datasets gradio scikit-learn
