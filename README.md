# LLM Judge: Detecting Hallucinations in Language Models

This project demonstrates how to fine-tune and evaluate a Mistral AI language model to detect factual inconsistencies and hallucinations in text summaries.

## Overview

The project consists of two main parts:
1. Data preparation (`01_prepare_data.ipynb`)
2. Model fine-tuning and evaluation (`02_finetune_and_eval.ipynb`)

## Features

- Prepares datasets from Factual Inconsistency Benchmark (FIB) and USB
- Fine-tunes a Mistral 7B model for hallucination detection
- Evaluates model performance using accuracy, F1 score, precision, and recall
- Integrates with Weights & Biases for experiment tracking

## Requirements

- Python 3.11+
- Libraries: mistralai, pandas, weave, scikit-learn, datasets

## Usage

1. Prepare the data:
   - Run `01_prepare_data.ipynb` to process and format the datasets

2. Fine-tune and evaluate the model:
   - Run `02_finetune_and_eval.ipynb` to:
     - Evaluate baseline Mistral models (7B and Large)
     - Fine-tune a Mistral 7B model
     - Evaluate the fine-tuned model

## Key Components

- `MistralModel`: Wrapper for Mistral AI API calls
- `Evaluation`: Custom evaluation pipeline using Weave
- `BinaryMetrics`: Scorer for binary classification metrics

## Results

The notebook demonstrates improvements in hallucination detection after fine-tuning, with detailed metrics and comparisons between model versions.

## Notes

- Ensure you have the necessary API keys for Mistral AI and Weights & Biases
- Adjust `NUM_SAMPLES` in the evaluation notebook to control the number of examples used

For more details, refer to the individual notebooks and comments within the code.