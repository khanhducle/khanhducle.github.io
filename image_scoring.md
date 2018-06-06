## Image Scoring module
The target results in the index image database are assigned with a relevance score for ranking and then returned to users. The relevance score can be defined by measuring distance between the BOVW feature vector obtained from Image Representation module. There are a lot of similarity functions to measure how “similar” two feature vectors are, but two important ones can be used in this project are **chi-squared distance** and **cosine distance**:

**Chi-squared distance** measure the distance between two histograms. Images that have a chi-squared distance of 0 will be considered to be identical to each other. As the chi-squared similarity value increase, the images are less similar to each other.
<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/distance_metric.png">
</p>
<p align="center">
    <b>Chi-squared Distance</b>
</p>


**Cosine distance**, on the other hand,  returns a value between -1 and 1, where 1 indicates perfect similarity, 0 indicates orthogonality (decorrelation), and -1 corresponds to “exactly opposite”. 

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/distance_metric1.png">
</p>
<p align="center">
    <b>CCosine Distance</b>
</p>
