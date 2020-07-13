<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Convexity of Generalized Linear Models  
  
**Exercise 4**  
In this exercise we will explore and show some nice properties of Generalized Linear Models, specifically those related to its use of Exponential Family distributions to model the output. Most commonly, GLMs are trained by using the negative log-likelihood (NLL) as the loss function. This is mathematically equivalent to Maximum Likelihood Estimation (i.e., maximizing the log-likelihood is equivalent to minimizing the negative log-likelihood). 

In this problem, our goal is to show that the NLL loss of a GLM is a convex function w.r.t the model parameters. As a reminder, this is convenient because a convex function is one for which any local minimum is also a global minimum.

An exponential family distribution is one whose probability density can be represented as:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/GLM.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/GLM.png" title="GLM" alt="GLM" height="26"></a>
&nbsp;  

If *η* is scalar and *T(y)=y* the exponential family representation take the form:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/GLMsub.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/GLMsub.png" title="GLM subgroup" alt="GLM subgroup" height="29"></a>

where *η* is the natural parameter of the distribution. Moreover, in a Generalized Linear Model, **η** is modeled as **(θ.T).x**, where *x ∈ IRd* are the input features of the example, and *θ ∈ IRd* are learnable parameters. 


&nbsp;  
**4.a)**  
The [answer to the question 4.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/ex4_a.md) derives the expression for *E[Y|X;θ]* expressed as the gradient of the log-partition function *a* w.r.t the natural parameter *η*:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/function_a.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/function_a.png" title="Log-partition function a wrt the natural parameter n" alt="Log-partition function a wrt the natural parameter n" height="26"></a>

&nbsp;  
**4.b)**  
The [answer to the question 4.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/ex4_b.md) derives the expression for the *Var(Y|X;θ)* expressed as the derivative of the mean w.r.t the natural parameter *η*:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/var_func.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/img/var_func.png" title="Variance function wrt the natural parameter n" alt="Variance function wrt the natural parameter n" height="26"></a>

Questions **4.a** and **4.b** shows that whereas calculating mean and variance of distributions in general involves integrals (hard), surprisingly we can calculate them using derivatives (easy) for exponential family.

&nbsp;  
**4.c)**  
The [answer to the question 4.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/ex4_c.md) write out the loss function *ℓ(θ)*, the NLL of the distribution, as a function of *θ*. Then, calculates the Hessian of the loss with respect to *θ*, and show that it is always PSD. This proves that any GLM model is convex in its model parameters and thus have no local minima.
&nbsp;  
&nbsp;  

&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
