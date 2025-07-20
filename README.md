# CADEC Entity Evaluator

This repository contains code for evaluating entity extraction and normalization on the [CADEC](https://academic.oup.com/jamia/article/23/1/116/2379847) (CSIRO Adverse Drug Event Corpus) dataset. The tasks are focused on mapping extracted entities such as Adverse Drug Reactions (ADRs), Drugs, Diseases, and Symptoms to standard ontologies like **MedDRA** and **SNOMED CT**.

---

## 🧠 Project Tasks

### ✅ Task 1: Enumerate Distinct Entities
- Extract and enumerate **distinct entities** for each label type:
  - `ADR`, `Drug`, `Disease`, `Symptom`
- Output:
  - Unique entity list and count per label type from the complete dataset.

### ✅ Task 2: BIO Tagging with LLM
- Use a suitable **LLM from Hugging Face** to label forum post text with entity types.
- **Two-step labeling:**
  1. BIO (IOB) tagging at word level
  2. Convert to CADEC-style annotation format as found in the `original` sub-directory

### ✅ Task 3: Evaluate Labeling Performance
- Compare the predicted annotations from Task 2 against the **ground truth** in the `original` sub-directory.
- Use a suitable metric (e.g., Precision, Recall, F1-score).
- Justify your metric choice in code comments.

### ✅ Task 4: Evaluate ADRs using MedDRA
- Repeat the Task 3 evaluation **only for `ADR` labels**.
- Use the MedDRA-specific annotations in the `meddra` sub-directory as ground truth.

### ✅ Task 5: Evaluate on 50 Random Forum Posts
- Extend evaluation (as in Task 3) to **50 randomly selected forum posts** from the `text` directory.
- Automate sampling and report overall performance.

---
