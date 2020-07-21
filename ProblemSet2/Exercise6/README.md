
<a href="https://i.dlpng.com/static/png/498606_preview.png"><img src="https://i.dlpng.com/static/png/498606_preview.png" title="Stanford" alt="Stanford" height="50"></a>

## Spam classification
  
**Exercise 6**  
In this problem, we will use the **Naive Bayes** algorithm and an **SVM** to build a spam classifier. In recent years, spam on electronic media has been a growing concern. Here, we’ll build a classifier to distinguish between real messages, and spam messages. For this, we will be building a classifier to detect SMS spam messages. The goal of this assignment is to build a classifier from scratch that can tell the difference the spam and
non-spam messages using the text of the SMS message.  

&nbsp;  
The [code for this problem]() uses the **get_words**, **create_dictionary**, and **transform_text** functions for processing the the spam messages into numpy arrays that can be fed into machine learning models. It also implements a **Naive Bayes** classifier for spam classification with multinomial event model and Laplace smoothing.  

We verify that some tokens are particularly indicative of an SMS being in a SPAM class. The top 5 most indicative tokens are:  
*claim*, *won*, *prize*, *tone* and *urgent!*.

Then, using **SVM** as an alternative machine learning algorithm, we find the best SVM radius wich maximizes accuracy on the validation dataset; The radius that works best is *0.1* achieving an accuracy of 96%. 



&nbsp;  
---

#### Aline Gabriel de Almeida  
<a href="https://www.linkedin.com/in/alinegalmeida/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/201_Linkedin-512.png" title="Linkedin: alinegalmeida" alt="https://www.linkedin.com/in/alinegalmeida/" height="20"></a>
&nbsp; <a href="https://www.kaggle.com/almeidaalin3"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/189_Kaggle-512.png" title="Kaggle: almeidaalin3" alt="https://www.kaggle.com/almeidaalin3" height="20"></a>
&nbsp; <a href="mailto:aline.gabriel.almeida@gmail.com"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/147_Gmail-512.png" title="aline.gabriel.almeida@gmail.com" alt="aline.gabriel.almeida@gmail.com" height="20"></a>
&nbsp; <a href="https://github.com/AlmeidaAlin3/"><img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/142_Github-512.png" title="Github: AlmeidaAlin3" alt="https://github.com/AlmeidaAlin3/" height="20"></a> 

