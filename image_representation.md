Image Representation Module
The key problem in content-based image retrieval is how to efficiently measure the similarity between images. Since the visual objects or scenes may undergo various changes or transformations, it is impossible to directly compare images at pixel level. Therefore, visual features are usually extracted from images and subsequently transformed into a fix-sized vector for image representation.
One of the state-of-the-art techniques for image representation in the early 20s is bag-of-visual-words model [1]. Bag-of-visual-words concepts is taken from the “bag of words” model from the field of information retrieval and text analysis. The idea is to represent “documents” as a collection of important keypoints while disregarding the order the words appear in. Documents that share a large number of the same keywords are considered to be relevant to each other. In computer vision, the same concept is applied; instead of using keywords, “words” are now image patches and their associated feature vectors. Building bag of visual words can be broken down into three-step process:
Step #1: Feature Extraction
Step #2: Codebook construction
Step #3: Feature quantization


[1] J. Sivic and A. Zisserman, “Video Google: A text retrieval approach to object matching in videos,” in IEEE Conference on
Computer Vision and Pattern Recognition, 2003, pp. 1470–1477
