
<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Logistic Regression: Training stability
  
**Exercise 1**  
The goal of this exercise is to delve deeper into the workings of logistic regression and to develop the skills in debugging machine learning algorithms.

&nbsp;  
**1.a)**  
This exercise provided a [implementation of logistic regression](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/ex1_a.ipynb) that were ran using two labeled datasets *A* and *B*. The most notable difference in training the model on these datasets were that the training on dataset *A* finished with few iterations, while *B* did not converge.

&nbsp;  
**1.b)**  
The Datasets *A* and *B* plots are shown below:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/A_plot.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/A_plot.png" title="Dataset A" alt="Dataset A" height="200"></a>  
*plot i) Dataset A*

&nbsp;  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/B_plot.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/B_plot.png" title="Dataset B" alt="Dataset B" height="200"></a>  
*plot ii) Dataset B*

&nbsp;  
From the two plots above we can see that only the dataset *B* is perfectly linearly separable; This is the reason why the model training did not converge. Remember that the model optimization goal is to maximize the likelihood estimation given by the equation:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/likelihood.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/likelihood.png" title="likelihood" alt="likelihood" height="65"></a>

As the dataset is linearly separable, then for some optimal *θ* the term *(y * θ.T * x)* will always be positive. It means that *θ* can be multiplied by a larger scalar to get larger *L(θ)*, therefore there are nor only, but infinite number of maximum likelihood estimations.  

&nbsp;  
**1.c)**   
Let's verify the proposed solutions. Would it lead to provided training algorithm converging on datasets such as *B*?  
&nbsp;  
**i)** *Using a **different constant** learning rate*  

No, It would not solve the problem of convergence since *L(θ)* could still be arbitrarily large.  

&nbsp;  
**ii)** **Decreasing the learning rate over time**, *for example scaling the initial learning rate by **1/t²**, where **t** is the number of gradient descent iterations thus far*  

Yes, when the learning rate is sufficiently small, the update to *θ* would be also very small, and it will be judged as converged by the algorithm.  

&nbsp;  
**iii)** **Linear scaling** *of the input features*  

No, it would not help since the dataset would still be linearly seperable.  

&nbsp;  
**iv)** *Adding a **regularization term** ||θ||² to the loss function*  

Yes, adding a regularization term would penalize the model for larger values of *θ*, so it could not assume arbitrarily large values.  

&nbsp;  
**v)** *Adding **zero-mean Gaussian noise** to the training data or labels*  

Yes, It would very likely make the dataset not linearly seperable.  


&nbsp;  
**1.d)**  
The Support Vector Machines are **not** vulnerable to datasets like *B*, because it's objective is directly associated to geometric margins which is independent with the scaling of *θ*.  


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
