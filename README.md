# fast-news-rec
A lightweight and efficient news article recommendation API built with FastAPI, FAISS, and Sentence Transformers. It enables quick retrieval of semantically similar news articles from a dataset using state-of-the-art embeddings and nearest-neighbor search.

## Features
- **FastAPI** for serving recommendations via a RESTful API
- **Sentence Transformers (MiniLM-BERT)** for generating high-quality text embeddings
- **FAISS (Facebook AI Similarity Search)** for efficient similarity search
- **AG News Dataset** as the default corpus for article recommendations
- **Top-k Similar Article Retrieval** based on semantic similarity

## Installation

### Requirements
Ensure you have Python 3.8+ installed.

Clone the repository:
```bash
git clone https://github.com/yourusername/FastNewsRec.git
cd FastNewsRec
