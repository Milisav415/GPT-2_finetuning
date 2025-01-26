# GPT-2 Fine-Tuning Project

This repository demonstrates how to fine-tune a GPT-2 model on a custom text dataset (Wikipedia subset). The code uses [Hugging Face Transformers](https://github.com/huggingface/transformers) and the `datasets` library.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Setup & Installation](#setup--installation)
3. [Data Preparation](#data-preparation)
4. [Tokenization](#tokenization)
5. [Train & Validation Split](#train--validation-split)
6. [Fine-Tuning GPT-2](#fine-tuning-gpt-2)
7. [Evaluation & Testing](#evaluation--testing)
8. [Saving & Loading Datasets](#saving--loading-datasets)
9. [Troubleshooting](#troubleshooting)
10. [License](#license)

---

## Project Overview
The goal is to fine-tune GPT-2 on a smaller subset of Wikipedia data (or any custom dataset) while managing limited GPU resources (e.g., RTX 3050 Ti with 4GB VRAM).

Key features:
- Data splitting and tokenization
- Causal language modeling with GPT-2
- Low VRAM optimization
- Saving and loading tokenized datasets
