### Description
Unsupervised document clustering and topic modeling using K-Means

### Instructions
Run PP.java to execute program

Cluster assignments printed to standard output along with corresponding topics.
Topics can also be found in topics.txt which is generated on every run of PP.java.
Cluster Visualization created with outside tools, is not generated with code.

### Requirements

- StanfordCoreNLP

### File Descriptions

PP.java 
- preprocesses text data, creates document-term matrix
- runs Kmeans on document-term matrix
- "smart" kmeans (almost kmeans++) is implemented
- standard functionality of kmeans is to create k random vectors. I choose to randomly select k vectors from input data 
to be initial centroids, which yields higher convergence rate.
- performance function is called "purity", where a purity of 1 or 100% means that
the true clustering of documents is achieved. I compute this by determining if 
there exists 3 non-overlapping subsets of size 8 where each subset contains either
1,2, or 3 but not more than one kind of those values
e.g. assume we had 3 input documents where doc 1 and 2 are clustered together.
the true clustering would look like [1,1,2]. If my kmeans algorithm outputted
[1,1,1] my accuracy would be 66%. If my algorithm outputted [1,1,2] or [2,2,1]
my accuracy would be 100%
    
DistanceMeasure.java

- standard implementations of cosine and euclidean distance
- cosine is default measure
   
stopWords.txt

- found on google
