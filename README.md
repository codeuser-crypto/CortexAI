# CortexAI

AI Assistant powered by a custom-built Vector Database, HNSW Semantic Search, Retrieval Augmented Generation (RAG) and Local LLMs using Ollama.

CortexAI is an end to end AI system built from scratch in C++ that combines semantic search, document retrieval, and local large language models to answer questions from user-provided knowledge sources. The project demonstrates how modern AI systems such as ChatGPT, Claude, Perplexity, and enterprise RAG platforms work under the hood.

## 🚀 Features

### Vector Database from Scratch
- Custom Vector Database implemented in C++
- Supports high-dimensional embeddings
- Fast similarity search over semantic vectors

### Multiple Search Algorithms
- HNSW (Hierarchical Navigable Small World)
- KD Tree Search
- Brute Force Search

### Distance Metrics
- Cosine Similarity
- Euclidean Distance
- Manhattan Distance

### Retrieval Augmented Generation (RAG)
- Document chunking and storage
- Semantic retrieval using HNSW
- Context aware question answering

### Local AI Models
- Ollama Integration
- nomic embed text for embeddings
- llama3.2 for response generation
- Fully local execution without cloud APIs

### Interactive Web Interface
- Search interface
- Document management
- AI chat assistant
- PCA visualization of vector space
- Benchmark comparison dashboard

# 🏗 System Architecture

User Query
     │
     ▼
Embedding Model (nomic embed text)
     │
     ▼
Vector Database (HNSW)
     │
     ▼
Semantic Retrieval
     │
     ▼
Relevant Context
     │
     ▼
LLM (llama3.2)
     │
     ▼
Generated Response

# 📌 Core Components

## HNSW Search Engine

Hierarchical Navigable Small World (HNSW) is a graph based Approximate Nearest Neighbor algorithm used in modern vector databases such as:

- Pinecone
- Weaviate
- Chroma
- Milvus

Benefits:
- Near O(log N) search complexity
- High recall
- Production grade semantic retrieval

## KD Tree

A classical exact nearest neighbor search structure.

Benefits:
- Fast in low dimensional spaces
- Efficient pruning

Limitations:
- Performance degrades in high dimensions

## Brute Force Search

Compares every vector with the query vector.

Benefits:
- 100% accurate
- Useful as a benchmark baseline

Limitations:
- O(N) complexity

# Retrieval Augmented Generation (RAG)

CortexAI follows a complete RAG workflow:

1. User uploads documents
2. Documents are split into chunks
3. Chunks are converted into embeddings
4. Embeddings are indexed using HNSW
5. User asks a question
6. Relevant chunks are retrieved
7. Retrieved context is sent to the LLM
8. LLM generates an answer grounded in user documents

This reduces hallucinations and enables knowledge-specific question answering.

# Supported Features

Feature :-
1. HNSW Search
2. KD-Tree Search
3. Brute Force Search
4. REST API
5. RAG Pipeline
6. Ollama Integration
7. Document Embeddings
8. Semantic Search
9. PCA Visualization
10. Local LLM Chat

---

# Technologies Used

### Backend
- C++
- STL
- REST APIs
- Multi-threading

### AI
- Ollama
- llama3.2
- nomic-embed-text

### Search & Retrieval
- HNSW
- KD-Tree
- Vector Similarity Search

### Frontend
- HTML
- CSS
- JavaScript


# 📂 Project Structure

CortexAI/
│
├── .gitignore
├── README.md
├── httplib.h
├── index.html
└── main.cpp

# 🚀 Installation

## Prerequisites

Install:

- Git
- MSYS2
- GCC Compiler
- Ollama

### Required Models

ollama pull nomic-embed-text
ollama pull llama3.2

## Compile
g++ -std=c++17 -O2 main.cpp -o cortexai -lws2_32

## Run
./cortexai

Open:

http://localhost:8080

# 🔍 Example Workflow

### Insert Documents
Operating Systems Notes
Database Notes
Machine Learning Notes
Research Papers

The system retrieves relevant document chunks and generates answers using the local LLM.

# 📈 Performance Goals

- Fast semantic retrieval
- Scalable vector indexing
- Low-latency search
- Fully local AI execution
- Educational implementation of modern AI systems

# 🎯 Learning Objectives

This project was built to understand and implement the technologies behind:

- ChatGPT
- Claude
- Perplexity
- Pinecone
- Weaviate
- Chroma
- Enterprise AI Search Systems

Rather than relying on existing frameworks, CortexAI implements the underlying concepts from scratch for educational and research purposes.

# 🔮 Future Enhancements

- Hybrid Search (Keyword + Vector)
- Multi-Agent Architecture
- PDF Parsing
- Image Embeddings
- Voice Assistant
- Distributed Vector Storage
- GPU Acceleration
- Fine-Tuned Local Models
- Knowledge Graph Integration
