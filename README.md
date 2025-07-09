# Researcher Recommendation System based on arXiv Publications

This project builds an intelligent recommendation system to suggest **relevant researchers** for a given research query, based on semantic understanding of their publication history. It uses **Natural Language Processing (NLP)** techniques and **sentence embeddings** to compare user queries with author profiles.

---

## Objective

Given a research topic or query (e.g., `"deep learning for healthcare"`), the system returns the top N researchers whose past publications are most semantically similar.

---

## How The Code Works

1. **Load & Preprocess Dataset**
2. **Author Profiling**: Merge publication content per author
3. **Sentence Embedding**: Use `SentenceTransformer` to vectorize author profiles
4. **Query Matching**: Compute cosine similarity between user query and author embeddings
5. **Recommendation Output**: Top-N researchers + relevant publication titles

---

## Two Recommendation Modes

| Notebook                            | Description                                                  |
|-------------------------------------|--------------------------------------------------------------|
| `first_author_recommendation.ipynb` | Considers only the first author of each paper               |
| `all_authors_recommendation.ipynb`  | Explodes all authors to capture collaboration contribution   |

---

## Example Queries

Try one of these in the notebook:
- `"Deep learning for medical diagnosis"`
- `"Graph neural networks for social networks"`
- `"Reinforcement learning for robotics"`
- `"Language models for text summarization"`

---

## Dataset

This project uses the **[arXiv Scientific Research Papers Dataset](https://www.kaggle.com/datasets/Cornell-University/arxiv)** 

---

## Installation

Create a virtual environment and install dependencies:

```bash
pip install -r requirements.txt
```

---

## Output

Each recommendation includes:
- `author`: Name of the researcher
- `total_pub`: Total number of publications
- `relevant_pub`: Number of publications relevant to the query
- `relevance_ratio`: Ratio of relevant publications
- `matched_titles`: List of matching publication titles