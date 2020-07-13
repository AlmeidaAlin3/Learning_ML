<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Locally weighted linear regression  

**Exercise 5**  
The goal of this exercise is to generalize the linear regression problem to the weighted setting and explore how the bandwidth value changes the model predictions.

&nbsp;  
**5.a.i)**  
Consider a linear regression problem in which we want to “weight” different training examples differently. Specifically, suppose we want to minimize:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/cost_locally_weighted1.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/cost_locally_weighted1.png" title="Cost function for Locally Weighted Linear Regression" alt="Cost function for Locally Weighted Linear Regression" height="60"></a>

As shown in the [answer to the question 5.a.i](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/ex5_a_i.md), it can also be written as:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/cost_locally_weighted.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/cost_locally_weighted.png" title="Cost function for Locally Weighted Linear Regression" alt="Cost function for Locally Weighted Linear Regression" height="31"></a>

where:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/Wij.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/Wij.png" title="weight matrix" alt="weight matrix" height="65"></a>

&nbsp;  
**5.a.ii)**  
For linear regression, *θ* that minimizes *J(θ)*:  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/theta_normalEq_linreg.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/theta_normalEq_linreg.png" title="Linear Regression normal equation (solved for theta)" alt="Linear Regression normal equation (solved for theta)" height="26"></a>

For a locally weighted linear regression, *θ* that minimizes *J(θ)* (as shown in the [answer to the question 5.a.ii](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/ex5_a_ii.md))  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/theta_normalEq_locally_weighted.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/theta_normalEq_locally_weighted.png" title="Locally Weighted Linear Regression normal equation (solved for theta)" alt="Locally Weighted Linear Regression normal equation (solved for theta)" height="29"></a>


&nbsp;  
**5.a.iii)**  
For a dataset with *n* independent samples, suppose we model the values of *y* as drawn from conditional distributions with different levels of variance *σ²*.  
Specifically:  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/conditional_dist.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/conditional_dist.png" title="Conditional distribution model" alt="Conditional distribution model" height="55"></a>  
That is, each *y* is drawn from a Gaussian distribution with mean *θ^T.x* and variance *σ²* (where the *σ*’s are fixed, known, constants)
&nbsp;  
&nbsp;  
 
As shown in the [answer to the question 5.a.iii](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/ex5_a_iii.md), finding the maximum likelihood estimate of *θ* reduces to solving a weighted linear regression problem:  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/max_likelihood.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/max_likelihood.png" title="Maximum likelihood estimate of θ" alt="Maximum likelihood estimate of θ" height="90"></a>

&nbsp;  
**5.b)** 
The [code for the question 4.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/ex5_b.ipynb) trained a Locally Weighted Linear Regression using the bandwidth *τ=10*. The model predictions (red) and the actual dataset (blue) is shown below:  
&nbsp;  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/5b.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/5b.png" title="Linear Weighted Regression predicitons" alt="Linear Weighted Regression predicitons" height="200"></a>  
As we can see, the model predictions are underfiting the data.

&nbsp;  
**5.c)** 
The [code for the question 4.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/ex5_c.ipynb) compares model predictions using different values of *τ*.  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p03.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p03.png" title="Linear Weighted Regression predicitons for different tau values" alt="Linear Weighted Regression predicitons for different tau values" height="200"></a>  


<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p05.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p05.png" title="Linear Weighted Regression predicitons for different tau values" alt="Linear Weighted Regression predicitons for different tau values" height="200"></a>  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p1.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p1.png" title="Linear Weighted Regression predicitons for different tau values" alt="Linear Weighted Regression predicitons for different tau values" height="200"></a>  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p5.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau0p5.png" title="Linear Weighted Regression predicitons for different tau values" alt="Linear Weighted Regression predicitons for different tau values" height="200"></a>  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau1.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau1.png" title="Linear Weighted Regression predicitons for different tau values" alt="Linear Weighted Regression predicitons for different tau values" height="200"></a>  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau10.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise5/img/tau10.png" title="Linear Weighted Regression predicitons for different tau values" alt="Linear Weighted Regression predicitons for different tau values" height="200"></a> 

***τ=0.05*** achieved the best result with **MSE=0.017** in the test set.

&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
