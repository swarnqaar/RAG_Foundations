## Qdrant (VectorDB) database

--> why vectordb : 
1. Time: At the time of embedding, its find cosine simlarity at each line fron knowledgebase. And the when the knowledgebase is very huge, it may took more time.

2. Persistence: when power is cut(lost all the vector), we have to starts this program once again, and once again embedding will created and stored .

3. Memory: To store line of vector , it require space (when we storing million lines of vector , it may require GBs of storage)

Note: there are some other vectorDB such weavelet(steep learning), ChromaDB, FAISS, Pinecone like quadrant(free to use)

## VectorDB : collection of vectors (stored in arrays)

--> important points:
1. it have ID {101}
2. vector = (-10, 4, 9, 7, 4. -7)
3. Payload { actual meaning of vector}

Note--> How RAG using vector database works : first we create/store line of information in knowdgebase then apply embedding and stores the vector and their payload in vectorDB , and we give queryvector it find cosine similarity and then extract top vector with payload forwarded to LLM.