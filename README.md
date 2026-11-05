# Week 12 – RAG Data Indexing using FAISS

## Overview
This experiment demonstrates the data indexing stage of Retrieval-Augmented Generation (RAG) using LangChain, Hugging Face embeddings, and FAISS. A sample climate change document is divided into smaller chunks, converted into vector embeddings, and stored in a searchable vector database.

## Objective
To understand document chunking, embedding generation, vector storage, and similarity-based retrieval as fundamental components of a RAG pipeline.

## Technologies Used
- Python
- LangChain
- FAISS
- Hugging Face Embeddings
- `all-MiniLM-L6-v2`

## Experiment Description

### 1. Sample Document
The experiment uses a sample document containing information about climate change, including:
- Rising global temperatures.
- Changes in weather patterns.
- Melting glaciers and rising sea levels.
- Extreme weather events.
- Effects on agriculture, water resources, and human health.
- Renewable energy and greenhouse gas emission reduction.

### 2. Document Chunking
`RecursiveCharacterTextSplitter` divides the document into smaller chunks using:
- Chunk size: `300`
- Chunk overlap: `30`

### 3. Embedding Generation
`HuggingFaceEmbeddings` uses the `all-MiniLM-L6-v2` model to convert the document chunks into numerical vector representations.

### 4. FAISS Vector Store
`FAISS.from_documents()` creates a vector store containing the document chunks and their embeddings.

### 5. Similarity Search
The experiment searches the vector database using the query:

"What are the effects of climate change?"

It retrieves the top two relevant chunks using `similarity_search_with_relevance_scores()`.

## Model Configuration
- Embedding model: `all-MiniLM-L6-v2`
- Chunk size: `300`
- Chunk overlap: `30`
- Number of retrieved chunks: `2`

## How to Run
1. Open the Python file in Google Colab or a compatible Python environment.
2. Install the required dependencies.
3. Execute the experiment.
4. Allow the embedding model to download when it is first used.
5. Review the number of chunks generated.
6. Examine the top two retrieved chunks and their relevance scores.

## Expected Learning Outcome
- Understand the fundamentals of RAG data indexing.
- Learn how to split documents into manageable chunks.
- Understand how embeddings represent text numerically.
- Learn how FAISS stores and searches vector embeddings.
- Understand similarity-based document retrieval.

## Output
The experiment displays:
1. Number of document chunks.
2. The search query.
3. The top two retrieved chunks.
4. Their corresponding relevance scores.

Save an output screenshot in the `outputs/` directory.

## Conclusion
This experiment demonstrates how raw text can be transformed into searchable vector representations. Document chunking, embedding generation, and FAISS similarity search form an important foundation for building Retrieval-Augmented Generation systems.