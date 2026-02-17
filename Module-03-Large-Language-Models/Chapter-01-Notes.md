# Week 3 – Session 1  
## LLM Concepts, RAG, Agents & Evaluation

### Overview

In this session, I understood how Large Language Models actually work and how they are used in real-world applications. The discussion covered core concepts like tokens and self-attention, and then moved to practical systems like embeddings, RAG, agents, and evaluation.

---

## 1. API Keys & Proxy

- API keys are required to access LLM APIs.
- They must be stored securely using environment variables.
- Proxies help manage cost and control usage.

This made it clear how backend systems safely interact with AI models.

---

## 2. How LLMs Work

- Text is broken into tokens.
- Tokens are converted into vectors.
- The model predicts the next token based on probability.
- Transformers use self-attention to understand relationships between words.

Self-attention helps the model understand context within a sentence.

---

## 3. Context Limits

LLMs have a limited context window.  
Long documents must be split into smaller chunks.  
This is why techniques like RAG are needed.

---

## 4. Embeddings & Vector Databases

- Embeddings convert text into numerical vectors.
- Similar texts have similar vectors.
- Used for search, clustering, and similarity matching.
- Stored in vector databases like ChromaDB or LanceDB.

This forms the foundation of semantic search systems.

---

## 5. RAG & Hybrid RAG

RAG (Retrieval Augmented Generation):

- Retrieves relevant document chunks.
- Then uses the LLM to generate answers.
- Reduces hallucinations.

Hybrid RAG combines keyword search + vector search for better results.

---

## 6. Multimodal & Base64

- Base64 encoding is used to send images/audio via APIs.
- Vision models can analyze images and video frames.
- Multimodal models combine text, image, and audio inputs.

AI is no longer limited to text-only systems.

---

## 7. Prompt Engineering

Better prompts = better results.

Key points:
- Be clear and specific.
- Define output format.
- Provide examples.
- Use structured instructions.

---

## 8. Function Calling, Agents & Tools

- Function calling allows LLMs to trigger real functions.
- Agents can plan tasks and use multiple tools.
- Example: travel agent system that collects input and calls APIs.

This connects AI reasoning with real applications.

---

## 9. Evaluation & Testing

- Use structured tests (YAML, assertions).
- Monitor cost and performance.
- Prevent regression issues.
- Important for commercial applications.

---

## Key Takeaway

This session connected theory (transformers, tokens, embeddings) with practical AI systems (RAG, agents, evaluation). It showed how modern AI applications are built using retrieval, structured prompts, tools, and proper testing.
