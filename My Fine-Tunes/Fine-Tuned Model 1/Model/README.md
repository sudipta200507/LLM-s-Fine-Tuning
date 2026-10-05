# Fine-Tuned Model Artifact

The complete fine-tuned DeBERTa-v3 email threat classifier is hosted on Hugging Face because the model artifact is approximately **700 MB**.

## Complete Model

Hugging Face:

https://huggingface.co/sudiptaroy07/forentisai-deberta-v3-email-threat-classifier

The Hugging Face repository contains the complete model artifact, including the large model weights required for inference.

## GitHub Role

This directory is intentionally kept lightweight.

GitHub stores the documentation for the model and points to the hosted model artifact rather than duplicating the large model weights.

## Model

- **Base:** `microsoft/deberta-v3-base`
- **Task:** Binary email threat classification
- **Labels:** BENIGN / MALICIOUS
- **Parameters:** Approximately 184.4M
- **Format:** Safetensors
