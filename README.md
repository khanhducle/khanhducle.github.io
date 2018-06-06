# Visual Search

Visual search is an old and well-studied topic in computer vision and is integrated into many widely-used search engines such as Google, Bing, and DuckDuckGo. Instead of submitting a keyword or text to the system and getting relevant documents back, user will submit an image and the system will return images that have similar visual contents. 
Traditional approach to web-scale image retrieval relies on bag-of-visual-word model. In this model, local features such as SIFT or SURF are extracted from the query images. Those features are then assigned to their closest visual words in a visual vocabulary. A visual vocabulary is constructed by extracting local features from all of the images in the database, then using k-means clustering to find the centers of each cluster. The centers are the visual words of the vocabulary. The query image is accordingly represented by a global histogram of visual words, and matched with database images by tf-idf weighting using inverted files. This research activity will explore this techniques step by step so that the user has an overview about image retrieval in general.

## [Overview of Image Search Engine](cbir_intro.md)
## [Basic Image Search Pipeline](basic_cbir_pipeline.md)
### [1. Image Representation Module](image_representation.md)
### [* Feature Extraction Submodule](feature_extraction.md)
### [* Codebook Construction Submodule](codebook_construction.md)
### [* Feature Quantization Submodule](feature_quantization.md)
### [2. Database Indexing Module](database_index.md)
### [3. Image Scoring Module](image_socring.md)
### [4. Spatial Verification Module](spatial_verification.md)


