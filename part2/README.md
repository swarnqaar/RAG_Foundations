## Embedding (Retrieval)

--> we as a human can classify the synonyms (different sentences of similar meaning) but computer/rag cannot, thats why embedding comes into role.

## suppose we are giving information (apple, cake, kukure) in knowledge base.

--> here computer doesnot understand the meaning of above information thats why will convert (apple , cake , kurkure) into vector/array based on sweetness and crunch
--> these are called embedding.

-->sweet(0-10)
-->crunch(0-10)

1. apple --> (8 , 7)
2. cake --> (10 , 2)
3. kurkure --> (1 , 9)

==> here we have to calculate the similarities b/w apple and cake 
==> |8-10| + |7-2| = 7 
--> here the differences b/w apple and cake are 7/20 , this difference is called cosine differences. 

## note --> in real embedding the size of array is 784 , means there are 784 feature in each data/the data is trained on 784 features. "every index of the array represents different features"
