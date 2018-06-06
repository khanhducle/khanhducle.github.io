## Spatial Verification Module
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/database_index_main1.png">
</p>
<p align="center">
    <b>Spatial Verification Module</b>
</p>
The initially returned result list can be post-processed to boost the accuracy of the image retrieval by applying spatial verification. It is the process of performing keypoint detection, extracting local invariant descriptors, computing a homography matrix (using an algorithm such as RANSAC) between two images, and finally determining how many keypoints between the two images are matched. Based on how many keypoints match, the search results can be reranked, hence yielding better search accuracy. However, because spatial verification is a computationally expensive process, only top search results returned by the CBIR system are applied spatial verification.
