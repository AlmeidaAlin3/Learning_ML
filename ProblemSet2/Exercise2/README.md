
<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Model Calibration
  
**Exercise 2**  
In this exercise we will try to better understand the output *h(x)* of the hypothesis function of a logistic regression model, in particular why we might treat the output as a probability (besides the fact that the sigmoid function ensures *h(x)* always lies in the interval (0, 1)).    

When the probabilities outputted by a model match empirical observation, the model is said to be **well-calibrated** (or reliable). For example, if we consider a set of examples *x^(i)* for which *h(x^(i)) ≈ 0.7*, around 70% of those examples should have positive labels. In a well-calibrated model, this property will hold true at every probability value.  

Logistic regression tends to output well-calibrated probabilities (this is often not true with other classifiers such as Naive Bayes, or SVMs). We will dig a little deeper in order to understand why this is the case, and find that the structure of the loss function explains this property.


&nbsp;  
**2.a)**  
In order for the model to be considered well-calibrated, given any range of probabilities *(a, b)* such that *0 ≤ a < b ≤ 1*, and training examples
*x^(i)* where the model outputs *h(x^(i))* fall in the range *(a, b)*, the fraction of positives in that set of examples should be equal to the average of the model outputs for those examples.  

The gradient of the log likelihood is given by:  

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/log_likelihood.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/log_likelihood.png" title="log-likelihood" alt="log-likelihood" height="25"></a> 

For the best θ, we will have:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/best_theta.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/best_theta.png" title="solution" alt="solution" height="30"></a>

If we only consider one feature of X, (first row of X.T) we will find:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/proof.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/proof.png" title="proof" alt="proof" height="60"></a>

This shows that the the model is indeed well-calibrated.

&nbsp;  
**2.b)**  
If we have a binary classification model that we know is perfectly calibrated, it **does not** necessarily imply that the model achieves perfect accuracy. And the converse is also **not true**.  

For example, suppose a dataset that contains the result got from flipping a biased coin multiple times and it has 50% of positive data (tails).  
Then a model which always outputs 0.5 will be perfectly calibrated, but not necessarily acurate. On the other hand, a model that outputs 0.75 for positive examples (tails) and 0.25 for negative examples (heads) could have perfect accuracy, but would be not perfectly calibrated.  

&nbsp;  
**2.c)**  
When including a L2 regularization in the logistic regression, the equation becomes:

<a href="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/regularization.png"><img src="https://github.com/AlmeidaAlin3/MachineLearning/blob/master/ProblemSet2/Exercise2/img/regularization.png" title="Regularization term added" alt="Regularization term added" height="65"></a>

The regularization given by *λ||θ||* has no effect on model calibration.  

&nbsp;  
*Remark: When the training and test set are from the same distribution and when the model has not overfit or underfit, logistic regression tends to be well-calibrated on unseen test data as well. This makes logistic regression a very popular model in practice, especially when we are interested in the level of uncertainty in the model output.*



&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 
