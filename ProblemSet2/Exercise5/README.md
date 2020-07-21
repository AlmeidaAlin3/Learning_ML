
<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Kernelizing the Perceptron
  
**Exercise 5**  
Let there be a binary classification problem with **y** ∈ {0, 1}. The perceptron uses hypotheses of the form:  
**hθ(x) = g(θ.T . x)**, 

where:  
**g(z) = sign(z) = 1** if **z ≥ 0** or **0** otherwise.  

In this problem we will consider a stochastic gradient descent-like implementation of the perceptron algorithm where each update to the parameters *θ* is made
using only one training example. However, unlike stochastic gradient descent, the perceptron algorithm will only make one pass through the entire training set. The update rule for this version of the perceptron algorithm is given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/perceptron_update.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/perceptron_update.png" title="perceptron update rule" alt="perceptron update rule" height="35"></a> 

where *θ^(i)* is the value of the parameters after the algorithm has seen the first *i* training examples. Prior to seeing any training examples, *θ* is initialized to the vector of zeros.  

&nbsp;  
&nbsp;  
**5.a)**  
The answer to the question 5.a describes how to apply the *kernel trick* to the perceptron to make it work in high-dimensional feature space **φ**, but without ever explicity computing **φ(x)**. Specifically:  

**i)**    
The [answer 5.a.i]() shows how implicitly represent the high-dimensional parameter vector **θ^(i)**, including how the initial value **θ^(0) = 0** is represented.  

**ii)**   
The [answer 5.a.ii]() shows how efficiently make a prediction on a new input **x^(i+1)**.  

**iii)**  
The [answer 5.a.iii]() shows how to modify the update rule given to perform an update to **θ** on a new training example **( x^(i+1) , y^(i+1) )**.  

&nbsp;  
&nbsp;  
**5.b)**  
The [code for the question 5.b](https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/ex5_b.ipynb) implements the perceptron using the answers given in 5.a.  

&nbsp;  
&nbsp;  
**5.c)**   
Then we ran the perceptron using two kernels, a **dot product** kernel and an **radial basis function** (rbf) kernel. The plots are shown below:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/5c_plot_i.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/5c_plot_i.png" title="Dot-product kernel plot" alt="Dot-product kernel plot" height="200"></a>

*plot i) Dot-product kernel*  

&nbsp;  
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/5c_plot_i.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/5c_plot_i.png" title="Radial basis function kernel plot" alt="Radial basis function kernel plot" height="200"></a>  

*plot ii) Radial basis function kernel*

&nbsp;  
The dot-product kernel shown in the *plot i* performs extremely poorly in classifying the points beacuse using a dot-product is equivalent to use **φ(x^(i)) = x^(i)**, but the data is not linearly seperable.  


&nbsp;  

&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
