

<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## KL divergence and Maximum Likelihood
  
**Exercise 2**  

The **Kullback-Leibler divergence** is a measure of how much one probability distribution is different from a second one. In this problem, we will introduce KL divergence over discrete distributions, practice some simple manipulations, and see its connection to **Maximum Likelihood Estimation**.  

The **KL divergence** between two discrete-valued distributions *P(X)*, *Q(X)* over the outcome space *X* is defined as follows:
<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL.png" title="Kullback-Leibler divergence" alt="Kullback-Leibler divergence" height="50"></a>

&nbsp;  

Before we dive deeper, we give a brief **Information Theoretic background** on KL divergence. We start with the **entropy** *H(P)* of a probability distribution *P(X)*, which is defined as:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/Entropy.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/Entropy.png" title="Entropy" alt="Entropy" height="47"></a>

Intuitively, entropy measures how dispersed a probability distribution is. For example, a **uniform distribution** is considered to have **very high entropy** (i.e. a lot of uncertainty), whereas a distribution that assigns all its mass on a **single point** is considered to have **zero entropy** (i.e. no uncertainty).  

Notably, it can be shown that among continuous distributions over IR, the **Gaussian distribution** *N(μ, σ²)* has the **highest entropy** (highest uncertainty) among all possible distributions that have the given mean μ and variance σ².  

&nbsp;  

*Motivation from comunication theory:*  

*Suppose we want to communicate from a source to a destination, and our messages are always a sequence of discrete symbols over space X (for example, X could be letters {a, b, . . . , z}). We want to construct an encoding scheme for our symbols in the form of sequences of binary bits that are
transmitted over the channel. Further, suppose that in the long run the frequency of occurrence of symbols follow a probability distribution P(X). This means, in the long run, the fraction of times the symbol x gets transmitted is P(x).*  

*A common desire is to construct an encoding scheme such that the average number of bits per symbol transmitted remains as small as possible. Intuitively, this means we want very frequent symbols to be assigned to a bit pattern having a small number of bits. Likewise, because we are interested in reducing the average number of bits per symbol in the long term, it is tolerable for infrequent words to be assigned to bit patterns having a large number of bits, since their low frequency has little effect on the long term average.*  

*The **entropy** of a probability distribution P(X) is its **optimal bit rate**, i.e., the lowest average bits per message that can possibly be
achieved if the symbols x ∈ X occur according to P(X). It does not specifically tell us how to construct that optimal encoding scheme. It only tells us that no encoding can possibly give us a lower long term bits per message than H(P).*  

*To see a concrete example, suppose our messages have a vocabulary of K = 32 symbols, and each symbol has an equal probability of transmission in the long term (i.e, uniform probability distribution). An encoding scheme that would work well for this scenario would be to have log2(K) bits per symbol, and assign each symbol some unique combination of the log2(K) bits. In fact, it turns out that this is the most efficient encoding one can come up with for the uniform distribution scenario.*

*The encoding scheme designed to be **optimal** for scenario A can in theory be reused in scenario B with a different set of symbols (assume equal vocabulary size for simplicity), with the **same long term efficiency**, as long as the symbols of scenario B follow the **same probability distribution** as the symbols of scenario A*  

*Reusing the encoding scheme designed to be optimal for scenario A, for messages in scenario B having a **different probability distribution** of symbols, will always be **suboptimal** for scenario B. To be clear, we do not need know what the specific optimal schemes are in either scenarios. As long as we know the distributions of their symbols, we can say that* **the optimal scheme designed for scenario A will be suboptimal for scenario B if the distributions are different.**  

&nbsp;  

Concretely, if we reuse the optimal scheme designed for a scenario having symbol distribution *Q(X)*, into a scenario that has symbol distribution *P(X)*, the long term average number of bits per symbol achieved is called the **cross entropy**, denoted by *H(P,Q)*:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/cross_entropy.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/cross_entropy.png" title="Cross entropy" alt="Cross entropy" height="48"></a>  

&nbsp;  
To recap:

**i)** The **entropy** *H(P)* is the best possible long term average bits per message (**optimal**) that can be achived under a symbol distribution **P(X)** by using an encoding scheme (possibly unknown) **specifically designed for P(X)**.  

**ii)** The **cross entropy** *H(P,Q)* is the long term average bits per message (**suboptimal**) that results under a symbol distribution **P(X)**, by reusing an encoding scheme (possibly unknown) designed to be **optimal for a scenario with symbol distribution Q(X)**.  

&nbsp;  

Now, KL divergence is the **penalty** we pay, as measured in average number of bits, for using the optimal scheme for *Q(X)*, under the scenario where symbols are actually distributed as *P(X)*. It is straightforward to see this:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/KLpenalty.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/KLpenalty.png" title="KL as a penalty" alt="KL as a penalty" height="133"></a>  
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;   (difference in average number of bits)  

&nbsp;  

&nbsp;  
**2.a)**  
The called *Jensen’s inequality* says that If f is a **convex** function, and X is a random variable, then **E[f(X)] ≥ f (E[X])**. For an interpretation of the theorem, consider the figure below:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/JensenInequality.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/JensenInequality.png" title="Jensen’s inequality" alt="Jensen’s inequality" height="150"></a>

Here, *f* is a convex function shown by the solid line. Also, *X* is a random variable that has a 0.5 chance of taking the value *a*, and a 0.5 chance of taking the value *b* (indicated on the x-axis). Thus, the expected value of *X* is given by the midpoint between *a* and *b*.  

We also see the values *f(a)*, *f(b)* and *f(E[X])* indicated on the y-axis. Moreover, the value *E[f(X)]* is now the midpoint on the y-axis between *f(a)* and *f(b)*. From our example, we see that because *f* is convex, it must be the case that *E[f(X)] ≥ f (EX)*.

&nbsp;  

The [answer to the question 2.a]() uses the Jensen's Inequality theorem to prove the **nonnegativity property of KL divergence** which states that If the cross entropy between *P* and *Q* is zero (and hence DKL(P||Q) = 0) then it necessarily means *P = Q*, that is: 

∀**P,Q &nbsp; DKL(P||Q) ≥ 0** &nbsp; where &nbsp;**DKL(P||Q) = 0** if and only if **P = Q**.  

&nbsp;  
&nbsp;  
**2.b)**  
The KL divergence between two **conditional distributions** *P(X|Y)*, *Q(X|Y)* is defined as follows:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL_conditional.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL_conditional.png" title="DKL conditional" alt="DKL conditional" height="60"></a>

This can be thought of as the expected KL divergence between the corresponding conditional distributions on **x**, that is, between *P(X|Y=y)* and *Q(X|Y=y)*, where the expectation is taken over the random **y**. 

&nbsp;  
As proven  in the [answer to the question 2.b](), the **chain rule for KL divergence** is the following:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL_chain.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/DKL_chain.png" title="DKL chain rule" alt="DKL chain rule" height="27"></a>


&nbsp;  
&nbsp;  
**2.c)**  
In Machine Learning, it is a common task to find a distribution *Q* that is “close” to another distribution *P*. To achieve this, we use DKL(Q||P) to be the loss function to be optimized.  

The **Maximum Likelihood Estimation**, which is a commonly used optimization objective, turns out to be **equivalent minimizing KL divergence between the training data (i.e. the empirical distribution over the data) and the model.**  

Consider a density estimation problem, and suppose we are given a training set *{x(i); i = 1, ..., m}*. Let the empirical distribution ^P be the uniform distribution over the training set; i.e., sampling from the empirical distribution is the same as picking a random example from the training set.)  

Suppose we have some family of distributions *Pθ* parameterized by *θ*. (If you like, think of *Pθ(x)* as an alternative notation for *P(x;θ)*.)

The [answer to the question 2.c]() proved that finding the maximum likelihood estimate for the parameter *θ* is equivalent to finding *Pθ* with minimal KL divergence from *P̂*:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/MLE_KL.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/MLE_KL.png" title="MLE KL" alt="MLE KL" height="60"></a>  


&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 

