# LLM Fine-Tuning

A personal repository where I **showcase the LLMs I fine-tune myself**.

The main purpose of this repository is to keep a public record of my fine-tuning work — the models I train or adapt, the tasks they are built for, the data/style of text I use, and the practical experiments I run, primarily in **Google Colab**.

The repository also contains a separate learning section with standalone HTML notes that anyone can download and open locally as a web page to learn the fundamentals and workflow of LLM fine-tuning.

## What This Repository Is Mainly About

This is my **fine-tuned model showcase**, not a course repository.

Every model added to **My Fine-Tunes** represents an experiment or project in which I personally fine-tuned a pretrained language model.

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
Model Artifact / Showcase
      ↓
Documentation
```

## My Fine-Tuning Work

The `My Fine-Tunes/` folder is the main showcase area.

Each fine-tuning project can contain:

- The fine-tuned model or model files
- Training/configuration files when useful
- Dataset or dataset description (when shareable)
- Notes about the task and training setup
- Evaluation results or sample outputs
- Links to the original pretrained model

### Models

| Model | Purpose | Fine-Tuning Environment | Status |
|---|---|---|---|
| **T5 — Forensics AI** | Fine-tuned for the Forensics AI project | Google Colab | Completed |

More models and experiments will be added here as I fine-tune them.

> **Note:** Model files may be large. When the full model cannot reasonably be stored directly in Git, the repository can contain the documentation/configuration and a link to the hosted model artifact.

## What I Normally Fine-Tune With

My fine-tuning experiments generally work with task-specific text such as:

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

The `LLM Fine-Tune Learning/` folder contains the existing standalone HTML learning notes.

These files are intended for people who want to learn how LLM fine-tuning works. They can be downloaded as `.html` files and opened directly in a browser — no build system is required.

Current learning notes:

1. **LLM Fine-Tuning — Complete Master Guide**
2. **Fine-tuning LLMs — 20 Min Master Guide**

These learning files are complementary to the main purpose of this repository: **showcasing my own fine-tuned models**.

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
    └── T5-Forensics-AI/
        └── README.md
```

## Fine-Tuning Philosophy

I use fine-tuning when the goal is to make a pretrained model better suited to a **specific task, domain, format, or behavior**.

The choice of fine-tuning method depends on the project. Depending on the model and resources available, this can include approaches such as:

- Full fine-tuning
- Parameter-Efficient Fine-Tuning (PEFT)
- LoRA
- Instruction tuning
- Supervised fine-tuning (SFT)

I also consider alternatives such as **prompt engineering** and **RAG** when they are a better fit for the problem.

## About

**Sudipta Roy**  
B.Tech CSE (AI & ML)

Interested in **AI/ML, LLM engineering, RAG, fine-tuning, and practical AI systems**.

---

### Repository intent

**Primary:** Showcase my personally fine-tuned LLMs and experiments.  
**Secondary:** Provide standalone learning material for understanding LLM fine-tuning.
