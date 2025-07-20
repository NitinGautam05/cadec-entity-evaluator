# CADEC Entity Evaluator

This repository contains code for evaluating entity extraction and normalization on the [CADEC](https://academic.oup.com/jamia/article/23/1/116/2379847) (CSIRO Adverse Drug Event Corpus) dataset. The tasks are focused on mapping extracted entities such as Adverse Drug Reactions (ADRs), Drugs, Diseases, and Symptoms to standard ontologies like **MedDRA** and **SNOMED CT**.

---

## 🧠 Project Tasks

### ✅ Task 1: BIO Tagging with LLM
- Extract medical entities using BIO tagging from forum posts.
- Uses a large language model (e.g., DeepSeek R1 Distill) to predict token-level labels.

### ✅ Task 2: Entity Normalization
- Normalize noisy or misspelled entities using ontology-based mapping.
- Matches entity clusters to their correct MedDRA or SNOMED CT codes.

### ✅ Task 3: Linking with SCT
- Link annotated text segments to SNOMED CT (SCT) concept IDs and descriptions.
- Match CADEC original annotations with SCT standard equivalents.

### ✅ Task 4: Performance Evaluation on ADR Labels
- Evaluate predicted vs. ground truth ADRs using MedDRA annotations.
- Calculate precision, recall, and F1-score specifically for ADR entity type.

### ✅ Task 5: Combined Standardization
- Combine outputs from original annotations and SCT normalization.
- Consolidate `code`, `label type`, `text`, and `standard description` in a unified format.

---
