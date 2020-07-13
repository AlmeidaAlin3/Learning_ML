<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Linear Classifiers (logistic regression and GDA)  
  
**Exercise 1**  
The goal in this exercise is to get a deeper understanding of the similarities and differences (and strengths and weaknesses) of two probabilistic linear classifiers. First, a discriminative linear classifier: **logistic regression**. Second, a generative linear classifier: **Gaussian discriminant analysis** (GDA). A Discriminative model models the decision boundary between the classes. A Generative Model explicitly models the actual distribution of each class. Both the algorithms find a linear decision boundary that separates the data into two classes, but make different assumptions.  

&nbsp;  
**1.a)**  
Given J(θ), the average empirical loss for logistic regression

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/LR_loss.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/LR_loss.png" title="LR loss" alt="LR loss" height="50"></a>

the [answer to the question 1.a](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_a.md) shows that the Hessian matrix of J(θ) is **positive semidefinite**; this implies that J(θ) is convex and has no local minima other than global one.  

&nbsp;  
**1.b)**  
The [code for the question 1.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_b.ipynb) trained a **regression** classifier using Newton's Method, starting with θ=0, until the error become smaller than 1x10^-5. The decision boundary that separates the data into two classes is shown below:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1b_plot.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1b_plot.png" title="Logistic regression plot" alt="Logistic regression plot" height="200"></a>

&nbsp;  
**1.c)**  
In GDA the joint distribution of *(x, y)* by the following equations:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA.png" title="GDA joint distribution" alt="GDA joint distribution" height="150"></a>

Suppose we have already fit the parameters of our model and now want to predict *y* given a new point *x*. To show that GDA results in a classifier that has a linear decision boundary, the [answer to the question 1.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_c.md) shows that,  the posterior distribution can be written as:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDAposterior.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDAposterior.png" title="GDA posterior distribution" alt="GDA posterior distribution" height="43"></a>

So, we can take:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDAtheta.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDAtheta.png" title="GDA theta" alt="GDA theta" height="40"></a>
 

&nbsp;  
**1.d)**  
Considering the dimension of *x* is *d = 1*, the maximum likelihood estimates of the parameters are given by:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA_likelihood_params.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA_likelihood_params.png" title="GDA likelihood parameters" alt="GDA likelihood parameters" height="200"></a>

As shown in the [answer to the question 1.d](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_d.md), by maximizing *ℓ* with respect to the four parameters, the log-likelihood of the data is:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA_log_likelihood.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA_log_likelihood.png" title="GDA log-likelihood" alt="GDA log-likelihood" height="50"></a>

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA_log_likelihood_sums.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/GDA_log_likelihood_sums.png" title="GDA log-likelihood" alt="GDA log-likelihood" height="50"></a>

&nbsp;  
**1.e)**  
The [code for the question 1.e](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_e.ipynb) used a **GDA** model to make predictions on the validation set. The decision boundary that separates the data into two classes is shown below:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1e_plot.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1e_plot.png" title="GDA model plot" alt="GDA model plot" height="200"></a>

&nbsp;  
**1.f)**  
Here are shown the plots using Dataset2:  
 
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1b_plot2.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1b_plot2.png" title="Logistic regression plot" alt="Logistic regression plot" height="200"></a>  
plot i) Logistic regression

&nbsp;  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1e_plot2.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/img/1e_plot2.png" title="GDA model plot" alt="GDA model plot" height="200"></a>  
plot ii) GDA  

&nbsp;  
**1.g)**  
GDA does seem to perform worse than logistic regression on Dataset1 because the distribution of this dataset is not gaussian.

&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
