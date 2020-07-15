
<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Kernelizing the Perceptron
  
**Exercise 5**  
Let there be a binary classification problem with **y** ∈ {0, 1}. The perceptron uses hypotheses of the form:  
**hθ(x) = g(θ.T . x)**, 

where: **g(z) = sign(z) = 1** if **z ≥ 0** or **0** otherwise.  

In this problem we will consider a stochastic gradient descent-like implementation of the perceptron algorithm where each update to the parameters *θ* is made
using only one training example. However, unlike stochastic gradient descent, the perceptron algorithm will only make one pass through the entire training set. The update rule for this version of the perceptron algorithm is given by:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/perceptron_update.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise5/img/perceptron_update.png" title="perceptron update rule" alt="perceptron update rule" height="35"></a> 

where *θ^(i)* is the value of the parameters after the algorithm has seen the first *i* training examples. Prior to seeing any training examples, *θ* is initialized to the vector of zeros.

**4.a)**  




&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
