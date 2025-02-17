# fast-news-rec
A lightweight and efficient news article recommendation API built with FastAPI, FAISS, and Sentence Transformers. It enables quick retrieval of semantically similar news articles from a dataset using state-of-the-art embeddings and nearest-neighbor search.

## Features
- **FastAPI** for serving recommendations via a RESTful API
- **Sentence Transformers (MiniLM-BERT)** for generating high-quality text embeddings
- **FAISS (Facebook AI Similarity Search)** for efficient similarity search
- **AG News Dataset** as the default corpus for article recommendations
- **Top-k Similar Article Retrieval** based on semantic similarity

## Installation

Ensure you have Python 3.8+ installed.

`pip install -r requirements.txt`

Clone the repository:

```
git clone https://github.com/yourusername/FastNewsRec.git
cd FastNewsRec
```

## Implementation Details

1. Data Processing: Loads the AG News dataset and extracts a subset of 1000 news articles.
2. Text Embeddings: Uses the all-MiniLM-L6-v2 model from Sentence Transformers to generate embeddings.
3. Efficient Search: FAISS is used to create an L2-based index for fast nearest-neighbor retrieval.
4. API Endpoint: Accepts an input article and returns the top-k most similar articles based on FAISS search.

## Usage

1. Start the API Server

Run the following command to start the FastAPI service:

`uvicorn app:app --host 0.0.0.0 --port 8000`

2. API Endpoint

Recommend Similar News Articles
- Endpoint: POST /recommend
- Request Body:

```
{
  "article_text": "Sample news article text here...",
  "top_k": 5
}
```

- Response Example:

```
{
  "input_article": "Sample news article text here...",
  "recommendations": [
    "Recommended article 1",
    "Recommended article 2",
    "Recommended article 3",
    "Recommended article 4",
    "Recommended article 5"
  ]
}
```

## Future Enhancements

- Expand dataset coverage for better recommendations.
- Implement additional embedding models for comparison.
- Deploy as a cloud-based microservice.

## License

This project is licensed under the MIT License.
