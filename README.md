# llms_practice

This repository contains hands-on notebook examples for working with transformer models, question answering, text classification, and local Ollama usage.

## Environment

Recommended Python environment:

- Python 3.10.20
- Conda environment

Create the environment with:

```bash
conda create -n llms_practice python=3.10.20 -y
conda activate llms_practice
```

Install the key packages used by the notebooks:

```bash
pip install transformers torch datasets evaluate cleantext emoji pandas numpy scikit-learn matplotlib seaborn openai langchain langchain-core langchain-community langchain-text-splitters faiss-cpu
```

> Notes:
>
> - The notebooks use `transformers`, `torch`, `datasets`, and several LangChain/Ollama packages.
> - `faiss-cpu` is recommended for local vector search in `ollama_models.ipynb`.

## Repository Contents

- `hugging_face_transformers.ipynb`
  - Demonstrates Hugging Face Transformers usage.
  - Covers inference pipelines, tokenizers, and saving/loading models.
  - Shows interoperability with PyTorch.

- `bert_question_and_answer.ipynb`
  - Loads a BERT question-answering model and tokenizer.
  - Computes embeddings and interprets model output.
  - Includes a FAQ-style question answering workflow.

- `xlnet_text_classification.ipynb`
  - Preprocesses and cleans text data for emotion classification.
  - Creates embeddings and fine-tunes an XLNet classification model.
  - Evaluates model performance on validation/test splits.
  - Uses data files from the `data/` folder:
    - `data/emotion-labels-train.csv`
    - `data/emotion-labels-val.csv`
    - `data/emotion-labels-test.csv`

- `ollama_models.ipynb`
  - Uses Ollama local model APIs and the OpenAI-compatible client.
  - Shows text generation, output customization, summarization, and a poetic chatbot.
  - Demonstrates LangChain document loading, embeddings, RAG, and memory store setup.

## Data

The repository includes emotion classification data in the `data/` directory.

## Usage

1. Activate the Conda environment.
2. Install the required Python packages.
3. Launch Jupyter Notebook or JupyterLab:

```bash
jupyter notebook
```

4. Open the notebooks in this repository and execute cells interactively.

## Additional Notes

- `ollama_models.ipynb` may require running a local Ollama server and using `api_key="ollama"` with `base_url="http://localhost:11434/v1"`.
- The `.vscode/settings.json` file contains editor theme customizations only.
