## Image Representation Module
The key problem in content-based image retrieval is how to efficiently measure the similarity between images. Since the visual objects or scenes may undergo various changes or transformations, it is impossible to directly compare images at pixel level. Therefore, visual features are usually extracted from images and subsequently transformed into a fix-sized vector for image representation.
One of the state-of-the-art techniques for image representation in the early 2000 is bag-of-visual-words model [1]. 

### Bag-of-visual-words (BOVW) Model
Bag-of-visual-words concepts is taken from the “bag of words” model from the field of information retrieval and text analysis. The idea is to represent “documents” as a collection of important keypoints while disregarding the order the words appear in. Documents that share a large number of the same keywords are considered to be relevant to each other. The advantage of treating a document as a “bag of words” is to allow us to efficiently analyze and compare documents since we do not have to store any information regarding the order and locality of words to each other — we simply count the number of times a word appears in a document, and then use the frequency counts of each word as a method to quantify the document 
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/bovw_text_example.jpg">
</p>
<p align="center">
    <b>Bag of Words Model for Text Retrieval<br/><b>Source: https://gilscvblog.com/tag/bag-of-words/</b></b>
</p>

In computer vision, the same concept is applied; instead of using keywords, “words” are now image patches and their associated feature vectors:

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/bovw_image_example.jpg">
</p>
<p align="center">
    <b>Bag of Visual Words Model for Image Retrieval<br/><b>Source: https://gilscvblog.com/2013/08/23/bag-of-words-models-for-visual-categorization/</b></b>
</p>

In Information Retrievel and text analysis field, performing bag-of-words model is trivially easy - you simply count them and construct a histogram of word occurrences. However, applying the bag of words concept in computer vision is not as simple. How exactly do you count the number of times an “image patch” appears in an image? And how do you ensure the same “vocabulary” of visual words is used for each image in your dataset? 

### Building bag-of-visual-words model
Building bag of visual words can be broken down into three-step process:
* Step #1: Feature Extraction
* Step #2: Codebook construction
* Step #3: Feature quantization

I will cover these steps in detail over the next few blogs.

#### Reference
[1] J. Sivic and A. Zisserman, “Video Google: A text retrieval approach to object matching in videos,” in IEEE Conference on
Computer Vision and Pattern Recognition, 2003, pp. 1470–1477
