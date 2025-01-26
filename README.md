# GPT-2 Fine-Tuning Project

This repository showcases how to fine-tune a GPT-2 model using a subset of Wikipedia data as an example. The code uses the Hugging Face Transformers library and the `datasets` library, and is configured to run on an environment with limited VRAM (such as an RTX 3050 Ti).

# Project Overview

The main goal of this project is to demonstrate the steps involved in preparing a dataset, splitting it into train and validation sets, tokenizing it according to GPT-2 requirements, and then running the fine-tuning process. The project also covers storing and reloading tokenized datasets to save time and disk space.

## Dataset Preparation
In this project, a subset of the Wikipedia dataset is loaded and reduced to keep the size manageable. You can replace this with any other text dataset as needed. The dataset is then tokenized using the GPT-2 tokenizer. During tokenization, the raw text column is replaced with input_ids and attention_mask, which are suitable for GPT-2’s causal language modeling task.

## Training and Validation
A standard 90/10 split is used to separate the training and validation sets. The code then demonstrates how to fine-tune GPT-2 using Hugging Face’s Trainer class and the DataCollatorForLanguageModeling, which configures the model for causal language modeling. Batch sizes and gradient accumulation steps are adjusted to accommodate limited GPU memory.

## Example training script details:
Use per_device_train_batch_size=2 and gradient_accumulation_steps=8 to simulate a larger effective batch size.
Enable mixed precision (fp16=True) to speed up training and reduce memory usage.
Save and evaluate the model every few steps, if desired.
Saving and Loading Tokenized Datasets
The project also demonstrates how to save the tokenized datasets to disk using save_to_disk, and load them later with load_from_disk. This approach allows you to avoid re-tokenizing the entire dataset each time you want to train or experiment with different hyperparameters.

## Future Work
1. Experiment with different subsets of data.
2. Use Git LFS if you need to store large files in the repository (to avoid file size limits).
-Explore optimizations such as gradient checkpointing for even lower VRAM usage.
-Apply these steps to other models or larger datasets once you have the capacity.
-License
-This project is provided under the MIT License. Feel free to modify or distribute as needed.

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<YourUsername>/GPT-2_finetuning.git
   cd GPT-2_finetuning
