

<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## A Simple Neural Network
  
**Exercise 1**  
Let **X = {x^(1), ..., x^(m)}** be a dataset of **m samples** with **2 features**. The samples are classified into 2 categories with labels **y^(i) ∈ {0, 1}**. A scatter plot of the dataset is shown below:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dataset_simpleNN.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dataset_simpleNN.png" title="Dataset simple NN" alt="Dataset simple NN" height="200"></a>  

&nbsp;  
In this exercise we want to we want to perform binary classification using a simple neural network with the architecture shown:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/arq_simpleNN.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/arq_simpleNN.png" title="Architecture simple NN" alt="Architecture simple NN" height="150"></a>

&nbsp;  
For the loss function, we’ll use **average squared loss** (instead of the usual negative log-likelihood), where *o^(i)* is the result of the output neuron for example *i*:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/AverageSquareLoss.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/AverageSquareLoss.png" title="Average Square Loss" alt="Average Square Loss" height="58"></a>    


&nbsp;  
**1.a)**  
Suppose we use the **sigmoid function** as the the activation function for **h1**, **h2**, **h3** and **o** and **α** is the learning rate. Let:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/l.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/l.png" title="l" alt="l" height="28"></a>  


&nbsp;  
Consider we want the gradient descent update to **w1,2^[1]**, then:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dl_1.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dl_1.png" title="dl" alt="dl" height="55"></a>  


&nbsp;  
That is:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dl_2.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dl_2.png" title="dl" alt="dl" height="55"></a>  

&nbsp;  
Now, lets compute the partial derivatives; The **l** function:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/l.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/l.png" title="l" alt="l" height="28"></a>  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dl_3.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dl_3.png" title="dl" alt="dl" height="45"></a>

&nbsp;  
The **output** function:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/output.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/output.png" title="output" alt="output" height="31"></a>  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/do.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/do.png" title="do" alt="do" height="55"></a>

&nbsp;  
The **h2** function:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/h2.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/h2.png" title="h2" alt="h2" height="40"></a>  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dh2.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/dh2.png" title="dh2" alt="dh2" height="60"></a>


&nbsp;  

Combining the equations, as shown in the [answer to the question 1.a](), we get the equation for gradient descent update:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/grad.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/grad.png" title="equation for gradient descent update" alt="equation for gradient descent update" height="60"></a>


&nbsp;  
**1.b)**  
Now, suppose instead of using the sigmoid function for the activation function for **h1**, **h2**, **h3** and **o**, we instead used the **step function** f(x), defined as:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/step_function.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/step_function.png" title="step function" alt="step function" height="61"></a>
  
As verified in the [answer to the question 2.a](), it is possible to have a set of weights that allow the neural network to classify the dataset with 100% accuracy. Three lines can be used to determine the decision boundary:  
**x1 = 0.5**   
**x2 = 0.5**  
**x1 + x2 = 4**  

if we make:  
**h1 = 1**, then **x1 ≤ 0.5**  
**h2 = 1**, then **x2 ≤ 0.5**  
**h3 = 1**, then **x1 + x2 ≤ 4**  
**o = 1** &nbsp;, then **h1 + h2 + h3 ≥ 1**  

Thus **o = 1** if and only if the points are not in the triangle region. The weights can then be determined using these equations.  

&nbsp;  
**1.c)**  
On the other hand, if we let the activation functions for *h1*, *h2*, *h3* be the **linear function** *f(x) = x* and the activation function for *o* be the same **step function** as before, it is not possible to have a set of weights that allow the neural network to classify the dataset with 100% accuracy.  
Note that in this case we have:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/h_step.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise1/img/h_step.png" title="h linear" alt="h lienar" height="59"></a>

The decision boundary will be a single line which cannot separate the two classes.


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
