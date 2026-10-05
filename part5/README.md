## Multi-tenant RAG using qdrant ( Filters and HNSW)

## HNSW(hierarchial Navigable small world) : this is a type of algorithm used for search from vectorDB

Example : suppose qdrant have 10 vector one query vector , then qdrant extract maximum similarity data by calculating cosine similarity. there are some methods of it.

1. linear search : each vector calculate cosine similarity with query vector and get 10 score in which it will select top3. (this method can be applied for small vector but for million of vector its not possible as it take much time )

2. HNSW : example--> suppose i am at my house , i have to reach BCET for admission, then there is two method, first linear search (step out of house and ask everyone is this BCET) and second one is HNSW (stepout out of the house then ask where the busstand is and then ask which is next bus for durgapur, then at durgapur station ask rapido to drop bidhanagar, then asked anyone where the BCET ) this method is HNSW.


##  Filters  
1. 
text:"24 days of leave"
category:"vacation"
is_active:"true"

2. 
text:"24 days of leave"
category:"vacation"
is_active:"false"

3. 
text:"8 hrs of work"
category:"work-life balance"
is_active:"true"

--> how many days of leave?
==> then it directly go through category of filter instead of iterating each and every vector.

## for using filter, we have to create index

1. collection--> create knowledge base
2. index--> category , is-active (vacation/work-life-balance)

NOTE --> create index on category, is-active so qdrant remember from it and when we search it will easily finds from here.

# how to use this filters (3 things)

1. Must: (more than one condition and both should true)--> Ex: (category:"vacation", is-active:"true)
2. Must Not: (only one condition) --> Ex: (category:"vacation")
3. should: (anyone condition should true) --> Ex: (category:"vacation", is-active:"true)