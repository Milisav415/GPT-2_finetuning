# GPT-2 Fine-Tuning Project

This repository showcases how to fine-tune a GPT-2 model using a subset of Wikipedia data as an example. The code uses the Hugging Face Transformers library and the `datasets` library, and is configured to run on an environment with limited VRAM (such as an RTX 3050 Ti).

## Project Overview

The main goal of this project is to demonstrate the steps involved in preparing a dataset, splitting it into train and validation sets, tokenizing it according to GPT-2 requirements, and then running the fine-tuning process. The project also covers storing and reloading tokenized datasets to save time and disk space.

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<YourUsername>/GPT-2_finetuning.git
   cd GPT-2_finetuning
