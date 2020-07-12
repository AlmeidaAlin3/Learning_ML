
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
From the plots above we can see that only the dataset *B* is a perfectly linearly separable dataset; This is the reason why the model training on dataset *B* did not converge.
The model optimization goal is to maximize the likelihood estimation given by the equation:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/likelihood.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/likelihood.png" title="likelihood" alt="likelihood" height="65"></a>

The intuition is that large positive number means that x is likely to be positive (y = 1), and negative number means x is negative (y = 0):
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/sigmoid_func.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/sigmoid_func.png" title="sigmoid" alt="sigmoid" height="200"></a>

As the dataset is linearly separable, then for some optimal *θ* the term *(y * θ.T * x)* will always be positive. Remember that *θ* update rule is given by de equation:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/likelihood.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise1/img/likelihood.png" title="likelihood" alt="likelihood" height="65"></a>

So the algorithm 





&nbsp;  
**1.c)**  
the [answer to the question 1.c](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_c.md) shows that

&nbsp;  
**1.d)**  


&nbsp;  
**1.e)**  
The [code for the question 1.e](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet1/Exercise1/ex1_e.ipynb) used a **GDA** model to make predictions on the validation set. 

&nbsp;  
**1.f)**  


&nbsp;  
**1.g)**  


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
