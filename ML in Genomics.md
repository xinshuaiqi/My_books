# ML in genomics

[TOC]





## [Wiki： Machine learning in bioinformatics](https://en.wikipedia.org/wiki/Machine_learning_in_bioinformatics)





## People in ML

##### Yann LeCun

http://yann.lecun.com/

https://en.wikipedia.org/wiki/Yann_LeCun

##### Geoff Hinton

University of Toronto Computer Science

https://en.wikipedia.org/wiki/Geoffrey_Hinton

##### Yoshua Bengio

Canaca; ANN; DL;

##### Yair Weiss





## Useful resources:

A list of deep learning implementations in **biology**: [link](https://github.com/hussius/deeplearning-biology)

A curated list of awesome deep learning applications in the field of **computational biology** [link](https://github.com/gokceneraslan/awesome-deepbio)



[Keras Documentation](https://keras.io/) and [中文文档](https://keras-cn.readthedocs.io/en/latest/)

[TensorFlow 官方文档中文版](http://docs.pythontab.com/tensorflow/)

[莫烦python](https://morvanzhou.github.io/) (python 入门+ Machine Learning)



## Papers:

##### [Evolutionarily informed deep learning methods: Predicting transcript abundance from DNA sequence](https://www.biorxiv.org/content/early/2018/07/19/372367)



##### [Deep Learning for Population Genetic Inference](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004845)

```
 * jointly inferring natural selection and demography
 
 * We find many regions of the genome that have experienced hard sweeps, and fewer under selection on standing variation (soft sweep) or balancing selection.
 
 
 
 
 
 
 
 
```

##### [Deep learning for computational biology](http://msb.embopress.org/content/12/7/878.abstract)

[C Angermueller](https://scholar.google.com/citations?user=OXZC0mQAAAAJ&hl=en&oi=sra), T Pärnamaa, [L Parts](https://scholar.google.com/citations?user=ktEf4ZUAAAAJ&hl=en&oi=sra)… - Molecular systems …, 2016 - msb.embopress.org

```markdown
# the most accurate prediction of gene expression levels is currently made from a broad set of epigenetic features using sparse linear models (Karlic et al, 2010; Cheng et al, 2011) or random forests (Li et al, 2015)

Most of these applications can be described within the canonical machine learning workflow, which involves four steps: 
* data cleaning and pre‐processing, 
* feature extraction, 
* model fitting and 
* evaluation 

A major recent advance in machine learning is automating this critical step by learning a suitable representation of the data with deep artificial neural networks

Briefly, a deep neural network takes the raw data at the lowest (input) layer and transforms them into increasingly abstract feature representations by successively combining outputs from the preceding layer in a data‐driven manner, encapsulating highly complicated functions in the process

depth of the layer X the width of the layer

backward propagation algorithm ultimately enabling efficient training of neural networks using stochastic gradient descent


其他的DNN变形
convolutional neural networks, which are widely used for **modelling images**
recurrent neural networks for **sequential data**
restricted Boltzmann machines and autoencoders for **unsupervised learning**

comprehensive background on all technical details, which can be found in the more specialized literature (Bengio, 2012; Bengio et al, 2013; Deng, 2014; Schmidhuber, 2015; Goodfellow et al, 2016). 
```



##### [*Machine learning** applications in **genetics** and **genomics**](https://www.nature.com/articles/nrg3920)

[MW Libbrecht](https://scholar.google.com/citations?user=O4SMk-sAAAAJ&hl=en&oi=sra), [WS Noble](https://scholar.google.com/citations?user=plt2_DsAAAAJ&hl=en&oi=sra) - Nature Reviews **Genetics**, 2015 - nature.com



##### [Machine Learning in Genomics – Current Efforts and Future Applications](https://www.techemergence.com/machine-learning-in-genomics-applications/)



##### [Deep learning meets genome biology](https://www.oreilly.com/ideas/deep-learning-meets-genome-biology)

An interview with Brendan Frey about realizing new possibilities in genomic medicine.



## Books

[Hands-On Machine Learning with Scikit-Learn and TensorFlow](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1491962291/ref=sr_1_3?ie=UTF8&qid=1537500797&sr=8-3&keywords=machine+learning&dpID=51%252BkYprYK1L&preST=_SX218_BO1,204,203,200_QL40_&dpSrc=srch)



[The Elements of Statistical Learning](https://www.amazon.com/Elements-Statistical-Learning-Prediction-Statistics/dp/0387848576/ref=sr_1_1?ie=UTF8&qid=1537500853&sr=8-1&keywords=the+elements+of+statistical+learning&dpID=41aQrQaPseL&preST=_SY291_BO1,204,203,200_QL40_&dpSrc=srch)



## Tools

[pysster](https://github.com/budach/pysster): 

	 training and interpretation of convolutional neural networks on biological sequence data

	**One_Hot_Encoder**



