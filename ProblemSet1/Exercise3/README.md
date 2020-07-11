<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Poisson Regression  
  
**Exercise 3**  
The goal of this problem is to explore Poisson distribution.   

&nbsp;  
**3.a)**  
Consider the Poisson Distribution given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson.png" title="Poisson" alt="Poisson" height="55"></a>

The [answer to the question 3.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_a.md) shows that the Poisson distribution is in the exponential family.

&nbsp;  
**3.b)** 
Consider performing regression using GLM with Poisson response variable. The [answer to the question 3.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_b.md) shows that the canonical response function for the family is:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_canonical.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_canonical.png" title="Poisson Canonical response" alt="Poisson Canonical response" height="30"></a>

**3.c)** 
The [answer to the question 3.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_c.md) derives the stochastic gradient ascent update rule for learning using a GLM model with Poisson responses y. The update rule is given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_update.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_update.png" title="Poisson update rule" alt="Poisson update rule" height="30"></a>



For a training set {(x (i) , y (i) ); i = 1, . . . , m}, let the log-likelihood of an example
be log p(y (i) |x (i) ; θ). By taking the derivative of the log-likelihood with respect to θ j , derive
the stochastic gradient ascent update rule for learning using a GLM model with Poisson
responses y and the canonical response function.

Consider performing regression using GLM with Poisson response variable. The [answer to the question 3.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_b.md) shows that the canonical response function for the family is:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_canonical.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_canonical.png" title="Poisson Canonical response" alt="Poisson Canonical response" height="30"></a>

&nbsp;  
**3.c)**  
The [code for the question 2.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex2_c.ipynb) ...:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/2e_plot.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/2e_plot.png" title="" alt="" height="200"></a>


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
