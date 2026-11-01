# MP-G09 — Contract Clause Autocompletion Using GPT-2

An educational prototype that continues pretraining GPT-2 Small on a subset of CUAD contract documents and generates possible continuations for user-entered contract-clause prefixes.

## Project details

- **Project ID:** MP-G09
- **Course:** Learn from Scratch: Large Language Models (ISE23704C)
- **Model:** GPT-2 Small (124M parameters)
- **Dataset:** Contract Understanding Atticus Dataset (CUAD)
- **Tokenizer:** GPT-2 BPE tokenizer (`tiktoken`)
- **Training approach:** Continued pretraining with next-token prediction
- **Data loading:** Custom sliding-window `Dataset` and `DataLoader`
- **Interface:** Gradio
- **Decoding options:** Greedy, Temperature sampling, and Top-k sampling

## Main notebook

`MP-G09_Contract_Clause_Autocompletion_CORRECTED.ipynb`

Open the notebook in Google Colab and run the cells from top to bottom. The notebook installs its dependencies and downloads the official textbook companion code and the CUAD data as part of its workflow.

## How to run

1. Open the notebook in Google Colab.
2. Select a runtime suitable for the available compute. The notebook uses PyTorch and may run slowly on CPU.
3. Run the cells in order to install dependencies, download/process the CUAD subset, tokenize the text, and create the data loaders.
4. Run the model initialization and pretrained-weight loading cells.
5. Run the evaluation and continued-pretraining cells.
6. Run the decoding and checkpoint cells.
7. Run the Gradio application cell.
8. Enter a contract-clause prefix, choose a decoding strategy, and submit to view the generated continuation.

## Textbook companion code

The project imports the GPT model implementation and GPT-2 weight-loading utilities from the official companion repository:

https://github.com/rasbt/LLMs-from-scratch

## Dataset

Contract Understanding Atticus Dataset (CUAD):

- Project website: https://www.atticusprojectai.org/cuad/
- Hugging Face dataset: https://huggingface.co/datasets/theatticusproject/cuad

The notebook processes a limited subset of contract PDFs for this educational project. Refer to the notebook outputs for the actual sample count and preprocessing details from the run.

## Important limitations

- This is an educational prototype, not a legal advice system.
- Generated text may be repetitive, irrelevant, or legally inaccurate.
- All generated legal text must be reviewed by a qualified legal professional.
- Training uses a limited dataset subset and a short training run; results should not be treated as production-quality legal drafting.

## AI assistance

AI coding assistance was used to help plan, debug, and organize parts of the implementation. The project code and outputs were reviewed and tested by the student.

## Model weights

Model checkpoint/weight files are intentionally not included in this repository, in accordance with the project submission instructions.
