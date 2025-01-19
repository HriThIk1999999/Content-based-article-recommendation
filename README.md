# Real-Time Article Search with Content-Based Filtering

This project, Real-Time Article Search with Content-Based Filtering, demonstrates an end-to-end pipeline for scraping, processing, and querying news articles using state-of-the-art AI techniques. The solution combines web scraping, data processing, embeddings, and Large Language Models (LLMs) to recommend articles in real-time. Below is a detailed description of the project and its implementation.

# Features

Web Scraping: Retrieves real-time articles from The Guardian using their API.

Data Preprocessing: Cleans and processes raw article content by parsing HTML tags, removing stopwords, and extracting metadata.

Embeddings: Converts article text into embeddings using Sentence Transformers (e.g., MiniLM).

Large Language Models (LLMs): Utilizes LLaMA 2 for language understanding and enhanced recommendations.

Query Engine: Implements a content-based filtering system to recommend articles based on user queries.

Technologies: Built using LlamaIndex, RAG (Retrieval-Augmented Generation), and LangChain.

# Workflow

1. Web Scraping
Libraries Used: beautifulsoup4, requests
Description:
Fetches articles using The Guardian’s API with an API key.
Extracts the content, metadata (title, author, publication date), and categories.

2. Data Processing
Steps:
Parse the raw HTML content and remove unwanted tags.
Tokenize text and remove stopwords using NLTK or SpaCy.
Extract and store metadata for better indexing and search results.

3. Embeddings
Library Used: Sentence Transformers (sentence-transformers)
Description:
Generate dense vector representations of articles.
Embeddings are stored in a vector index for efficient similarity searches

4. Large Language Models
LLM Used: LLaMA 2
Description:
Enhances article recommendations with better language understanding and contextual relevance.
Works alongside embeddings for hybrid search capabilities.

5. Vector Store Index
Technology: LlamaIndex
Description:
Stores embeddings and metadata in a searchable vector database.
Efficiently retrieves relevant articles based on user queries.

6. Query Engine
Framework: LangChain + RAG
Description:
Combines retrieval-augmented generation with content-based filtering.
Delivers article recommendations that match user input.

# Tools and Libraries
Web Scraping: beautifulsoup4, requests
Data Processing: nltk, spacy
Embeddings: sentence-transformers
LLM Integration: LLaMA 2
Indexing: llama-index
Query Engine: langchain


# Folder Structure
real-time-article-search/
├── data/                  # Stores raw and processed article data
├── embeddings/           # Embedding vectors
├── models/               # Pre-trained LLaMA 2 models
├── utils/                # Utility scripts for data processing
├── main.py               # Entry point for the pipeline
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
