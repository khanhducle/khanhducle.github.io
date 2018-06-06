## Database Indexing module
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/database_index_main2.png">
</p>
<p align="center">
    <b>Database Indexing module</b>
</p>

Image index refers to a database organizing structure to assist for efficient retrieval of the target images. Since the response time is a key issue in retrieval, database indexing plays an important role in content-based image retrieval. One of the indexing techniques are popularly adopted is **inverted file indexing**, or **inverted index** [1].

In the **inverted file structure**, each visual word is followed by an inverted file list of entries. Each entry stores the image IDs where the visual word appears:
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/database_index.png">
</p>
<p align="center">
    <b>Inverted Index Data structure</b>
</p>

When performing a search in online stage, those images sharing common visual words with the query image need to be checked. Therefore, the number of candidate images to be compared is greatly reduced, achieving an efficient response.


#### Reference
[1] R. Baeza-Yates, B. Ribeiro-Neto et al., Modern information retrieval. ACM press New York., 1999, vol. 463
