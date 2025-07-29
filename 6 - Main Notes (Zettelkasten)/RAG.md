2025-07-29 16:32

### Status: #baby

### Tags: [[machine-learning]]

# What is Retrieval-Augmented Generation

RAG is a GenAI technique where you retrieve relevant data with search-like methods, then use this data to ***augment*** the model's input prompt, thus generating a better response for the user.

So, a context to use RAG is with internal company data - it allows you to feed your model with it's own company data and from there iterate and generate better responses rather than relying solely on a LLM. This avoids hallucination, where the LLM can spit out anything with 0 relevance.


## Tech stack
- Retrieval: vector databases (FAISS, Pinecone, OpenSearch, etc.)
- Generation: Some LLM
- Middleware: AWS Bedrock, LangChain







# References
---

## 📜 Seminal Papers

### 1. [**Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks** (Lewis et al., 2020)](https://arxiv.org/abs/2005.11401)
- **Summary**: Introduced the RAG architecture, combining dense passage retrieval with generative models like BART.
- **Why it matters**: It's the foundational paper that formalized the RAG paradigm.

---

### 2. [**Dense Passage Retrieval for Open-Domain QA** (Karpukhin et al., 2020)](https://arxiv.org/abs/2004.04906)
- **Summary**: Proposes Dense Passage Retrieval (DPR), a dual-encoder model for retrieving documents using semantic similarity.
- **Why it matters**: DPR became the de facto retriever for early RAG systems.

---

### 3. [**REALM: Retrieval-Augmented Language Model Pre-Training** (Guu et al., 2020)](https://arxiv.org/abs/2002.08909)
- **Summary**: Integrates retrieval directly into pretraining, allowing the model to learn to find and use relevant text spans.
- **Why it matters**: Early, influential work from Google on retrieval-aware pretraining.

---

### 4. [**Fusion-in-Decoder (FiD)** (Izacard & Petroni, 2020)](https://arxiv.org/abs/2007.01282)
- **Summary**: Explores how to integrate multiple retrieved passages efficiently using early fusion (before decoding).
- **Why it matters**: Enhanced multi-document conditioning and generation quality.

---

### 5. [**ColBERT: Contextualized Late Interaction over BERT** (Khattab & Zaharia, 2020)](https://arxiv.org/abs/2004.12832)
- **Summary**: Proposes a scalable, late-interaction dense retrieval method.
- **Why it matters**: Allows high-quality retrieval with better latency characteristics.

---

## 🧪 Emerging Research & Techniques

### 6. [**Self-RAG** (Asai et al., 2023)](https://arxiv.org/abs/2307.06981)
- **Summary**: The model iteratively refines its own queries to improve retrieval and final answers.
- **Why it matters**: Bridges retrieval and generation quality in a self-improving loop.

### 7. [**InstructRAG** (Liu et al., 2023)](https://arxiv.org/abs/2310.12731)
- **Summary**: Enhances RAG pipelines with instruction-following LLMs to better structure retrieval and prompt engineering.
- **Why it matters**: Improves real-world performance by making the pipeline more modular and controllable.

---

## 🧰 Tools & Frameworks

- [**LangChain**](https://www.langchain.com)  
  Orchestration framework for building LLM apps with RAG, agents, tools, and memory.

- [**LlamaIndex (GPT Index)**](https://docs.llamaindex.ai)  
  Framework for RAG pipelines focused on document loaders, vector stores, and query routing.

- [**OpenAI: RAG vs Fine-Tuning Blog**](https://openai.com/blog/fine-tuning-vs-rag)  
  Explains when to use RAG versus model fine-tuning — practical guidance from OpenAI.

---

## 📌 Related Concepts

- **Vector Databases**: FAISS, Pinecone, Weaviate, Qdrant, OpenSearch
- **Prompt Engineering**: Use of context windows, chunking, and system instructions
- **Dense vs Sparse Retrieval**: DPR (dense), BM25 (sparse), hybrid models

---

## 🧠 Summary

RAG is a powerful strategy for enhancing LLMs with real-time knowledge retrieval. It's ideal for domains where up-to-date or proprietary information is required without retraining the base model.

Use it when:
- You need grounded, factual outputs
- Your data changes frequently
- You want to avoid costly fine-tuning

---







