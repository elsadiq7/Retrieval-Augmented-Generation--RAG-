### **Question 1**

What is the fundamental difference between k-nearest neighbors (kNN) and approximate nearest neighbors (ANN) algorithms in vector search?

* kNN is used for classification tasks while ANN is used for search tasks.
* kNN works with vectors while ANN works with other data structures.
* kNN calculates distances to all vectors while ANN uses optimized structures to avoid exhaustive search.
* kNN returns k results while ANN returns a variable number of results.
* **kNN performs an exhaustive search by calculating distances between the query and every single vector in the database, while ANN algorithms use specialized data structures like proximity graphs to approximate results without examining all vectors.** ✅

---

### **Question 2**

A data scientist is implementing a vector database for a recommendation system that needs to handle millions of product embeddings. What should they understand about the results returned by the vector database?

* The vector database will always calculate distances to all vectors, just more efficiently.
* The results might not always be the exact nearest neighbors, but searches can be completed substantially faster.
* Query time will increase linearly as the number of vectors increases.
* The vector database still performs an exhaustive search, but only considers the vectors in the neighborhood of the query vector.
* **They prioritize search speed by using approximation algorithms that may not find the mathematically perfect nearest neighbors but find very close matches efficiently.** ✅

---

### **Question 3**

What is the key feature that distinguishes hybrid search from running vector and keyword searches independently?

* Hybrid search alternates between vector and keyword search methods depending on query complexity.
* Hybrid search assigns weights to results from both methods and combines their rankings using an alpha parameter.
* Hybrid search always adds semantic and keyword scores equally to compute a final document rank.
* Hybrid search uses vector search results and then filters them based on keyword matches.
* **It integrates semantic and keyword results by applying configurable weighting.** ✅

---

### **Question 4**

Why might using very large chunks in a vector database potentially reduce retrieval accuracy?

* Large chunks require more processing time to convert to vectors.
* Large chunks create vectors that average many different topics together, diluting specific concepts.
* Large chunks result in duplicate vectors being created for the same content, causing confusion during retrieval.
* Large chunks make it impossible for the database to build an effective index.
* **This accurately reflects the challenge with large chunks. When many topics are compressed into a single vector, it becomes a broad average rather than a precise representation of specific concepts, making targeted retrieval difficult.** ✅

---

### **Question 5**

A company has implemented query parsing in their retrieval system. Which expectation about this implementation is most realistic?

* Query parsing will sometimes provide benefits but at such a high computational cost that the tradeoff is not worth it.
* Query parsing will improve retrieval quality and works well in conjunction with other techniques like thoughtful chunking and re-ranking.
* Query parsing will help determine if a prompt should be processed by a cheaper bi-encoder or a more costly cross-encoder.
* Query parsing ensures only prompts that will result in a successful retrieval are processed by the system.
* **This accurately reflects query parsing's role. It enhances retrieval through techniques like query rewriting and entity extraction, but models aren't perfect and systems benefit from ongoing evaluation and improvement.** ✅

---

### **Question 6**

Which of the following is a genuine limitation developers should consider when using Named Entity Recognition (NER) in query parsing?

* NER models can only process short queries under 50 words.
* NER models only extract entities from categories they're specifically configured to identify.
* NER models work only on formal, professionally written queries.
* NER models must be retrained for each new query type.
* **NER models, including advanced ones like GLiNER, rely on a predefined set of entity types (such as "person," "location," "product") to function.** ✅

---

### **Question 7**

What is the most accurate characterization of bi-encoder models used in vector databases compared to cross-encoders used in reranking?

* Bi-encoders are a historical but ultimately primitive search technology that has since been replaced by the cross-encoder.
* Bi-encoders are effective at capturing general semantic similarity but miss some nuanced query-document interactions.
* Bi-encoders provide the same accuracy as cross-encoders but are restricted to initial retrieval due to design preference.
* Bi-encoders only work for exact keyword matching while cross-encoders handle semantic matching.
* **Bi-encoders efficiently capture semantic relationships but can miss some of the specific interactions between queries and documents that cross-encoders can identify.** ✅

---

### **Question 8**

In a hierarchical navigable small world (HNSW) algorithm, why does starting the search at the top layer with fewer vectors improve efficiency?

* The top layer contains only the most important documents in the collection.
* It allows making large navigational jumps to quickly identify the approximate neighborhood where the query belongs.
* It eliminates the need to build proximity graphs for lower layers.
* It reduces the total number of documents that need to be indexed.
* **The algorithm can make "big jumps" to quickly find the general area where matching vectors are located before drilling down to more precise matches.** ✅

---

### **Question 9**

What is a primary drawback of using semantic or LLM-based chunking in a RAG pipeline?

* These techniques tend to increase retrieval latency due to the higher number of chunks.
* These techniques rely too heavily on fixed chunk sizes that may not match content boundaries.
* Semantic and LLM-based chunking require extensive pre-processing and are computationally expensive.
* Semantic and LLM-based chunking produce lower retrieval quality than fixed-size chunking.
* **These advanced methods often produce higher quality chunks but require significant compute resources.** ✅

---

### **Question 10**

In the HyDE (Hypothetical Document Embeddings) technique, what is the role of the hypothetical document?

* It is used to build filters for metadata search.
* It replaces the original prompt during semantic search.
* It improves LLM summarization during generation.
* It helps generate keywords for improved lexical search.
* **HyDE generates a hypothetical document using an LLM, then embeds it to serve as the query vector, improving semantic alignment between prompt and retrieved content.** ✅