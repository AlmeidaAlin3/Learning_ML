

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
Using this fact, the [answer to the question 3.a]() shows that **the expected value of the score is 0**, that is:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/E_score.png.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/E_score.png" title="Score Expected Value" alt="Score Expected Value" height="36"></a>

&nbsp;  
Note:  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/score0.png.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/score0.png" title="Score Expected Value" alt="Score Expected Value" height="170"></a>

&nbsp;  
&nbsp;  
**3.b)**  
Let us now introduce a quantity known as the **Fisher information**. It is defined as the covariance matrix of the score function,  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher.png" title="Fisher information" alt="Fisher information" height="30"></a>

Intuitively, the Fisher information represents the amount of information that a random variable *Y* carries about a parameter *θ* of interest. When the parameter of interest is a vector (as in our case, since *θ* ∈ IRn ), this information becomes a matrix. The [answer to the question 3.b]() shows that Fisher information can equivalently be given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher_E.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher_E.png" title="Fisher information" alt="Fisher information" height="31"></a>

Note that the Fisher Information is a function of the parameter. The parameter of the Fisher information is both **the parameter value at which the score function is evaluated**, and **the parameter of the distribution with respect to which the expectation and variance is calculated**.

&nbsp;  
&nbsp;  
**3.c)**  
It turns out that the **Fisher Information** can not only be defined as the covariance of the score function, but in most situations it can also be represented as the **expected negative Hessian of the log-likelihood**:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher_H.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher_H.png" title="Fisher information" alt="Fisher information" height="35"></a>  

&nbsp;  
**Remark:** *The Hessian represents the curvature of a function at a point. This shows that the expected curvature of the log-likelihood function is also equal to the Fisher information matrix. If the curvature of the log-likelihood at a parameter is very steep (i.e, Fisher Information is very high), this generally means you need fewer number of data samples to a estimate that parameter well (assuming data was generated from the distribution with those
parameters), and vice versa. The Fisher information matrix associated with a statistical model parameterized by θ is extremely important in determining how a model behaves as a function of the number of training set examples.*


&nbsp;  
&nbsp;  
**3.d)**  
We are interested in the set of all distributions that are at a small fixed *DKL* distance away from the current distribution. In order to
calculate *DKL* between **p(y; θ)** and **p(y; θ+d)**, where **d** *∈ IRn* is a small magnitude “delta” vector, we approximate it using the Fisher Information at **θ**.  

Eventually **d** will be the **natural gradient** update we will add to **θ**. 

To approximate the KL-divergence with Fisher Information, we will start with the Taylor Series expansion of *DKL* and see that the Fisher
Information pops up in the expansion. The [answer to the question 3.d]() shows that:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/DKL_fisher.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/DKL_fisher.png" title="approximate the KL-divergence with Fisher Information" alt="Approximate the KL-divergence with Fisher Information" height="45"></a>  


&nbsp;  
&nbsp;  
**3.e)**  
Now we move on to calculating the **natural gradient**. Recall that we want to maximize the log-likelihood by moving only by a fixed *DKL* distance from the current position.  

In the previous sub-question we came up with a way to approximate *DKL* distance with Fisher Information. Now we will set up the constrained optimization problem that will yield the natural gradient update **d**.  

Let the log-likelihood objective be **ℓ(θ) = log p(y; θ)**. Let the *DKL* distance we want to move by, be some small positive constant **c**. The **natural gradient update** *d∗* is:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/d_star.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/d_star.png" title="natural gradient update d∗" alt="natural gradient update d∗" height="40"></a>  

subject to:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/DKL_c.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/DKL_c.png" title="DKL distance" alt="DKL distance" height="31"></a>

&nbsp;  
In order to solve this constrained optimization problem, we employ the method of **Lagrange multipliers**. Consider the following constrained optimization problem, where function **f** is the **objective function** and **g** is the **constraint**:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/d_star_lagr.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/d_star_lagr.png" title="natural gradient update d∗" alt="natural gradient update d∗" height="39"></a>  

subject to:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/cont_lagr.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/cont_lagr.png" title="constraint g" alt="constraint g" height="27"></a>

&nbsp;  
We instead optimize the **Lagrangian L(d, λ)** with respect to both **d** and **λ**, where **λ** *∈ IR+* is called the Lagrange multiplier. The Lagrangian is defined as:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/lagrange.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/lagrange.png" title="Lagrange" alt="Lagrange" height="30"></a>

&nbsp;  
In order to optimize the above, we construct the following system of equations:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/lagr_eqs.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/lagr_eqs.png" title="Lagrangian system of equations" alt="Lagrangian system of equations" height="55"></a>

So we have two equations with two unknowns **d** and **λ**, which can be sometimes be solved analytically (in our case, we can). The final final expression for **d∗** is given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/d_star_final.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/d_star_final.png" title="Final expression for d ∗" alt="Final expression for d ∗" height="75"></a>

&nbsp;  
&nbsp;  
**3.f)**   
Finally, we will see how this new natural gradient based optimization is actually equivalent to Newton’s method for Generalized Linear Models. 

The natural gradient update rule is given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/natural_gradient_update.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/natural_gradient_update.png" title="Natural gradient update rule" alt="Natural gradient update rule" height="28"></a>

And Newton’s rule gives

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/newtons_update_rule.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/newtons_update_rule.png" title="Newtons rule update" alt="Newtons rule update" height="30"></a>

Note that

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher-1.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/fisher-1.png" title="fisher^-1" alt="Fisher^-1" height="30"></a>

As we know, in generalized linear model, *H* is only dependent on *x* but not *y*. So:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/same_direction.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise3/img/same_direction.png" title="Same direction" alt="Same direction" height="27"></a>

That is, the **direction of update** of Newton’s method, and the direction of natural gradient, **are exactly the same** for Generalized Linear Models. While the two methods agree on GLMs, in general they need not be equivalent.


&nbsp;  

&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 

