# Week 3 – Session 2  
## Embeddings, Vector Search & RAG Implementation

In this session, I implemented a complete embedding-based retrieval workflow for Project 1.

### Embeddings

- Generated embeddings using OpenAI API via HTTPX (async requests).
- Used `text-embedding-3-small` for cost-effective vector generation.
- Stored API keys securely using environment variables (`.bashrc`) and AI Pipe proxy.
- Handled JSON parsing safely and added request timeouts.
- Computed cosine similarity using NumPy:
  - dot product
  - vector norm
  - normalized similarity score

### Multimodal Embeddings

- Generated embeddings for both text and images (Nomic models).
- Compared text ↔ image embeddings for cross-modal similarity.
- Understood how multimodal retrieval works in practice.

### Chunking Strategy

- Split large documents into token-safe chunks.
- Stored chunks in `chunks.json` with:
  - `id`
  - `source`
  - `text`
  - `embedding`
- Avoided repeated API calls by precomputing embeddings.

### Retrieval (ask_question.py)

- Converted user query into embedding.
- Compared against stored chunk embeddings.
- Ranked using cosine similarity.
- Retrieved top-5 most relevant chunks.
- This forms the retrieval stage of RAG.

### Optimization & Cost Awareness

- Used smaller embedding models for efficiency.
- Cached embeddings instead of recomputing.
- Ensured async execution for better performance.

### Key Takeaway

This session helped me build a practical embedding pipeline:
Generate → Store → Compare → Retrieve.

It strengthened my understanding of semantic search, vector similarity, multimodal embeddings, and cost-aware RAG implementation.
