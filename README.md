# 🏥 EHRSQL: Reliable Text-to-SQL Modeling on Electronic Health Records

This repository contains code and experiments for the Clinical NLP 2024 Shared Task on **Text-to-SQL modeling** over the MIMIC-IV Electronic Health Records dataset. The goal is to build models that can translate natural language questions into executable SQL queries.

---

## 🚀 Project Flow

### 1. **Setup & Installation**
- Clone the repository
- Install required dependencies (e.g., `transformers`, `sentencepiece`, etc.)
- Set up directory structure for data and checkpoints

### 2. **Data Preparation**
- Download and unzip MIMIC-IV demo dataset
- Preprocess input questions and schema files
- Split data into `train`, `validation`, and `test` sets

### 3. **Model Training**
- Train three baseline models:
  - `T5` (vanilla encoder-decoder)
  - `MedT5SQL` (domain-adapted variant)
  - `CodeT5` (code-specialized transformer)
- Save checkpoints and logs

### 4. **Model Evaluation**
- Evaluate models using:
  - Accuracy@0, Accuracy@5, Accuracy@10, Accuracy@N
  - Support for filtering unanswerable queries
- Compare model performance

### 5. **Inference & Submission**
- Run inference on `test.jsonl`
- Generate SQL predictions
- Format output for Codabench or local analysis

---

## 📊 Accuracy Comparison (Filtered Unanswerable)

| Model       | Accuracy@0 | Accuracy@5 | Accuracy@10 | Accuracy@N |
|-------------|-------------|-------------|--------------|-------------|
| T5          | 72.49%      | -61.66%     | -195.80%     | -274.28     |
| MedT5SQL    | 65.95%      | -92.10%     | -250.15%     | -323.34     |
| CodeT5      | 69.07%      | **-4.59%**  | **-78.24%**  | **-150.31** |

---

## 📁 Folder Structure

