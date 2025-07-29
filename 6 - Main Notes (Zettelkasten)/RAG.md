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

#### 1. **Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks**

**Authors:** Patrick Lewis, Ethan Perez, Aleksandra Piktus, et al.  
**Year:** 2020  
**📎 Link:** [https://arxiv.org/abs/2005.11401](https://arxiv.org/abs/2005.11401)  
🧠 **Why it matters:**  
This is _the_ OG RAG paper from Facebook AI. Introduces the architecture that combines a dense retriever (like DPR) with a generator (like BART). Showed that RAG can outperform traditional open-domain QA systems.

#### 2. **Dense Passage Retrieval for Open-Domain Question Answering**

**Authors:** Vladimir Karpukhin, Barlas Oğuz, Sewon Min, et al.  
**Year:** 2020  
**📎 Link:** [https://arxiv.org/abs/2004.04906](https://arxiv.org/abs/2004.04906)  
🧠 **Why it matters:**  
This paper introduced **DPR**, the retrieval engine that underpins many RAG systems. It made dense retrieval _actually work_ for real-world QA tasks.


#### 3. **REALM: Retrieval-Augmented Language Model Pre-Training**

**Authors:** Kelvin Guu, Kenton Lee, Zora Tung, et al.  
**Year:** 2020  
**📎 Link:** [https://arxiv.org/abs/2002.08909](https://arxiv.org/abs/2002.08909)  
🧠 **Why it matters:**  
From Google Research. One of the earliest frameworks where a language model learns to retrieve _during pretraining_. A more baked-in approach than RAG, which is modular.





