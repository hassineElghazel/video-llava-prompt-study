# video-llava-prompt-study
A research project evaluating how prompt engineering influences the prediction accuracy of the Video-LLaVA model on video question answering tasks.

# 🎥 Video-LLaVA Prompt Engineering Study

This repository investigates how **prompt design** affects the performance of the [Video-LLaVA](https://huggingface.co/LanguageBind/Video-LLaVA-7B-hf) model in the context of **video-based question answering (VideoQA)**.

We evaluate different prompt strategies—ranging from generic instructions to task-specific augmentations—and compare their impact on generated answers using standard metrics such as **BLEU**, **ROUGE**, and **BERTScore**.

## 🧪 Goals

- Evaluate baseline vs engineered prompts on short-form video segments.
- Quantify improvement in answer quality using multiple language metrics.
- Identify over-constrained prompts that harm lexical match but improve semantics.
- Build a reproducible batch-processing pipeline in Google Colab.

## 📂 Contents

- `notebooks/`: Colab notebooks for running the evaluation.
- `prompt_utils.py`: Dynamic prompt generation based on question intent.
- `process_batch.py`: Batch inference script for evaluation.
- `metrics.py`: BLEU, ROUGE, and BERTScore calculation.
- `results/`: Example outputs and evaluation logs.

## 🔧 Model Used

- `LanguageBind/Video-LLaVA-7B-hf` from Hugging Face.

## 📊 Evaluation Metrics

- BLEU-1 to BLEU-4
- ROUGE-1, ROUGE-L
- BERTScore (Precision, Recall, F1)

## 🧠 Prompt Engineering Logic

Prompt instructions are automatically adapted based on:
- Question type (`how many`, `what color`, `where did I`, etc.)
- Semantic intent (counting, yes/no, location, object interaction)
- Desired output constraints (length, specificity)

## 🚀 Getting Started

Run everything from `main.ipynb` in Google Colab or use `process_batch.py` to run on a local machine with a compatible GPU.

## 📜 License

MIT License
