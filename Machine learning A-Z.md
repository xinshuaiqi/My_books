# **Machine learning A-Z**

## Regression
#### Simple Linear Regression
Relationships between two continuous (quantitative) variables
y = b0 + b1X1
in R:

    regressor=lm(formula=Salary~ YearsExperience, 
    					data = training_set)
    summary(regressor)
	# the coefficients significance indicates how strong does x associate with the Y.
	
**X** independent variable

**Y** dependent variable 
coefficients (least square coefficients, LSC; estimation based on the observed data)

#### evaluate the accuracy of model
residual SD
: the average amount that the response will **deviate from the true regression line**. 
* the absolute measure of **lack of fit of the model**. 

R<sup>2</sup>
: the proportion of variance explained **(PVE)** by the regression. Range from [0,1]
* close to 0, either the model is wrong, or the inherent error σ<sup>2</sup> is high.






----------


#### Multiple Linear Regression

 **Assumptions of linear regression**
1. **Linearity**
2. Homoscedasticity 方差齐性[不同样本的总体方差是否相同]
3. Multivariate normality
4. Independence of errors
5. Lack of multicollinearity

---
#### **Taking care of the dummy variables**
Such as : NYC and CA => 0, 1
You can not including both dummy variables in the multi linear regression. 

Because of __dummy variable trap__:
 *always omit one dummy variable (n -1)*

-----
#### **How to build a model**
Why choose variables
* garbage IN, garbage OUT
* you have to explain, only keep the right variables

#### **Methods to build a model**

 - All in
 - **Backward elimination** (stepwise regression) **fastest one among the five**
	 1. Select a significant level, such as 0.05
	 2. fit the model with all possible predictors
	 3. remove the variable with the highest P value that >0.05
	 4. fit the model again (after remove step 3 variable)
	 5. Until all P value smaller than 0.05

 - **Forward selection** (stepwise regression)
	  1. Select a significant level, such as 0.05
	  2. all simple linear regression models, select the one with the smallest P value
	  3. two variable, 3, 4, variable linear regression. 
	  4. when > 0.05, the previous model is the best model 

- **Bidirectional elimination** (stepwise regression)
	 1. select 0.05 
	 2. forward selection, add a new variable 
	 3. Backward elimination
	 4. forward, Back, forward, Back. 
	 5. No more variables can enter, no old variables can exit.
 - All possible models 
	 1. select goodness of fit (eg Akaike criterion)
	 2. construct all possible models (2square n -1)  10 columns =>1023 models
	 3. Select the one with the best criterion. 
 
 - score comparison 

---
#### Polynomial Regression
y = b0 + b1x1 + b2X1<sup>2</sup>
This is still linear regression. 
The **linear** refers to the power of coefficients. 


#### Support Vector Regression (SVR)




#### Decision Tree Regression
CART

A decision tree is a decision support tool that uses a tree-like graph or model of decisions and their possible consequences

**qxs:** after subsets the plots, get distinct mean values among the subsets.

*[qxs]: Xinshuai Qi

#### Random Forest Regression
Ensemble Learning. Like bootstrap
* pick K points from the whole dataset
* build a decision tree based on the subset
* build another, another decision tree...
* get N results, take average of these N results.




## Evaluating Regression Models Performance
**R-squared:**

SS<sub>res</sub> = (yi-yi`)<sup>2</sup>

SS<sub>total</sub> = (yi-y<sub>ave</sub>`)<sup>2</sup>

R<sup>2</sup> =1-(SS<sub>res</sub>-SS<sub>total</sub> )

**goodness of fit**
 - How good is your line (compare to the average line)!
 - The closer to 1, the better your model is.

**adjusted R-squared**
 - Problem of R<sup>2</sup>: 
 - add more variable always increase the R<sup>2</sup>.
 - **penalize for add additional variable**. 

# Classification
#### Logistic Regression
Estimate the probability of 1 or 0

#### K-Nearest Neighbors (K-NN)

 1. choose the number of K
 2. using Euclidean distance find the nearest neighbors. 
 3. count the numbers of nearest points of the new point in each group.
 4. **put the new point to the group with the most nearest-neighbors**.

#### Support Vector Machine (SVM)
find the best boundary; find the support vectors
the line in the middle called: maximum margin hyperplane/classifier
**Merits**
 
- apple like orange, orange like apple 


#### Kernel SVM

 - when data is not linear separatable 
 - use 3D; map to a higher dimension
 - can be highly compute-intensive
 - Gaussian RBF Kernel

Types of Kernel Function

- Gaussian RBF Kernel
- Sigmoid Kernel
- Polynomial Kernel

[ML Kernels](http://mlkernels.readthedocs.io/en/latest/)



#### Naive Bayes

**Why "Naive"?**

- Bayes requires the variables are **independent**, but in many cases, that is not true. Thus the assumptions are "naive".


 - **P (Drives | X ) = P (X |drives) * P(drives) / P(x)**
 - poster probability: P (Drives | X ) ; PP 样本X中，事件发生 ("1") 的概率 
 - likelihood: P (X |drives); sample X are people who drive 
 - prior probability: 在总样本中，事件发生 ("1") 的概率
 - P(X) 样本占总体的比例　**可以忽略，当你compare 0 和　１的概率.**


#### Decision Tree Classification
#### Random Forest Classification

## Evaluating Classification Models Performance





# CLUSTERING
#### K-Means Clustering
#### Hierarchical Clustering
very similar or same as K-mean clustering. 

Two types of clustering:
- Agglomerative
	- each point is one cluster, in total N clusters
	- **merge the two closest points** to one cluster. N-1
- Divisive (revise of Agglomerative)
- Until you reach only one cluster.







# ASSOCIATION RULE LEARNING
#### Apriori
#### Eclat



# Reinforcement learning
Also called: online learning 

Solve interacting problems where the data observed up to time t is considered to decide which action to take at time t + 1

一种试图使用包含复杂结构或由多重非线性变换构成的多个处理层对数据进行高层抽象的算法

- use a cascade of multiple layers of nonlinear processing units for feature extraction and transformation. Each successive layer uses the output from the previous layer as input.
- 



# Deep learning 
 



## ANN - Artificial neural network
- not a new thing, but need a LOT of data
- Geoffrey Hinton: the **GODfather** of Deep Learning. [Check his video on YouTube]
- Mimic human brain 
- Artificial Neural Network:
	- **input layer** 
		- columns in the data
	- **Hidden layer**
		- weight the input. like regression, least square...
		- each of the neuron weight the input layers differently
		- a combination of the weighed decision of all these neuron can provide a powerful output layer.
	- Output layer****
	- Hyperbolic Tangent (tanh)
	

##### Neuron
##### Activation function
- Threshold (yes/no)
- **Sigmoid** (commonly used in the **output layer**)  
	- 类似 logistic regression trendline
- **Rectifier** (commonly used in the **hidden layers**)   
	- 折线图: __/
- Hyperbolic Tangent (tanh)
	- 类似sigmoid, logistic (-1,1)

##### How it works.
##### How it learn
- once get the output value, **compare with the actual value**, then feedback on the weight of each neuron. **(cost function)**
	- cost function: what is the gap between prediction and actual value
	- reduce the cost, adjust the weight
- Adjust the weight of each neuron.
- Then feed roles in, then again, again, and again. 

[list of cost funcstions](https://stats.stackexchange.com/questions/154879/a-list-of-cost-functions-used-in-neural-networks-alongside-applications)- Adjust the weight of each neuron.
- Then feed roles in, then again, again, and again. 

### How to decrease the cost function:
#####  Gradient Descent
minimize the cost of function in a very efficient way
碗里的小球，最后停在了碗底
#####  Stochastic Gradient Descent
multiple local minimum, not the best global minimum => use Stochastic gradient descent
`**steps of deep learning:** `

 1. randomly initialise the weights, small number, close to 0
 2. => forward propagation; calculate the errors
 3. <= back propagation, adjust weights at the same time 
 4. repeat 1 and 2 **after each observation** (reinforcement learning ) or **after a batch of observation** (batch learning)
 5. then you got an epoch. Redo more epochs.

### example
many customer leaved the bank in the past 6 months
sample of 10,000 customer, did they left or not
Now, why?# 

### Install libraries
GPU is better for ANN and deep learning. Good at parallel 

- Theano
- TensorFlow
- [Keras](https://keras.io/) (develop deep learning using Theano and TensorFlow within a few lines)

### make ANN
```
classifier =Sequential()
classifier.add(Dense(output_dim = 6, init = "uniform", activation = 'relu', input_dim = 11))
classifier.add(Dense(output_dim = 6, init = "uniform", activation = 'relu')) 
classifier.add(Dense(output_dim = 1, init = 'uniform', activation = 'sigmoid'))
classifier.compile(optimizer = 'adam', loss = 'binary_crossentropy', metrics = ['accuracy'])
classifier.fit(X_train, y_train, batch_size = 10, nb_epoch = 100)
```
- use the **(input column + output column)/2** as your **output_dim** 
- the second hidden layer does not need to know the input_dim
- if you are dealing with **dependent variable (y) with multiple categories**, use **softmax**, instead of sigmoid for the **activation function**

## CNN- Convolutional Neural Networks
- image recognition 
- self-driving car

- **Yann Lecun**, students of Geoffrey Hinton, gradfather of CNN

### How it works
(find features in the image)
1. use a **feature detector** (3x3, 5x5, 7x7) / filter, go through the image, see if it match or not, create a **feature map**. Now the image is smaller. 
2. then create many feature map**s**, together called **convolutional layer**
3. apply **pooling/downsampling** to each of the convolutional layer
4. repeat. make another **convolutional layer** and **pooling layer**
5. **flattening** the matrix, as the input layer of a ANN.
6. add a **new ANN**. input layer => **Full connected layer** => output layer

### ReLU layer ［rectified linear unit (ReLU)］

- **Rectifier** increase **non-linearity** in the image
play with [this link](http://scs.ryerson.ca/~aharley/vis/conv/flat.html)

 

### Forward propagation
### Backpropagation 反向传播


# Dimensionality reduction
Why two independent variables?
* to visualize better
There are two types of Dimensionality Reduction techniques:

1 **Feature Selection**

Backward Elimination, Forward Selection, Bidirectional Elimination, Score Comparison and more. We covered these techniques in Part 2 - Regression.

2 **Feature Extraction**

* Principal Component Analysis (PCA)
* Linear Discriminant Analysis (LDA)
* Kernel PCA
* Quadratic Discriminant Analysis (QDA)


#### **PCA**
#### **Linear Discriminant Analysis (LDA) 线性判别分析** 
[wiki](https://zh.wikipedia.org/wiki/%E7%B7%9A%E6%80%A7%E5%88%A4%E5%88%A5%E5%88%86%E6%9E%90)
a linear combination of features that characterizes or separates two or more classes of objects or events.
Udemy: from the n independent variables, LDA extracts p (<n) new independent variables that separate the most classes of the dependent variable. 
A supervised model. 

#### **Kernel PCA**





# Model Selection
**Evaluate the model performance and improve the performance**


Model Selection techniques including:

# **k-Fold Cross Validation**
split the data into K iteration, like bootstrap, get mean and SD for the accuracy of the model.

Applying k-Fold Cross Validation

    from sklearn.model_selection import cross_val_score
    accuracies = cross_val_score(estimator = classifier, X = X_train, y = y_train, cv = 10)
    accuracies.mean()
    accuracies.std()
**cv** is the K-fold parameter

in R



    library(caret)
    folds = createFolds(training_set$Purchased, k = 10)
    cv = lapply(folds, function(x) {
      training_fold = training_set[-x, ]
      test_fold = training_set[x, ]
      classifier = svm(formula = Purchased ~ .,
                       data = training_fold,
                       type = 'C-classification',
                       kernel = 'radial')
      y_pred = predict(classifier, newdata = test_fold[-3])
      cm = table(test_fold[, 3], y_pred)
      accuracy = (cm[1,1] + cm[2,2]) / (cm[1,1] + cm[2,2] + cm[1,2] + cm[2,1])
      return(accuracy)
    })
    accuracy = mean(as.numeric(cv))

#### **Grid Search**
improve model performance
find the optimal value for parameters
which model is the best? linear or non-linear

Find the parameters that you want to improve in your model fitting, such as "C", "kernel".
Also use K-fold cross validation to estimate the accuracy.

    # Applying Grid Search to find the best model and the best parameters
    from sklearn.model_selection import GridSearchCV
    parameters = [{'C': [1, 10, 100, 1000], 'kernel': ['linear']},
                  {'C': [1, 10, 100, 1000], 'kernel': ['rbf'], 'gamma': [0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9]}]
    grid_search = GridSearchCV(estimator = classifier,
                               param_grid = parameters,
                               scoring = 'accuracy',
                               cv = 10,
                               n_jobs = -1) 
							# n_jobs: in case working on large dataset
    grid_search = grid_search.fit(X_train, y_train)
    best_accuracy = grid_search.best_score_
    best_parameters = grid_search.best_params_



#### **XGBoost**
Eventually we will finish this course by a last bonus section included in this part, dedicated to one of the most powerful Machine Learning model, that has become more and more popular: XGBoost. 

High performance on large dataset

    # Fitting XGBoost to the Training set
    from xgboost import XGBClassifier
    classifier = XGBClassifier()
    classifier.fit(X_train, y_train)

 
# Reinforcement learning
- robot walking
# Natural Language processing
- Spoken and Written word
- translator
- book categories, review, 

#


# **Machine learning resources** 
[**Udemy** Machine Learning A-Z](https://www.udemy.com/machinelearning/learn/v4/overview)
* [superdatascience](https://www.superdatascience.com/machine-learning/)
[*Python* DataScience Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)

### [Top 15 Python Libraries for Data Science in 2017](https://medium.com/activewizards-machine-learning-company/top-15-python-libraries-for-data-science-in-in-2017-ab61b4f9b4a7)
- NumPy:	Data wrangling
- SciPy:	Data wrangling
- Pandas:	Data wrangling
- Matplotlib:	Visualization
- Seaborn:	Visualization
- Bokeh:	Visualization
- Plotly:	Visualization
- SciKit-Learn:	Machine learning
- Keras:	Machine learning
- TensorFlow:	Machine learning


  * [qxs EverNote](http://www.evernote.com/l/ALwaRXZXpbxFYLobSB04bU-A_Sm0mnWbN88/)
	
- Scrapy:	Data scraping
- NLTK:	NLP(natural language processing)
- Gensim:	NLP
- Statsmodels:	Statistics
---
More:
- [PyTorch]() 
- a deep learning framework; Tensor; Deep Neural Networks

### [Top 20 R Machine Learning and Data Science packages](https://www.kdnuggets.com/2015/06/top-20-r-machine-learning-packages.html)
1. **e1071** Functions for latent class analysis, short time Fourier transform, fuzzy clustering, support vector machines, shortest path computation, bagged clustering, naive Bayes classifier etc (142479 downloads) 
2. **rpart** 
	Recursive Partitioning and Regression Trees. (135390)
3. **igraph** A collection of network analysis tools. (122930)
4. **nnet** Feed-forward Neural Networks and Multinomial Log-Linear Models. (108298)
5. **randomFores**t Breiman and Cutler's random forests for classification and regression. (105375)
6. **caret** package (short for Classification And REgression Training) is a set of functions that attempt to streamline the process for creating predictive models. (87151)
7. **kernlab** Kernel-based Machine Learning Lab. (62064)
8. **glmnet** Lasso and elastic-net regularized generalized linear models. (56948)
9. **ROCR** Visualizing the performance of scoring classifiers. (51323)
10. **gbm** Generalized Boosted Regression Models. (44760)
11. **party** A Laboratory for Recursive Partitioning. (43290)
12. **arules** Mining Association Rules and Frequent Itemsets. (39654)
13. **tree** Classification and regression trees. (27882)
14. **klaR** Classification and visualization. (27828)
15. **RWeka** R/Weka interface. (26973)
16. **ipred** Improved Predictors. (22358)
17. **lars** Least Angle Regression, Lasso and Forward Stagewise. (19691)
18. **earth** Multivariate Adaptive Regression Spline Models. (15901)
19. **CORElearn** Classification, regression, feature evaluation and ordinal evaluation. (13856)
20. **mboost** Model-Based Boosting. (13078)

# other Machine learning resources

[漫画解读：轻松看懂机器学习十大常用算法](https://mp.weixin.qq.com/s?__biz=MjM5ODI5Njc2MA==&mid=2655812776&idx=1&sn=ab736c0acb5e43458fd471e350b2fd3d&chksm=bd74317f8a03b86935f1ccdd1c79cf13483e60d8a2a64487e55d0aebb9ecc3916a8e030be050&scene=21#wechat_redirect)

# Machine learning in genomics

[buckler lab machine learning paper](https://www.biorxiv.org/content/early/2017/11/21/222927)




# Advanced Machine Learning

## [morvanzhou machine-learning](https://morvanzhou.github.io/tutorials/machine-learning/)

## [MorvanZhou/tutorials github](https://github.com/MorvanZhou/tutorials)


## [Theano](http://deeplearning.net/software/theano/isatlitall)

# [Machine Learning Crash Course by Google](https://developers.google.com/machine-learning/crash-course/)



# Keras
[Keras 中文文档](https://keras-cn.readthedocs.io/en/latest/)






## TensorFlow
* TensorFlow
  * [TensorFlow 官方文档中文版](tional etor Too T 官方http://m/tensorflow/)
  * [TensorFlow 中文](http://www.tensorfly.cn/tfdoc/get_started/introduction.html)
* [TensorFlow official tutorial](https://www.t# TensorFlow
* TensorFlow
  * [TensorFlow 官方文档中文版](http://docs.pythontab.cothb.com/sofw/

 http://t.com/oN/

   ras
erhttsresearirosoto计算。

## Theano
[Theano教程](http://deeplearning.net/software/theano/install.html#install)

Theano is a Python library that allows you to define, optimize, and evaluate mathematical expressions involving **multi-dimensional arrays** efficiently. 

## PyTorch 
[PyTorch教程](http://www.pytorchtutorial.com/)

## CNTK
Computational Network Toolkit (CNTK) 是微软出品的开源深度学习工具包。

1. 官方入门教程  https://github.com/Microsoft/CNTK/wiki/Tutorial  本文也主要以这里的教程为例

2. 官方论坛 https://github.com/Microsoft/CNTK/issues

3. 官方论文 # Keras
[Keras 中文](https://research.microsoft.com/pubs/226641/CNTKBook-20160217..pdf  这个有150页，我是当作字典来用，遇到问题的时候就在里面搜keras-cn.readthedocs.io/en/latest/)






## TensorFlow和Theano的比较 （以及PyTorch, Caffe）
[从TensorFlow到Theano：横向对比七大深度学习框架](https://www.jiqizhixin.com/articles/2017-02-17-12)
[对比深度学习十大框架：TensorFlow最流行但并不是最好](https://www.jiqizhixin.com/articles/2017-01-02-7)
{23个深度学习库大排名}(https://www.jiqizhixin.com/articles/2017-10-24-6)
