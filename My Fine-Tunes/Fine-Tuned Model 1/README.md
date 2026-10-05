# Fine-Tuned Model 1 — DeBERTa-v3 Email Threat Classifier

## Overview

This is my **first completed fine-tuned model** showcased in this repository.

The model is based on **Microsoft DeBERTa-v3-base** and was fine-tuned for **binary email threat classification** as part of an AI-powered email security and forensic intelligence use case.

## What the Model Does

The model analyzes email text and predicts one of two classes:

- **BENIGN**
- **MALICIOUS**

It is intended to act as the **AI classification component** of a broader email threat detection pipeline.

## Model Information

- **Base model:** `microsoft/deberta-v3-base`
- **Architecture:** DeBERTa / Transformer-based encoder
- **Task:** Binary email threat classification
- **Labels:** BENIGN / MALICIOUS
- **Parameters:** Approximately **184.4M**
- **Maximum sequence length:** 256
- **Tokenizer:** `DebertaV2Tokenizer`
- **Training dataset:** `ForentisAI_DeBERTa_Dataset_V2`
- **Dataset type:** Synthetic
- **Training environment:** Google Colab
- **Model format:** Safetensors

## Hugging Face Model

The complete fine-tuned model is hosted on Hugging Face.

**Model repository:**

https://huggingface.co/sudiptaroy07/forentisai-deberta-v3-email-threat-classifier

The Hugging Face repository contains the large model artifact and is the recommended location for downloading and testing the complete model.

## Fine-Tuning

The model was fine-tuned from:

```text
microsoft/deberta-v3-base
```

The best checkpoint recorded in the training metadata was:

```text
/content/forentisai_deberta_v3/checkpoint-1312
```

## Evaluation

The recorded evaluation was performed on **4,499 synthetic test samples**.

| Metric | Result |
|---|---:|
| Accuracy | 1.00 |
| Precision | 1.00 |
| Recall | 1.00 |
| F1 | 1.00 |
| ROC-AUC | 1.00 |

> **Important:** These results come from a synthetic test set and do **not** establish equivalent real-world deployment performance.

## Manual Testing

The model was also tested manually with previously unseen, constructed email examples.

It correctly classified several benign, obvious phishing, subtle phishing, and Business Email Compromise-style examples during basic testing. One deliberately subtle phishing-style example was classified as `benign`, demonstrating that high-confidence predictions are not guaranteed to be correct.

This is why additional testing on diverse and representative real-world email data is required before production deployment.

## Repository Organization

### `Model/`

The `Model/` directory documents where the large model artifact belongs conceptually.

The complete model is approximately **700 MB** and is hosted on Hugging Face instead of being stored directly in GitHub.

See:

https://huggingface.co/sudiptaroy07/forentisai-deberta-v3-email-threat-classifier

### `Model Files/`

This directory contains the smaller supporting files that describe the model and its deployment configuration.

Current files include:

- `config.json`
- `deployment_info.json`
- `forentisai_model.json`
- `tokenizer_config.json`

## Model Purpose

This model is part of my practical work in **AI-powered email threat detection and forensic intelligence**.

It can be used as one component of a larger workflow:

```text
Incoming Email
      ↓
Email Text Extraction
      ↓
Text Preprocessing
      ↓
DeBERTa Threat Classifier
      ↓
BENIGN / MALICIOUS
      ↓
Additional Security Analysis
      ↓
Final Threat Assessment
```

## Limitations

- The training and evaluation dataset is synthetic.
- The reported metrics may not represent real-world performance.
- False positives and false negatives are possible.
- The model may encounter threat patterns that were not represented in training.
- A high confidence score does not guarantee a correct prediction.
- The model should not be the sole decision-maker for cybersecurity incidents.
- Representative real-world evaluation is required before production deployment.

## Status

**Fine-tuned — Completed**

**Fine-tuned by Sudipta Roy**
