## Codebook Construction submodule
Usually, hundreds or thousands of features are extracted from a single image. To achieve a compact representation, those features are quantized to visual words of a pre-trained visual codebook (Codebook Construction submodule)  and based on the quantization results, an image with a set of features can be transformed to a fixed-length vector by Bag-of-Visual Words model (Feature Quantization submodule).

To construct a visual codebook beforehand, k-means clustering algorithm, an unsupervised learning algorithm that automatically forms clusters of similar points, is used to cluster the feature vectors obtained from Feature Extraction submodule [1]. After running k-means algorithm, the clustering centers are considered as visual words.
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/k_means.png">
</p>
<p align="center">
    <b> Example of k-means results with three clusters of data and their corresponding centers. Each center will represent a visual word</b>
</p>

Because of the high computational complexity to train a large visual codebook, mini-batch k-means algorithm [2], a more efficient and scalable version of the original k-means algorithm is proposed. It breaks the dataset into small segments, clustering each of the segments individually, then merging the clusters resulting from each of these segments together to form the final solution. 
While the clusters obtained from mini-batch k-means are not as accurate as the ones using the standard k-means algorithm, it run faster than standard k-means. In reality, perfect cluster centers from k-means is not necessary,  therefore, mini-batch k-means is chosen over standard k-means whenever possible.


#### Reference
[1] J. Sivic and A. Zisserman, “Video Google: A text retrieval approach to object matching in videos,” in IEEE Conference on
Computer Vision and Pattern Recognition, 2003, pp. 1470–1477.
[2] Sculley, D, “Web-scale k-means clustering,” 2010.
