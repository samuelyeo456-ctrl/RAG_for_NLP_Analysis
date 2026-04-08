# RAG for NLP Analysis

This is a Python based RAG project where insights can be found from survey data. Additionally, LLM-evaluation metrics, and topic modelling techniques are used.


The project covers the following process:
1. Data Preprocessing Techniques
   - Text Refinement: Comprehensive Regular Expressions (Regex) to remove filler words
   - Greedy Chunking: It splits the long transcripts into smaller, 1000-character "chunks" with a 200-character overlap
2. The Retrieval System (Vector Store)
   - Embedding Model: all-MiniLM-L6-v2 to convert your text chunks into numerical vectors
   - FAISS: IndexFlatIP (Inner Product) FAISS index to store  vectors and perform ultra-fast similarity searches
3. Triple-Pronged Topic Modeling
   - N-gram Extraction: Uses TF-IDF to find the most frequent multi-word phrases
   - LDA (Latent Dirichlet Allocation): A statistical model that clusters words into distinct topics
   - BERTopic: A modern, transformer-based approach that provides much higher "diversity" and "coverage" scores
4. Generation & Local RAG
   - Research prompting and tuning
   - Local method uses flan-t5-large, all-MiniLM-L6-v2 and FAISS
   - Cloud method uses text-embedding-3-small, and OpenAI GPT4.1 mini
5. Evaluation & Optimization
   - Top-K,Temperature, Top-P, Similarity Thresholds
