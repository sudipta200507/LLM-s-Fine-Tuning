# LLM Fine-Tuning

A personal repository where I **showcase the language models I fine-tune myself**.

The main purpose of this repository is to keep a public record of my fine-tuning work — the pretrained models I adapt, the tasks they are built for, the datasets and text used, the training experiments I run primarily in **Google Colab**, and the resulting model artifacts.

The repository also contains a separate learning section with standalone HTML notes for understanding LLM fine-tuning.

## What This Repository Is Mainly About

This is my **fine-tuned model showcase**, not a course repository.

Every model added to **My Fine-Tunes** represents a practical fine-tuning experiment or project.

Typical workflow:

```text
Pretrained Model
      ↓
Task / Project Definition
      ↓
Dataset & Text Preparation
      ↓
Fine-Tuning in Google Colab
      ↓
Evaluation / Testing
      ↓
Model Artifact / Model Hub
      ↓
Documentation
```

## My Fine-Tuning Work

The `My Fine-Tunes/` folder is the main showcase area.

Each fine-tuning project can contain:

- Model-specific documentation
- Configuration and tokenizer files
- Training/deployment metadata
- Evaluation results
- Sample testing information
- A link to the complete hosted model artifact

### Models

| Model | Purpose | Base Model | Parameters | Environment | Status |
|---|---|---|---:|---|---|
| **Fine-Tuned Model 1 — DeBERTa-v3 Email Threat Classifier** | Email threat classification for an AI-powered email security / forensic intelligence use case | `microsoft/deberta-v3-base` | **184.4M** | Google Colab | Completed |

### Fine-Tuned Model 1

The first completed model is a **Transformer-based DeBERTa model fine-tuned for binary email threat classification**.

It classifies email text into:

- **BENIGN**
- **MALICIOUS**

The model was fine-tuned on the synthetic `ForentisAI_DeBERTa_Dataset_V2` dataset and evaluated on 4,499 synthetic test samples.

Recorded evaluation metrics:

| Metric | Score |
|---|---:|
| Accuracy | 1.00 |
| Precision | 1.00 |
| Recall | 1.00 |
| F1 | 1.00 |
| ROC-AUC | 1.00 |

> **Important:** These metrics were obtained on a synthetic test set and do not establish real-world deployment performance.

### Complete Model

The complete ~700 MB fine-tuned model is hosted on Hugging Face rather than stored directly in this Git repository.

**Hugging Face Model:**

https://huggingface.co/sudiptaroy07/forentisai-deberta-v3-email-threat-classifier

The GitHub repository contains the model documentation and supporting files, while Hugging Face hosts the complete model artifact for testing and use.

## What I Normally Fine-Tune With

My fine-tuning experiments can work with task-specific text such as:

- Instruction → response pairs
- Question → answer datasets
- Domain-specific explanations
- Classification / labeling examples
- Forensic or cybersecurity-related text
- Project-specific technical text
- Structured prompt-response examples
- Other curated text designed for a specific downstream behavior

The exact dataset format depends on the base model and the objective of the experiment.

## Learning Resources

The `LLM Fine-Tune Learning/` folder contains standalone HTML learning notes.

These files can be downloaded and opened directly in a browser. No build system is required.

Current learning notes:

1. **LLM Fine-Tuning — Complete Master Guide**
2. **Fine-tuning LLMs — 20 Min Master Guide**

These resources are complementary to the primary purpose of this repository: **showcasing my own fine-tuned models**.

## Repository Structure

```text
LLM-s-Fine-Tuning/
│
├── README.md
│
├── LLM Fine-Tune Learning/
│   ├── LLM_FineTuning_MasterNote_Interactive.html
│   └── finetune-llms-notes.html
│
└── My Fine-Tunes/
    └── Fine-Tuned Model 1/
        ├── README.md
        ├── Model/
        │   └── README.md
        └── Model Files/
            ├── README.md
            ├── config.json
            ├── deployment_info.json
            ├── forentisai_model.json
            └── tokenizer_config.json
```

The large `model.safetensors` and complete tokenizer/model package are hosted on Hugging Face.

## Fine-Tuning Philosophy

I use fine-tuning when the goal is to make a pretrained model better suited to a **specific task, domain, format, or behavior**.

Depending on the project and available resources, approaches can include:

- Full fine-tuning
- Parameter-Efficient Fine-Tuning (PEFT)
- LoRA
- Instruction tuning
- Supervised fine-tuning (SFT)

I also consider alternatives such as **prompt engineering** and **RAG** when they are a better fit for the problem.

## About

**Sudipta Roy**  
B.Tech CSE (AI & ML)

Interested in **AI/ML, LLM engineering, RAG, fine-tuning, cybersecurity, and practical AI systems**.

---

### Repository Intent

**Primary:** Showcase my personally fine-tuned models and experiments.  
**Secondary:** Provide standalone learning material for understanding LLM fine-tuning.
