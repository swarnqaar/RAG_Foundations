## Multi-tenant RAG using qdrant ( Filters and HNSW)

## HNSW(hierarchial Navigable small world) : this is a type of algorithm used for search from vectorDB

Example : suppose qdrant have 10 vector one query vector , then qdrant extract maximum similarity data by calculating cosine similarity. there are some methods of it.

1. linear search : each vector calculate cosine similarity with query vector and get 10 score in which it will select top3. (this method can be applied for small vector but for million of vector its not possible as it take much time )

2. HNSW : 


##  Filters