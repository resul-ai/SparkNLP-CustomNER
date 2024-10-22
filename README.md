# SparkNLP Healthcare NER Pipeline

This project demonstrates the development of a custom Named Entity Recognition (NER) model for healthcare data using Spark NLP, implemented in three main phases.

## Project Overview

Using a medical transcription dataset (mt_samples), we built a pipeline that:
1. Combines multiple pre-trained clinical NER models
2. Generates standardized CoNLL training data
3. Trains a custom NER model

## Implementation

### Phase 1: Multi-Model NER Pipeline
- Implemented a pipeline combining three pre-trained Spark NLP models:
  - `ner_clinical`: For clinical entities
  - `ner_posology`: For medication-related entities
  - `ner_deid_generic`: For de-identification entities
- Used `ChunkMergeApproach` to combine and prioritize entity predictions
- Processed the mt_samples dataset containing 50 medical transcriptions

### Phase 2: CoNLL Generation
- Converted the merged NER predictions into CoNLL format
- Generated training data with 6 entity types:
  - PROBLEM
  - TREATMENT
  - TEST
  - DRUG
  - NAME
  - DATE
- Applied standardized BIO tagging scheme for entity boundaries

### Phase 3: Custom Model Training
- Trained a new medical NER model using the generated CoNLL data
- Utilized clinical word embeddings for enhanced domain specificity
- Implemented early stopping and model evaluation
- Achieved test set performance:
  - Macro-average F1: 0.79
  - Micro-average F1: 0.81

## Results

The final model successfully recognizes domain-specific entities in medical text, with particularly strong performance on clinical problems (F1: 0.85) and diagnostic tests (F1: 0.80).

## Setup & Usage

The implementation is organized in three Jupyter notebooks:
1. `1_Pipeline_Implementation_with_Chunk_Merger.ipynb`
2. `2_CoNLL_File_Generation.ipynb`
3. `3_Custom_NER_Model_Training.ipynb`

Requires Spark NLP Healthcare license and dependencies as specified in each notebook.

---
*Developed by R. Caliskan*