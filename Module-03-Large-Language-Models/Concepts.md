## Concepts – Week 3

### 1. LLM Basics
- Text is split into tokens.
- Tokens are converted into vectors.
- The model predicts the next token using probability.
- Self-attention captures context between words.

LLMs have limited context windows, so long documents must be chunked.

---

### 2. API Security
- API keys must be stored in environment variables.
- Never hardcode keys.
- Use proxies (AI Pipe) for cost control.
- Access keys securely using `os.getenv()`.

---

### 3. Embeddings & Vector Search
- Embeddings convert text into numerical vectors.
- Similar meaning → similar vectors.
- Cosine similarity measures closeness.
- Store embeddings in a vector database.
- Workflow: Generate → Store → Compare → Retrieve.

---

### 4. RAG (Retrieval Augmented Generation)
- Convert query into embedding.
- Retrieve top relevant chunks.
- Send retrieved context to LLM.
- Generate grounded answer.

RAG reduces hallucination and improves factual accuracy.

---

### 5. Multimodal & Base64
- Images are encoded in Base64 for API requests.
- Multimodal models process text + image together.

---

### 6. Prompt Engineering
- Be clear and specific.
- Define output format.
- Provide examples.
- Structured prompts improve reliability.

---

### 7. Function Calling & Agents
- Define tool schema.
- Model returns structured JSON.
- Backend executes function.
- Agents combine reasoning + tools.

---

### 8. Evaluation & Deployment
- Use structured tests.
- Monitor cost and performance.
- Fix configuration issues (ports, env variables).
- Most deployment issues are setup-related.

---

### Summary

Modern AI systems combine:
LLMs + Embeddings + Vector Search + RAG + Prompt Engineering + Tools + Secure Deployment.
