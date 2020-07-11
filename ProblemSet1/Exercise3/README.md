<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Poisson Regression  
  
**Exercise 3**  
In this problem we will consider training binary classifiers in situations where we do not have full access to the labels. In particular, we consider a scenario where we have labels only for a subset of the positive examples. All the negative examples
and the rest of the positive examples are unlabelled.  

&nbsp;  
**2.a)**  
Suppose that each y^(i) and x^(i) are conditionally independent given t^(i). Note this is equivalent to saying that labeled examples were selected uniformly at random
from the set of positive examples. The [answer to the question 2.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex2_a.md) proves that the probability of an example being labeled differs by a constant factor from the probability of an example being positive.  
That is:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/alpha.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/alpha.png" title="alpha" alt="alpha" height="30"></a>

&nbsp;  
**2.b)**  
Suppose we want to estimate *alpha* using a trained classifier *h* and a held-out validation set *V*. Let *V+* be the set of labeled (and hence positive) examples in V. Assuming that *h(x^(i))* is aproximatelly *p(y^(i)=1 | x^(i))*, for all examples *x^(i)*, the [answer to the question 2.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex2_a.md) shows that: 

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/h_alpha.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/h_alpha.png" title="h(alpha)" alt="h(alpha)" height="30"></a>

&nbsp;  
**2.c)**  
The [code for the question 2.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex2_c.ipynb) ...:  

&nbsp;  
**2.d)**  
The [code for the question 2.d](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex2_d.ipynb) ...: 

&nbsp;  
**2.e)**  
The [code for the question 2.e](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex2_e.ipynb) ...: 

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/2e_plot.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/img/2e_plot.png" title="" alt="" height="200"></a>


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 