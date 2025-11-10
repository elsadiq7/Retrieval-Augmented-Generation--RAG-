### **Question 1**

What is the primary function of metadata filtering in a retrieval system?

* To analyze document content for semantic meaning
* To convert documents into dense vector representation
* **To match specific document attributes against strict query criteria** ✅
* To find documents containing the same keywords as the query

---

### **Question 2**

What fundamental limitation makes metadata filtering less effective than other retrieval methods for comprehensive document discovery?

* It requires more processing power than semantic search methods
* It cannot work alongside other retrieval techniques in RAG systems
* **It evaluates only document metadata while ignoring the actual content** ✅
* It supports filtering on only one metadata field at a time

---

### **Question 3**

When text is represented as a "Bag of Words" in keyword search, what single aspect of the original text is preserved?

* The sequence in which words appear in the document
* The grammatical relationships between adjacent words
* The proximity of words to one another in phrases
* **The number of times each word appears in the text** ✅

---

### **Question 4**

What primary capability defines keyword search when implemented in retrieval systems?

* Interpreting the meaning behind words in documents
* **Matching documents that contain the exact words found in the query** ✅
* Identifying documents whose metadata includes at least one of a supplied list of keywords
* Analyzing the structure of sentences in documents

---

### **Question 5**

What fundamental limitation of keyword search do embedding models specifically address in retrieval systems?

* The inability to process lengthy documents efficiently
* **The inability to connect semantically similar words or concepts** ✅
* The requirement for manual tagging of all indexed documents
* The inability to rank results based on term frequency

---

### **Question 6**

How do embedding models determine the vector space positions of words during their training process?

* By assigning each semantic concept to a predefined location in space
* **By iteratively adjusting positions based on training data made up of "positive" and "negative" word pairs** ✅
* By mapping words to locations according to definitions provided by linguists
* By analyzing dictionary definitions of words to calculate optimal locations

---

### **Question 7**

In which specific situation would keyword search likely perform better than semantic search in a retrieval system?

* When retrieving documents containing common everyday terminology
* **When searching for precise technical terminology or product codes** ✅
* When searching for documents with frequent misspellings
* When analyzing documents with complex metaphorical language

---

### **Question 8**

What is the primary function of Reciprocal Rank Fusion (RRF) in a hybrid search system?

* To execute keyword and semantic searches simultaneously
* **To merge ranked lists from different search methods mathematically** ✅
* To select which search method to apply to each query
* To ensure duplicate documents aren’t returned as a result of using multiple scoring techniques

---

### **Question 9**

In retrieval system evaluation, what is the primary purpose of using a Top-K cutoff when calculating metrics like precision or recall?

* It's simply a mathematical convenience that makes calculations more efficient
* **It helps standardize evaluation by focusing on the top-ranked results, which are typically the most useful for downstream tasks** ✅
* It helps to fuse and re-rank results from multiple disparate search methods into a single coherent list
* It ensures the evaluation process is faster by limiting the number of documents analyzed

---

### **Question 10**

You work at a popular cooking website with over 50,000 recipes. Your database includes both short recipe cards (just 1–2 paragraphs) and comprehensive cookbook chapters (over 10 pages).

When users search for "chocolate," they're only seeing tiny recipe cards at the top, even when there are excellent 10-page chocolate cake cookbook chapters in your database. The problem is that recipe cards mention "chocolate" in 5% of their words (3 times in 60 words), while the detailed cookbook chapters only mention it in 0.5% of their words (30 times in 6000 words).

Your team must choose between TF-IDF and BM25 to fix this problem where short documents unfairly dominate search results. Which algorithm should you implement?

* TF-IDF, because it rewards documents that include more copies of a keyword
* BM25, because it favors longer documents
* TF-IDF, because it rewards documents for including rare keywords like "chocolate" using its IDF term
* **BM25, because it penalizes long documents less aggressively than TF-IDF** ✅

