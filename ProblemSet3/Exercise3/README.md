

<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## KL Divergence, Fisher Information, and the Natural Gradient
  
**Exercise 3**  
As seen before, the Kullback-Leibler divergence between two distributions is an asymmetric measure of how different two distributions are. Consider two distributions over the same space given by densities *p(x)* and *q(x)*. The KL divergence between two **continuous distributions**, *q* and *p* is defined as,

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/DKL_continuous.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/DKL_continuous.png" title="DKL continuous" alt="DKL continuous" height="160"></a>

A nice property of KL divergence is that it **invariant to parametrization**. This means, KL divergence evaluates to the same value no matter how we parametrize the distributions *P* and *Q*. For example, if *P* and *Q* are in the exponential family, the KL divergence between them is the same whether we are using natural parameters, or canonical parameters, or any arbitrary reparametrization.  

&nbsp;  
Now we consider the problem of fitting model parameters using **gradient descent** (or stochastic gradient descent). As seen previously, fitting model parameters using Maximum Likelihood is equivalent to minimizing the KL divergence between the data and the model.  

While **KL divergence is invariant to parametrization**, the **gradient** w.r.t the model parameters (i.e, direction
of steepest descent) **is not invariant to parametrization**.

To see its implication, suppose we are at a particular value of parameters (either randomly initialized, or mid-way through the optimization process). The value of the parameters correspond to some probability distribution (and in case of regression, a conditional probability distribution).  

If we follow the direction of steepest descent from the current parameter, take a small step along that direction to a new parameter, we end up with a new distribution corresponding to the new parameters.  

The **non-invariance** to reparametrization means, a step of fixed size in the parameter space could end up in a distribution that could either be extremely far away in DKL from the previous distribution, or on the other hand not move very much at all w.r.t DKL from the previous distributions.  

&nbsp;  
This is where the **natural gradient** comes into picture.
&nbsp;  

In the usual **gradient descent**, we first choose the direction by calculating the gradient of the MLE objective w.r.t the parameters, and then move a magnitude of step size (where size is measured in the parameter space) along that direction.  

Whereas in **natural gradient**, we first choose a divergence amount by which we would like to move, in the DKL sense. This effectively gives us a perimeter around the current parameters (of some arbitrary shape), such that points along this perimeter correspond to distributions which are at an equal DKL-distance away from the current parameter. Among the set of all distributions along this perimeter, we move to the distribution that maximizes the objective (i.e minimize DKL between data and itself) the most.  

This approach makes the optimization process invariant to parametrization. That means, even if we chose a new arbitrary reparametrization, by starting from a particular distribution, we always descend down the same sequence of distributions towards the optimum.

&nbsp;  
&nbsp;  
**3.a)**  
The **score function** associated with **p(y;θ)** is defined as:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/score_function.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/score_function.png" title="Score Function" alt="Score Function" height="28"></a>

which signifies the sensitivity of the likelihood function with respect to the parameters. Note that the score function is actually a vector since it’s the gradient of a scalar quantity with respect to the vector *θ*.

Recall that:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/E_g(y).png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/E_g(y).png" title="E_g(y)" alt="E_g(y)" height="32"></a>

&nbsp;  
Using this fact, the [answer for the question 3.a]() shows that **the expected value of the score is 0**, that is:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/E_score.png.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/E_score.png" title="Score Expected Value" alt="Score Expected Value" height="36"></a>

&nbsp;  
Note:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/score0.png.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/score0.png" title="Score Expected Value" alt="Score Expected Value" height="180"></a>

&nbsp;  
&nbsp;  
Finally, we will see how this new natural gradient based optimization is actually equivalent to
Newton’s method for Generalized Linear Models.

&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 

