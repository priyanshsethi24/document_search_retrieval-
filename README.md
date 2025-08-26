# document_search_retrieval-
Developed a scalable retrieval system that benchmarks 12+ embedding models for both accuracy and latency. The system integrates a MongoDB backend for efficient embedding storage, enabling OCR-powered search workflows and flexible configurations tailored for large-scale document automation and information retrieval.

## 1) Overview

This repository contains a document search and extraction system that integrates:

Semantic Document Search – Benchmarks multiple top-performing embedding models (e.g., bge, nomic, sbert, mixedbread) for query-based retrieval on PDF documents.

Entity & Statement Extraction – Performs entity extraction, statement reconciliation, and table detection (both structured and unstructured), generating bounding boxes for tabular data and non-table entities.

OCR + Embeddings + MongoDB – Uses OCR for text/image extraction, embeddings for semantic search, and MongoDB utilities for storage and retrieval.

The goal is to enable scalable information retrieval and automation pipelines with high retrieval accuracy and efficient query response times.


## 2) Features

a) Semantic Search

i) Benchmarks 12+ embedding models (bge, e5, gte, nomic, sbert, mixedbread)
ii) Evaluates accuracy vs. latency trade-offs
iii) Achieved up to 100% retrieval accuracy with bge-m3 and nomic-v1 models

b) Database Integration
MongoDB support for storing embeddings & documents


## 3) Installation & Setup

1. Clone the repository:

git clone <repo-url>
cd <repo-name>


2. Install dependencies:

pip install -r requirements.txt


Place your PDF files inside the pdf_documents/ directory.Run the main pipeline:
python main.py

3. Usage


a) Modify and run queries in Question_Queries.txt to test retrieval performance.
Results will be stored inside the results/ directory.

b) Mongo utilities (mongo/mongo_utils.py) allow storing & retrieving embeddings in MongoDB.

3. Future Improvements

1) Add multi-modal search (text + image embeddings).

2) Improve table structure detection with advanced vision models.

3) Optimize latency for large-scale document search.
