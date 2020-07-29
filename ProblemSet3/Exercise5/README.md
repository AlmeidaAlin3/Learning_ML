<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## K-means for compression
  
**Exercise 5**  
In this exercise, we will apply the K-means algorithm to lossy image compression, by reducing the number of colors used in an image. We will be using the peppers-small.tiff and peppers-large.tiff.  

The peppers-large.tiff file contains a 512x512 image of peppers represented in 24-bit color. This means that, for each of the 262144 pixels in the image, there are three 8-bit numbers (each ranging from 0 to 255) that represent the red, green, and blue intensity values for that pixel. The straightforward representation of this image therefore takes about *262144 × 3 = 786432 bytes* (a byte being 8 bits).  

To compress the image, we will use K-means to reduce the image to k=16 colors. More specifically, each pixel in the image is considered a point in the three-dimensional (r, g, b)-space. We will cluster these points in color-space into 16 clusters, and replace each pixel with the closest cluster centroid.









<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise5/xx/.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise5/img/xx.png" title="xx" alt="xx" height="125"></a>

&nbsp; 
&nbsp;  
**5.a)**  
...




&nbsp;  
&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 


