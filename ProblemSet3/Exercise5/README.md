<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## K-means for compression
  
**Exercise 5**  
In this exercise, we will apply the K-means algorithm to lossy image compression, by reducing the number of colors used in an image. We will be using the *peppers-small.tiff* and *peppers-large.tiff*.  

The *peppers-large.tiff* file contains a 512x512 image of peppers represented in 24-bit color. This means that, for each of the 262144 pixels in the image, there are three 8-bit numbers (each ranging from 0 to 255) that represent the red, green, and blue intensity values for that pixel. The straightforward representation of this image therefore takes about *262144 × 3 = 786432 bytes* (a byte being 8 bits).  

To compress the image, we will use K-means to reduce the image to k=16 colors. More specifically, each pixel in the image is considered a point in the three-dimensional (r, g, b)-space. We will cluster these points in color-space into 16 clusters, and replace each pixel with the closest cluster centroid.

&nbsp; 
&nbsp;  
**5.a)**  
...
(a) [15 points] [Coding Problem] K-Means Compression Implementation. From the
data directory, open an interactive Python prompt, and type
from matplotlib.image import imread; import matplotlib.pyplot as plt;
and run A = imread(’peppers-large.tiff’). Now, A is a “three dimensional matrix,”
and A[:,:,0], A[:,:,1] and A[:,:,2] are 512x512 arrays that respectively contain the
red, green, and blue values for each pixel. Enter plt.imshow(A); plt.show() to display
the image.
Since the large image has 262144 pixels and would take a while to cluster, we will instead run
vector quantization on a smaller image. Repeat (a) with peppers-small.tiff. Treating
each pixel’s (r, g, b) values as an element of R 3 , run K-means 2 with 16 clusters on the pixel
data from this smaller image, iterating (preferably) to convergence, but in no case for less
than 30 iterations. For initialization, set each cluster centroid to the (r, g, b)-values of a
randomly chosen pixel in the image.
Take the matrix A from peppers-large.tiff, and replace each pixel’s (r, g, b) values with
the value of the closest cluster centroid. Display the new image, and compare it visually
to the original image. Include in your write-up all your code and a copy of your
compressed image.

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise5/xx/.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise5/img/xx.png" title="xx" alt="xx" height="125"></a>


&nbsp; 
&nbsp;  
**5.b)**  

(b) [5 points] Compression Factor. If we represent the image with these reduced (16) colors,
by (approximately) what factor have we compressed the image?
Answer: Each pixel can now be represented as a 4-bit color versus 24-bit. So compression
rate is approximately 1/6.



&nbsp;  
&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 


