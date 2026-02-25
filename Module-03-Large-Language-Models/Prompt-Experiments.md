## Prompt Experiments – Week 3

### 1. Basic vs Structured Prompt

Simple Prompt:
"Extract product details."

Result:
- Unstructured output

Structured Prompt:
- Clearly defined fields
- Requested JSON format

Result:
- More consistent and reliable

Learning:
Clear structure improves output quality.

---

### 2. Role-Based Prompting

Used roles:
- developer
- user
- assistant

Observation:
Model remembers only what is sent in `messages`.

Learning:
Conversation memory must be explicitly provided.

---

### 3. RAG vs No RAG

Without RAG:
- Hallucinated answers

With RAG:
- Retrieved top relevant chunks
- More accurate responses

Learning:
RAG improves factual grounding.

---

### 4. Cosine Similarity Tuning

- Ranked chunks using cosine similarity.
- Top 3–5 chunks worked best.

Learning:
Too much context reduces quality.

---

### 5. Multimodal Prompting

- Sent Base64 image + text instruction.
- Extracted structured product data.

Learning:
Multimodal models combine visual + textual reasoning.

---

### 6. Function Calling

- Defined tool schema.
- Received structured JSON output.

Learning:
Function calling enables reliable machine-readable responses.

---

### Final Insight

Good prompts improve:
- Accuracy
- Structure
- Cost efficiency
- Production readiness.
