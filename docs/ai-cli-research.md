# AI CLI Research

- [Network Chuck - AI cli stack](https://github.com/theNetworkChuck/ai-in-the-terminal/blob/main/README.md) - [yt](https://www.youtube.com/watch?v=MsQACpcuTkU&t=1798s)

## Postgres vector

- https://www.pgedge.com/blog/building-ai-agents-on-postgres-why-we-built-the-pgedge-agentic-ai-toolkit
- https://github.com/pgEdge
- https://www.pgedge.com/blog/introducing-the-pgedge-postgres-mcp-server

PostgreSQL can be used as a vector store by  
utilizing the open-source extension pgvector. This extension adds a  data type, indexing mechanisms, and operators for performing efficient similarity searches directly within your existing relational database, eliminating the need for a separate dedicated vector database in many scenarios. 
Key Features of PostgreSQL with pgvector 

• Native Integration  operates within PostgreSQL, allowing you to store and manage high-dimensional vector embeddings alongside your structured, relational data. 
• Similarity Search It enables similarity search using distance metrics like L2 distance (Euclidean), inner product, and cosine distance. This allows for finding items based on semantic meaning rather than exact keyword matches. 
• Indexing The extension supports indexing mechanisms like HNSW (Hierarchical Navigable Small Worlds) and IVFFlat for efficient approximate nearest neighbor (ANN) search on large datasets. 
• AI Applications  is a core component for building modern AI applications such as: 

	• Semantic text search 
	• Recommendation systems 
	• Image similarity lookup 
	• Retrieval-Augmented Generation (RAG) systems with Large Language Models (LLMs) [1, 2, 3, 4, 5, 6]  

Getting Started 
To enable and use PostgreSQL as a vector store, follow these general steps: 

1. Install the  extension  on your  PostgreSQL server 

. This is often pre-installed on managed cloud database services like Azure Database for PostgreSQL, Google Cloud SQL, and Timescale, but may require manual installation for self-hosted instances. 
2. Enable the extension in your target database by running the SQL command: 
3. Create a table with a vector column to store your embeddings, specifying the desired dimensions: 
4. Insert vectors into the table, either manually or via bulk copy operations: 
5. Perform similarity search using the provided operators. For example, to find the nearest neighbors by L2 distance: [1, 4, 8, 9, 10]  

Integrations 
 integrates with various development frameworks and libraries, including LangChain, LlamaIndex, and Semantic Kernel. This allows developers to easily incorporate vector search capabilities into their AI applications using familiar tools. [11, 12, 13, 14, 15]  

AI responses may include mistakes.

[1] https://github.com/pgvector/pgvector
[2] https://www.yugabyte.com/key-concepts/using-postgresql-as-a-vector-database/
[3] https://cloud.google.com/discover/what-is-pgvector
[4] https://www.tigerdata.com/learn/postgresql-extensions-pgvector
[5] https://www.enterprisedb.com/blog/what-is-pgvector
[6] https://www.tigerdata.com/blog/postgresql-as-a-vector-database-using-pgvector
[7] https://www.youtube.com/watch?v=ZwASqFrUXVw
[8] https://docs.cloud.google.com/sql/docs/postgres/generate-manage-vector-embeddings
[9] https://medium.com/tessell-dbaas/postgresql-as-vector-database-create-llm-apps-with-pgvector-64677de48fc2
[10] https://docs.cloud.google.com/sql/docs/postgres/generate-manage-vector-embeddings
[11] https://developers.llamaindex.ai/python/framework/integrations/vector_stores/postgres/
[12] https://docs.langchain.com/oss/javascript/integrations/vectorstores/pgvector
[13] https://learn.microsoft.com/en-us/semantic-kernel/concepts/vector-store-connectors/out-of-the-box-connectors/postgres-connector
[14] https://www.tigerdata.com/learn/postgresql-extensions-pgvector
[15] https://www.yugabyte.com/key-concepts/using-postgresql-as-a-vector-database/


## Google AI Tools Research
- Google AI [yt](https://www.youtube.com/watch?v=gXm4Rp6gjEU)
  1. AI Studio Build (inside Google AI Studio) 
  2. Opal 
  3. NotebookLM (specifically the Video Overview feature) 
  4. Pomelli (Google Labs) 
  5. Gemini Canvas (inside Gemini → Tools → Canvas)
  6. Nano Banana Pro (Gemini's image generation model, inside Gemini → Tools → Create Images; also in AI Studio)
  7. Multi-Speaker Audio Generation (inside Google AI Studio → Speech interface → Multi-Speaker)
- https://aistudio.google.com/
  - https://aistudio.google.com/generate-speech
- https://opal.google/landing/
- https://notebooklm.google.com/
- https://labs.google.com/pomelli/about/
- https://gemini.google.com/app
  - Tools -> Create Images
