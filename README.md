# 📦 Efficient Inventory Management with LLM

This project demonstrates how Large Language Models (LLMs) such as **Tapex** and **BERT** can be used to automate and optimize inventory management through intelligent question answering over tabular data.

By leveraging a sales dataset of 10,000 records, the models can:
- Understand inventory patterns
- Predict stock shortages
- Answer natural language questions
- Recommend data-driven restocking actions

---

## 🧠 Project Goals

- Use **Tapex** to answer complex inventory queries directly from tabular data
- Fine-tune **BERT** to generate contextual answers from structured inventory records
- Demonstrate how LLMs can power intelligent inventory dashboards

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `10000 Sales Records.csv` | Inventory/sales dataset with 10,000 records |
| `TAPEX_MODEL_BUILDING.ipynb` | LLM-based table QA using Microsoft Tapex |
| `BERT MODEL BUILDING.ipynb` | Context-based QA using BERT model |
| `README.md` | Full project documentation |

---

## 🔧 Technologies Used

- 🧠 **Microsoft Tapex** (table-specific LLM from Hugging Face)
- 🧠 **BERT** (`bert-base-uncased`) for context QA
- 🐍 Python, Pandas, PyTorch
- 🤗 Hugging Face Transformers
- 📊 CSV/Tabular data format

---

## 📊 Dataset Overview

**Filename**: `10000 Sales Records.csv`

| Column Name     | Description                    |
|-----------------|--------------------------------|
| Region          | Sales region (e.g., Asia)      |
| Country         | Country of the order           |
| Item Type       | Product category               |
| Sales Channel   | Online or Offline              |
| Order Priority  | H/M/L/C                        |
| Order Date      | When the order was placed      |
| Units Sold      | Quantity sold                  |
| Unit Price      | Price per unit                 |
| Unit Cost       | Cost per unit                  |
| Total Revenue   | Sales value                    |
| Total Cost      | Total cost of order            |
| Total Profit    | Net earnings from the sale     |

---

## 🔍 Key Features

- ✅ Ask questions like:
  - *What is the total profit from Africa in 2013?*
  - *Which item type has the lowest revenue in Europe?*
  - *Which countries had stockouts in 2015?*
- ✅ Answer generation using Tapex and BERT
- ✅ CSV parsing and prompt engineering
- ✅ Inventory insight generation

---

## 📘 Notebooks Explained

### 1️⃣ TAPEX_MODEL_BUILDING.ipynb

- Loads `10000 Sales Records.csv`
- Prepares prompt-style QA pairs
- Uses `microsoft/tapex-large` from Hugging Face
- Generates natural language answers from tabular input

### 2️⃣ BERT MODEL BUILDING.ipynb

- Converts table rows into readable context passages
- Tokenizes using `bert-base-uncased`
- Fine-tunes QA model for context-passage based answers
- Can be extended to chatbot-style applications

---

## 🚀 How to Run

```bash
# Install dependencies
pip install pandas torch transformers

# Launch either notebook
jupyter notebook TAPEX_MODEL_BUILDING.ipynb
# or
jupyter notebook BERT MODEL BUILDING.ipynb
