## Week 3 – Session 4  
## OpenAI API, Embeddings, RAG & Multimodal

In this session, I worked hands-on with the OpenAI API, implemented embeddings, built a small vector database, handled multimodal (image + text) inputs, and used function calling for structured data extraction. This session was highly practical and helped me understand how real-world AI systems are built.

---

### OpenAI API Fundamentals

Explored different models, pricing, and endpoints.

Understood the structure of an API call:

- URL  
- Headers  
- Authorization (Bearer API Key)  
- JSON body  
- POST request  

Used `httpx` to send API requests and converted responses using `.json()` to extract model outputs.

---

### Chat Completion and Roles

Learned how conversation memory works using roles:

- `developer` – system instruction  
- `user` – query  
- `assistant` – model response  

Built a chatbot by passing conversation history inside the `messages` array. Understood that LLMs only remember what we send in the request.

---

### Environment Setup and Security

Stored the API key in environment variables instead of hardcoding it.  
Accessed it securely using `os.getenv()`.

This ensures better security and cleaner project structure.

---

### Base64 Encoding and Image Handling

Learned how to convert an image into Base64 format:

Image → Binary → Base64 string  

This allows sending images in multimodal API requests. Also understood the decoding process.

---

### Word Embeddings and Semantic Meaning

Understood how text is converted into numerical vectors (embeddings).  
Similar words have closer vector representations in embedding space.

This is the foundation for semantic search systems.

---

### Distance and Cosine Similarity

Implemented:

- Euclidean distance  
- Cosine similarity  

Used cosine similarity to measure semantic closeness between vectors and retrieve the most relevant result.

---

### Mini Vector Database and RAG Concept

Created a small vector database storing:

- Text  
- Corresponding embeddings  

Compared query embeddings with stored vectors and retrieved the most similar entry.

This demonstrates the core idea behind Retrieval Augmented Generation (RAG).

---

### Multimodal Inputs (Text + Image)

Combined text instructions and Base64 encoded images in a single API request.  
Extracted product details directly from images.

This showed how multimodal models process both text and visual data together.

---

### Function Calling and Tools

Defined a function schema to extract structured data such as:

- Manufacturing date (MFD)  
- Expiry date (EXP)  
- Cost  
- Batch number  

Passed `tools` in the API request and received structured JSON output.  
This enables reliable machine-readable AI responses.

---

### Final Implementation – Product Q&A

Built a mini project that:

- Takes a product image  
- Converts it to Base64  
- Sends it to the API  
- Extracts structured product information  

This combined API calls, embeddings, multimodal input, and function calling into one complete pipeline.

---

### Key Learnings

- LLM memory depends on the messages provided.  
- Embeddings represent semantic meaning numerically.  
- Cosine similarity powers semantic search.  
- RAG combines retrieval with generation.  
- Function calling enables structured AI outputs.  
- Multimodal models process text and images together.

---

### Outcome

By the end of this session, I am able to:

- Make secure OpenAI API calls  
- Build a chatbot with conversation history  
- Work with embeddings and similarity search  
- Understand RAG fundamentals  
- Perform image-to-text extraction  
- Use function calling for structured outputs  
