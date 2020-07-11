<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Poisson Regression  
  
**Exercise 3**  
The goal of this problem is to explore Poisson distribution which distribution given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson.png" title="Poisson" alt="Poisson" height="55"></a>   

&nbsp;  
**3.a)**  
The [answer to the question 3.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_a.md) shows that the Poisson distribution is in the exponential family.

&nbsp;  
**3.b)**  
Consider performing regression using GLM with Poisson response variable. The [answer to the question 3.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_b.md) shows that the canonical response function for the family is:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_canonical.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_canonical.png" title="Poisson Canonical response" alt="Poisson Canonical response" height="30"></a>

&nbsp;  
**3.c)**  
The [answer to the question 3.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/ex3_c.md) derives the stochastic gradient ascent update rule for learning using a GLM model with Poisson responses y. The update rule is given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_update.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise3/img/poisson_update.png" title="Poisson update rule" alt="Poisson update rule" height="30"></a>

&nbsp;  
**3.d)**  
Consider a website that wants to predict its daily traffic. The website owners have collected a dataset of past traffic to their website, along with
some features which they think are useful in predicting the number of visitors per day. We will apply Poisson regression to model the number of visitors per day. Note that applying Poisson regression in particular assumes that the data follows a Poisson distribution whose natural parameter is a linear combination of the input features (i.e., *η = θ.T.x*).  
The [code for the question 3.d](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise2/ex3_d.ipynb) implements the Poisson regression and use gradient ascent to maximize the log-likelihood of *θ*.


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
