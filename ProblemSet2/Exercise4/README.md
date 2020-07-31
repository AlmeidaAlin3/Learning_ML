
<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Constructing kernels
  
**Exercise 4**  
In class, we saw that by choosing a kernel **K(x, z) = φ(x).T . φ(z)**, we can implicitly map data to a high dimensional space, and have the SVM algorithm work in that space. One way to generate kernels is to explicitly define the mapping **φ** to a higher dimensional space, and then work out the corresponding **K**.  

However in this question we are interested in direct construction of kernels. I.e., suppose we have a function *K(x, z)* that we think gives an appropriate similarity measure for our learning problem, and we are considering plugging *K* into the SVM as the kernel function. However for *K(x, z)* to be a valid kernel, it must correspond to an inner product in some higher dimensional space resulting from some feature mapping *φ*. Mercer’s theorem tells us that **K(x, z)** is a (Mercer) kernel if and only if for any finite set **{ x^(1), ... , x^(m) }**, the square matrix **K** ∈ IRm×m* whose entries are given by **Kij = K(x^(i), x^(j) )** is **symmetric and positive semidefinite**.  

For this exercise:   

Let **K1**, **K2** be kernels over IRn × IRn ;  
Let **a** ∈ IR+ be a positive real number;  
Let **f**: IRn → R be a real-valued function;  
Let **φ**: IRn → IRd be a function mapping from IRn to IRd;  
Let **K3** be a kernel over IRd × IRd;  
Let **p(x)** a polynomial over **x** with positive coefficients.   

For each of the functions **K** below, state whether it is necessarily a kernel. If you think it is,
prove it; if you think it isn’t, give a counter-example.

&nbsp;  
&nbsp;  
**4.a)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4a.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4a.png" title="4a" alt="4a" height="24"></a> 

**Yes**, it is a kernel. It is proved in the [solution 4.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_a.md).  

&nbsp;  
&nbsp;  
**4.b)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4b.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4b.png" title="4b" alt="4b" height="24"></a> 

**No**, it is not a valid kernel. A counter-example is given in the [solution 4.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_b.md).


&nbsp;  
&nbsp;  
**4.c)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4c.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4c.png" title="4c" alt="4c" height="24"></a> 

**Yes**, it is a kernel. It is proved in the [solution 4.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_c.md).

&nbsp;  
&nbsp;  
**4.d)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4d.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4d.png" title="4d" alt="4d" height="24"></a> 

**No**, it is not a valid kernel. A counter-example is given in the [solution 4.d](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_d.md).

&nbsp;  
&nbsp;  
**4.e)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4e.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4e.png" title="4e" alt="4e" height="24"></a> 

**Yes**, it is a kernel. It is proved in the [solution 4.e](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_e.md).

&nbsp;  
&nbsp;  
**4.f)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4f.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4f.png" title="4f" alt="4f" height="24"></a> 

**Yes**, it is a kernel. It is proved in the [solution 4.f](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_f.md).

&nbsp;  
&nbsp;  
**4.g)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4g.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4g.png" title="4g" alt="4g" height="24"></a> 

**Yes**, it is a kernel. It is proved in the [solution 4.g](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_g.md).

&nbsp;  
&nbsp;  
**4.h)**  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4h.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/img/4h.png" title="4h" alt="4h" height="24"></a> 

**Yes**, it is a kernel. It is proved in the [solution 4.h](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise4/ex4_h.md).


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
