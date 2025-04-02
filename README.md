# RAG-Pipeline-Benchmark
I benchmark different rerankers on a rag pipeline with NEET 2022 questions and their solution explanations as corpus.

##  RAG Pipeline Benchmark Results

All results are based on evaluation over **146 queries**.

Base Model = LLama-3.2-3b-Instruct

###  Baseline
- **Accuracy**:  52 / 146 = **35.62%**

---

###  With SentenceTransformer + Reranker

**Embedder**: `Leo1212/longformer-base-4096-sentence-transformers-all-nli-stsb-quora-nq`  
**Top-k Retrieval**: `k=20`  
**Rerank Top**: `rerank=5`  

| Reranker Model                            | Accuracy        | 
|-------------------------------------------|------------------|
| `cross-encoder/ms-marco-MiniLM-L-6-v2`    |  131 / 146     | 
| `cross-encoder/ms-marco-electra-base`     |  126 / 146     | 
| `BAAI/bge-reranker-v2-m3`                 |  135 / 146     | 

** Best Accuracy Achieved**: **92.47%** with `BAAI/bge-reranker-v2-m3`

---

![Graph(19)](https://github.com/user-attachments/assets/2206239d-5fa2-4742-a6c5-43d1f663f3ea)

