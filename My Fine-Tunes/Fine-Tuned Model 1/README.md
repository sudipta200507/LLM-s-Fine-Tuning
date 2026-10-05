# Fine-Tuned Model 1 — DeBERTa-v3 Email Threat Classifier

## Overview

This is my **first personally fine-tuned model** showcased in this repository.

The model is a fine-tuned **Microsoft DeBERTa-v3-base** model developed for the **Forensics AI / email threat detection** use case.

## Why I Fine-Tuned This Model

The purpose of this fine-tuning experiment was to adapt a pretrained language model for **email threat classification**.

The model classifies an email into two categories:

- **BENIGN**
- **MALICIOUS**

The model metadata identifies the task as binary_email_threat_classification.

## Base Model

- **Base model:** microsoft/deberta-v3-base
- **Architecture:** DeBERTa-v3-base
- **Task:** Binary email threat classification
- **Labels:** BENIGN / MALICIOUS
- **Maximum sequence length:** 256
- **Tokenizer:** DebertaV2Tokenizer
- **Training dataset:** ForentisAI_DeBERTa_Dataset_V2
- **Dataset type:** Synthetic

The model configuration identifies the underlying architecture as DebertaV2ForSequenceClassification, with 12 hidden layers, 12 attention heads, and a hidden size of 768.

## Fine-Tuning Environment

The fine-tuning experiment was performed in **Google Colab**.

The best checkpoint recorded in the model metadata is:

/content/forentisai_deberta_v3/checkpoint-1312

## Evaluation

The recorded evaluation was performed on **4,499 synthetic test samples**.

| Metric | Result |
|---|---:|
| Accuracy | 1.00 |
| Precision | 1.00 |
| Recall | 1.00 |
| F1 | 1.00 |
| ROC-AUC | 1.00 |

**Important:** These results come from the synthetic ForentisAI V2 test set and do **not** establish real-world deployment performance.

## Repository Files

The model directory is intentionally separated into:

### 1. Model

This is where the actual fine-tuned model artifact will be placed.

The complete model is approximately **700 MB**, so the model binary itself is not intended to be stored directly in this GitHub repository.

### 2. Model Files

This directory contains the supporting files required to describe or load the model, such as:

- Configuration
- Tokenizer
- Tokenizer configuration
- Deployment information
- Model metadata
- Other supporting artifacts

### 3. README.md

This file documents this specific fine-tuned model: why it was created, which base model was used, what task it performs, the training dataset, evaluation information, and the associated artifacts.

## Model Purpose

This model is part of my practical experimentation in **AI-powered email threat detection and forensic intelligence**.

It is designed as a classification component that can identify whether an email is benign or malicious.

## Status

**Fine-tuned — Completed**

The model and its supporting artifacts will be added to this directory manually.

---

**Fine-tuned by Sudipta Roy**