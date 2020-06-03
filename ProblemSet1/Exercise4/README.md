<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Convexity of Generalized Linear Models  
  
**Exercise 4**  
The goal in this exercise is to show that the NLL loss of a GLM is a convex function w.r.t the model parameters.  
As a reminder, this is convenient because a convex function is one for which any local minimum is also a global minimum.

&nbsp;  
**4.a)**  
The [solution of question 4.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/ex4_a.md) derives an expression for E[Y|X;θ] represented as the gradient of the log-partition function a with respect to the natural parameter η. 

&nbsp;  
**4.b)**  
The [solution of question 4.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/ex4_b.md) derives an expression for the Var(Y|X;θ) expressed as the derivative of the mean with respect to the natural parameter η. 

Questions **4.a** and **4.b** shows that whereas calculating mean and variance of distributions in general involves integrals (hard), surprisingly we can calculate them using derivatives (easy) for exponential family.

&nbsp;  
**4.c)**  
The [solution of question 4.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise4/ex4_c.md) write out the loss function l(θ), the NLL of the distribution, as a function of θ. 
Then, calculates the Hessian of the loss with respect to θ, and show that it is always PSD. 
This proofs that any GLM model is convex in its model parameters and thus have no local minima.

  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
