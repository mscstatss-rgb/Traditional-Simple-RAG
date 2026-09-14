# Traditional-Simple-RAG

An end-to-end implementation of a traditional Retrieval-Augmented Generation (RAG) pipeline, covering both the **Data Ingestion Pipeline** and the **Retrieval & Generation Pipeline**.

## Data Ingestion Pipeline

1. **Data Sources**
   Supports data from different sources and formats such as PDFs, Excel files, and SQL databases.

2. **Parsing & Chunking**
   Extracts and parses the source data, converts it into LangChain `Document` objects, and splits the content into smaller chunks for efficient retrieval.

3. **Embedding & Vector Storage**
   Generates embeddings for each document chunk using an embedding model/API and stores the resulting vectors in a vector database.

## Retrieval & Generation Pipeline

4. **Query Embedding & Similarity Search**
   Converts the user's query into an embedding and performs similarity search against the vector database to retrieve the most relevant document chunks.

5. **Context Augmentation & Prompting**
   Combines the retrieved information with the user's query to construct a context-aware prompt.

6. **LLM Generation**
   Passes the augmented prompt to an LLM to generate a response grounded in the retrieved information.

### Overall Flow

**Data Sources → Parsing → Chunking → Embedding → Vector Database → Query Embedding → Similarity Search → Context + Prompt → LLM → Response**
