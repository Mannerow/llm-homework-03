# llm-homework-03

## 📄 Overview

This project demonstrates the use of `Elasticsearch` for vector search tasks. The provided Jupyter Notebook, `vector_search.ipynb`, loads an embeddings model using `sentence-transformers`, creates embeddings for the combined question and answer field, and creates a Vector Search Engine to search for user questions in FAQ documents. We evaluate the search engine results using hit rate and mean reciprocal rank (MRR). Finally, evaluate Elasticsearch, which is more efficient as it uses approximate techniques rather than computing similarity with all the vectors, producing identical results. 

## 🚀 Installation

To set up the project, follow these steps:

```bash
pip install pipenv
pipenv install
```

Then, select the pipenv environment in the Jupyter kernel.

## 🛠 Run Elasticsearch

To run the Elasticsearch Docker container, use the following command:

```bash
docker run -it \
    --rm \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3
```