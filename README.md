# RAG Systems

A Retrieval-Augmented Generation pipeline that augments Llama 3.1 8B with BBC News headlines from 2024 -- information beyond the model's training cutoff.

## Pipeline

1. Encode query with sentence-transformers (BAAI/bge-base-en-v1.5)
2. Compute cosine similarity against pre-embedded BBC News documents
3. Retrieve top-k relevant articles
4. Format into a structured prompt with retrieved context
5. Call Meta-Llama-3.1-8B-Instruct-Turbo via Together.ai API

## Features

- Side-by-side comparison widget: LLM responses with and without RAG
- Pre-computed embeddings (joblib) for fast retrieval
- Custom prompt template system with `{query}` and `{documents}` placeholders

## Tech Stack

Python, sentence-transformers, scikit-learn, pandas, Together.ai API, ipywidgets
