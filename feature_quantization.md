##Feature Quantization submodule

After constructing the codebook, the next step is to assign each feature in an image to the closest visual word in the pre-trained visual codebook from the previous step. The simplest choice is to take the nearest neighbor search by calculating the Euclidean distance from  a given feature to all the visual words in the codebook to find the closest (the most similar) visual word. The quantization result of a single feature is a high-dimensional binary vector, where the non-zero dimension corresponds to the quantized visual words.
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/quantize1.png">
</p>
<p align="center">
    <b>An example of quantization result of a feature vector to the vector of visual words</b>
</p>

Finally, the BOVW vector is obtained by pooling the quantization results of all features in an image. For the basic CBIR system, counting the number of times each of visual words appears in an image is a common pooling technique. 
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/Quantize3.png" width="350">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/Quantize4.png" width="350">    
</p>

<p align="center">
    <b>Feature Quantization<br/><b>Source: http://www.cs.utexas.edu/~grauman/courses/fall2009/papers/bag_of_visual_words.pdf</b></b>
</p>

However, term frequency-inverse document frequency (tf-idf), a concept borrowed from the field of Information Retrieval, can be used instead to improve the retrieval accuracy since it weights more informative visual words in the dataset. 
Since the visual codebook is very large and the generated BOVW vector is very sparse, the bag-of-visual-words model usually used along with the inverted file indexing scheme, which is discussed in the next section.
