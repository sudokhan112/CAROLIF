# Unsupervised Crop Row Detection

The desiderata of a practical crop row detection method that works satisfactorily in real-life deployment are
below:  
(1) it is capable of detecting crop rows even with high weed pressure   
(2) it is applicable at different types of crop fields   
(3) it is capable to detect crop rows at different crop growth stages  
(4) it is capable to detect straight and reasonably curved crop rows; and finally,   
(5) the processing time of detection on an off-the-shelf computer satisfy real-time requirements.  
In this work, we propose a **Clustering Algorithm based RObust LIne Fitting (CAROLIF)** crop row detection method which satisfy all the above requirements. 

This is a challenging task due to substantial natural variations in crop row images due to various factors,  including, missing crops in parts of a row, high and irregular weed growth between rows, different crop growth stages, different inter-crop spacing, variation in weather condition, and lighting. The processing time of the detection algorithm also needs to be small so that the desired number of image frames from continuous video can be processed in real-time.  

To cope with all the above mentioned requirements, we propose a crop row detection algorithm consisting of the
following three linked stages:  
(1) projective transformation to transform camera view and color based segmentation for differentiating crop and weed from background,   
(2) differentiating crop and weed pixels using clustering algorithm and   
(3) robust line fitting to detect crop rows. 

Steps of the proposed CAROLIF algorithm:

<img src="https://github.com/sudokhan112/CAROLIF/blob/main/CAROLIF/1.png" width ="900" height="500">

(a) Projective transformation is used from Agricultural robot to transform camera 1 view to virtual camera 2 view. (b) For two camera planes, image planes are related by projective transformation when all world points are co-planer. (c) Original image from camera 1 view with boundary points. (d) Cropped image using boundary points. (e) Transformed cropped image from camera 1 view to camera 2 view.

<img src="https://github.com/sudokhan112/CAROLIF/blob/main/CAROLIF/2.png" width ="600" height="400">

Comparison of Kmeans, MeanShift, Agglomerative and HDBSCAN clustering algorithm on crop row detection. Run-time indicated on the top left corner of each image. Different colors indicate different clusters. Black colors indicate outliers

<img src="https://github.com/sudokhan112/CAROLIF/blob/main/CAROLIF/3.png" width ="600" height="400">

Performance of CAROLIF on real-time video captured from anagricultural vehicle.

<img src="https://github.com/sudokhan112/CAROLIF/blob/main/CAROLIF/4.png" width ="600" height="400">


**[Link to Paper](https://asmedigitalcollection.asme.org/IMECE/proceedings-abstract/IMECE2020/84553/V07BT07A003/1099261)**

**Citation**
```bash
Khan, N, Rajendran, VP, Al Hasan, M, and Anwar, S. 
"Clustering Algorithm Based Straight and Curved Crop Row Detection Using Color Based Segmentation." 
Proceedings of the ASME 2020 International Mechanical Engineering Congress and Exposition. Volume 7B: Dynamics, Vibration, and Control. Virtual, 
Online. November 16–19, 2020. V07BT07A003. ASME.
```
