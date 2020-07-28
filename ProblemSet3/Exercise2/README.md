

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
*Motivation from coomunication theory:*  

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

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/cross_entropy.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/cross_entropy.png" title="Cross entropy" alt="Cross entropy" height="45"></a>  

&nbsp;  
To recap:

**i)** The **entropy** *H(P)* is the best possible long term average bits per message (optimal) that can be achived under a symbol distribution *P(X)* by using an encoding scheme (possibly unknown) specifically designed for *P(X)*.  

**ii)** The **cross entropy** *H(P,Q)* is the long term average bits per message (suboptimal) that results under a symbol distribution *P(X)*, by reusing an encoding scheme (possibly unknown) designed to be optimal for a scenario with symbol distribution *Q(X)*.  

&nbsp;  
Now, KL divergence is the **penalty** we pay, as measured in average number of bits, for using the optimal scheme for *Q(X)*, under the scenario where symbols are actually distributed as *P(X)*. It is straightforward to see this:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/penalty.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet3/Exercise2/img/penalty.png" title="KL as a penalty" alt="KL as a penalty" height="130"></a> 






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

