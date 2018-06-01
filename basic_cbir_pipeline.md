# Basic CBIR Pipeline
![CBIR Pipeline](https://github.com/khanhducle/khanhducle.github.io/blob/master/images/Pipeline.PNG)
Visual search framework consists of an off-line stage and an on-line stage. 
- In the offline stage, each image in the database is represented by some feature vectors (Feature Extraction) and then indexed in the database using some data structure (Database Indexing).
- In the online stage, a user will submit a query image to the system (by uploading from computer/mobile app). The system will:
   1. extract features from this query image (Feature Extraction Block)
   2. apply similarity function to compare the query features to the features already indexed (Image Scoring)
   3. apply post-processing techniques to improve search results (Search Reranking)
   4. return most relevant results to the user (Output Images)

### Feature Extraction Block
**Feature** (**Feature vectors**): A list of numbers used to abstractly represent and quantify images. These vectors are the results ofr Feature Extraction process.
![Feature Extraction]("https://github.com/khanhducle/khanhducle.github.io/blob/master/images/Feature_Extraction.PNG")
<p align="center">
    <b>Feature Extraction Block</b>
</p>

The purpose of this block is to extract the features. **Feature extraction** is the process of quantifying the dataset by extracting features from each and every image in the dataset. Feature extraction is quite a simple concept in principle, but in reality it can become very complex depending on the size and scale of the dataset. 

### Database Indexing Block
Since the response time is a key issue in retrieval, the purpose of this block is to assist for efficient retrieval of the target images. This consists of 2 steps:
- Take the extracted features from previous step and store them on disk/database(CSV file, RDBMS, Redis, etc.) for later use
- **Indexing** the dataset using a specialized data structure (inverted index, kd-tree, or random projection forest) to reduce search time.
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/inverted_index.PNG">
</p>
<p align="center">
    <b>Database Indexing Block</b>
</p>

### Image Scoring Block

**Distance Metric / Similarity Function**: take 2 feature vectors as input, output a number that represents how "similar" the two feature vectors are

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/cbir_comparing_images.jpg">
</p>
<p align="center">
    <b>Image Scoring Block</b>
</p>

While searching, we need a way to rank the image based on its similarity. The purpose of this block is to assign a relevance score for each image that is returned from the search.

### Search Reranking Block
The purpose of this block is to post-process the search results to boost the accuracy of the image search. Some of the successful techniques include Geometric Verification (Spatial Verification), Query Expansion, and Retrieval Fusion 
