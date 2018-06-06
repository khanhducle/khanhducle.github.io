## Feature Extraction submodule
In image processing and computer vision area, **feature vector** is an abstraction of an image used to characterize and numerically quantify the contents of an image. In other words, it is a list of numbers used to represent an image. **Feature extraction** is the process of computing feature vectors from an image. Generally, the feature extraction for image retrieval involves two key steps: 
1. keypoint detection
2. local region description

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/feature_extraction1.png">
</p>
<p align="center">
    <b>Feature Extraction Pipeline <br/><b>Source: https://gilscvblog.com/tag/bag-of-words/</b></b>
</p>

### Keypoint Detection
**Keypoint detection** is to find the “interesting” regions of an image. These regions can be edges, corners, “blobs,” or regions of an image where the pixel intensities are approximately uniform. At the very core, keypoints are simply the (x, y) coordinates of the interesting, salient regions of an image. 
There are many different algorithms that can find and detect these “interesting” regions. Difference of Gaussian (DoG) [1] used to detect “blob”-like structures in images is an example of keypoint detection. What makes DoG stands out from other keypoints algorithm is its repeatability, meaning that the keypoints can be identified under various lighting conditions and transformation. However, because of the slow speed of DoG, Fast Hessian [2] is introduced instead. This algorithm is built on the same principles as DoG in that keypoints should be both repeatable and recognizable at different scales of an image.

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/keypoint_detection.png">
</p>
<p align="center">
    <b>An Example of Keypoint Detection <br/><b>Source: https://www.pyimagesearch.com/</b></b>
</p>

### Local Region Description
For each of the keypoints, feature vector are extracted to describe the visual appearance of the local region centered at the keypoint. This process of extracting multiple feature vectors, one for each keypoint, is called **local region description**. 
Just like keypoints detection, the descriptor is designed to be invariant to rotation, distortion, or noise… There are many different algorithms for this step also. The most popular choice is SIFT feature [1]. Some improvements have been made on the basis of SIFT. In [3], Arandjelovic *et al* proposed a root-SIFT by making root-normalization on the original SIFT descriptor. It is demonstrated to dramatically increase the image retrieval accuracy.

#### Refernce
[1] D. G. Lowe, “Distinctive image features from scale invariant keypoints,” International Journal of Computer Vision, vol. 60, no. 2, pp. 91–110, 2004
[2] K. Mikolajczyk and C. Schmid, “Scale & affine invariant interest point detectors,” International Journal of Computer Vision, vol. 60, no. 1, pp. 63–86, 2004
[3] R. Arandjelovic and A. Zisserman, “Three things everyone should know to improve object retrieval,” in IEEE Conference on Computer Vision and Pattern Recognition, 2012, pp. 2911–2918.
