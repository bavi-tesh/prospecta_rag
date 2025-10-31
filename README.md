# Prospecta – Hybrid RAG-Based IPO Insight Assistant
> A Retrieval-Augmented Generation (RAG)–powered financial assistant for IPO (DRHP) document analysis, combining semantic and keyword retrieval, reranking, and Llama 3.3 reasoning with an interactive Gradio chat UI.

---

## Workflow

1. **Document Ingestion** – Loads DRHP PDFs using `PyMuPDFLoader` and attaches metadata for traceability.  
2. **Text Chunking** – Splits documents with `RecursiveCharacterTextSplitter` for efficient retrieval.  
3. **Embedding & Indexing** – Encodes chunks using `HuggingFaceEmbeddings` and builds a **FAISS** index.  
4. **Hybrid Retrieval** – Combines **semantic** (FAISS) and **keyword** (BM25) results, deduplicated by content.  
5. **Cross-Encoder Reranking** – Refines the top results using a transformer-based **CrossEncoder** model.  
6. **LLM Response Generation** – Llama 3.3 processes the query and reranked context to produce a concise answer.  
7. **Interactive Interface** – Users interact with the system via **Gradio ChatInterface**.

---

## Example Queries

- “What is the meaning of DRHP?”  
- “Who regulates IPO filings in India?”  
- “Where is the registered office of the company?”  
- “What is the type of offer mentioned in the DRHP?”

---

## Future Enhancements

- Integration with **financial APIs** for real-time updates  
- Summary visualization of financial tables  
- Multi-document conversational memory for context retention  
- Fine-tuned reranker for IPO domain data

---

## Author

**Bavitesh M**  
[mbavitesh24@gmail.com](mailto:mbavitesh24@gmail.com)  
[LinkedIn](#) | [GitHub](#) | [Medium](#)


