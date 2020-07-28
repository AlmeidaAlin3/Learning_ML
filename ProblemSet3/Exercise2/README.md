

<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## KL divergence and Maximum Likelihood
  
**Exercise 2**  

The **Kullback-Leibler divergence** is a measure of how much one probability distribution is different from a second one. In this problem, we will introduce KL divergence over discrete distributions, practice some simple manipulations, and see its connection to **Maximum Likelihood Estimation**.  

The **KL divergence** between two discrete-valued distributions *P(X)*, *Q(X)* over the outcome space *X* is defined as follows:
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL.png" title="Kullback-Leibler divergence" alt="Kullback-Leibler divergence" height="50"></a>

&nbsp;  

Before we dive deeper, we give a brief **Information Theoretic background** on KL divergence. We start with the **entropy** *H(P)* of a probability distribution *P(X)*, which is defined as:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/Entropy.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/Entropy.png" title="Entropy" alt="Entropy" height="50"></a>

Intuitively, entropy measures how dispersed a probability distribution is. For example, a **uniform distribution** is considered to have **very high entropy** (i.e. a lot of uncertainty), whereas a distribution that assigns all its mass on a **single point** is considered to have **zero entropy** (i.e. no uncertainty).  

Notably, it can be shown that among continuous distributions over IR, the **Gaussian distribution** *N(μ, σ²)* has the **highest entropy** (highest uncertainty) among all possible distributions that have the given mean μ and variance σ².




&nbsp;  
**2.a)**  
...


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 

