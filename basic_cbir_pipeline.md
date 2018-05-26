# Basic CBIR Pipeline
Here is the basic building block of CBIR:
-- Image

## Building Block Explanation

### FEATURE EXTRACTION Block
**Feature** (**Feature vectors**): A list of numbers used to abstractly represent and quantify images. These vectors are the results ofr Feature Extraction process.
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/Feature_Extraction.PNG">
</p>
<p align="center">
    <b>Feature Extraction Block</b>
</p>
**Feature Extraction**: The process of quantifying the dataset by extracting features from each and every image in the dataset. Feature extraction is quite a simple concept in principle, but in reality it can become very complex depending on the size and scale of the dataset. 

### DATABASE INDEXING Block
**Indexing dataset of features**: 
- Take the extracted features from previous step and store them on disk/database(CSV file, RDBMS, Redis, etc.) for later use
- **Indexing** the dataset using a specialized data structure (inverted index, kd-tree, or random projection forest) to reduce search time.

### IMAGE SCORING Block

**Distance Metric / Similarity Function**: take 2 feature vectors as input, output a number that represents how "similar" the two feature vectors are

-- Image

### SEARCH RERANKING block
**Spatial Verification / Geometric Verification**: process of performing keypoint detection, extracting local invariant descriptors, computing a homography matrix (using  RANSAC) between 2 iamges, and finally determining how many keypoints between 2 images are "matches"
## Flowchart Explanation
