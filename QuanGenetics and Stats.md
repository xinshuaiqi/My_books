


# Quantitative Genetics, GWAS, and i

# General resources:
* [Tucson Plant Breeding Institute](http://www.plantbreedinginstitute.bio5.org/)
* [Textbook Animal Breeding and Genetics](https://wiki.groenkennisnet.nl/display/TAB/Textbook+Animal+Breeding+and+Genetics) a good on-line reference book 
* [Plant Breeding and Genomics Webnar](http://articles.extension.org/plant_breeding_genomics)
- [Online Resources for Plant Breeding Education(httpwww.plantbreeding.org/content/online-resources-for-plant-breeding-education)

- [Plant Breeding and Genomics YouTube Channel](https://www.youtube.com/channel/UCLdgn7_1J6n1Hk6bqNL_Xag)
	- [Estimating Heritability and BLUPs](https://www.youtube.com/watch?v=YIVY-9Jk-5c&list=PL25028B4AFDE62416) 




# Models (in order to ranking the plants)
refer:[Chapter 8](https://wiki.groenkennisnet.nl/display/TAB/Chapter+8%3A+Ranking+the+animals)

![Breeding program](https://wiki.groenkennisnet.nl/download/attachments/1901577/Breeding%20program.jpg?version=1&modificationDate=1419419649850&api=v2)




# How to rank the plants:
* Mass selection
	* not work when heritability is low
	* ```EBVmass selection = h2 * (P-Pmean) ```
* Animal selection: 
	* use relatives to estimate the breeding value for traits hard/can't measure directly. 
	* when pedigree is accurate
	* need large number of relatives
	```
	EBVoffspring =  bsingle parent-offspring * (Psingle parent - Pmean)

            = ½ h2 * (Psingle parent - Pmean)
            
*  Genomic selection
	* reference population: both pheno and geno data
	* predict population: large, with no pheno, but has geno.

In practice, use the best regression coefficient to predict the **estimated breeding value (EBV)**. Although **True breeding value(TBV)** is always unknown. 

 

# Fix effects and Random effects
 * **fixed effects**: 
	 * only consider study variance
	 * assume individual–specific effects are correlated with the independent variables
	 * 得到回归线截距会不同，但回归线平行
	 * **group mean is fixed** 
 * **random effects**: 
	 * consider both study variance and difference between study variance (env or other unconsidered variance)
	 * assume individual–specific effects are not correlated with the independent variables
	 * 同时影响模型截距与斜率，是指它还与其它变量相乘，那么分别得到的回归线截距和斜率都不同
	 * 对于随机效应我们只估计其方差，不估计其回归系数。
	 * **group mean is unknown**





## **Fixed effects model**
* a regression model in which **the group means are fixed** (non-random) as opposed to a random effects model in which the group means are a random sample from a population.

```Outcome = Intercept + Fixed Effects + Error(Residuals)```

## **Random effects model**



### how to decide fixed and random factors
- 随机效应（相关性比较强，而且不是主要研究对象,同时自身存在一定随机性，比如搜索点击数据，自身就不受控制，存在很多随机因素）；
- 固定效应（主要研究的解释变量）






## **Mixed model**

-  Mixed model [on wiki](https://en.wikipedia.org/wiki/Mixed_model)
 * A mixed model is a statistical model containing both **fixed effects** and **random effects**.
 * Mixed effects models are often preferred over more traditional approaches such as repeated measures ANOVA
 * it has advantage in dealing with missing values
 * History
	 * Ronald Fisher introduced random effects models to study the correlations of trait values between relatives. 
	 * In the 1950s, Charles Roy Henderson provided **best linear unbiased estimates (BLUE)** of fixed effects and **best linear unbiased predictions (BLUP)** of random effects.

```Outcome = Intercept + Fixed Eeffects +Random Effects+  Error(Residuals)```?


---
# [**Parameter test *vs* non-Parameter test**](http://blog.sciencenet.cn/blog-508298-855369.html)
[Baidu非参数检验](https://baike.baidu.com/item/%E9%9D%9E%E5%8F%82%E6%95%B0%E6%A3%80%E9%AA%8C)

  * 参数检验
	 + 针对参数做的假设检验
	 * 如**u检验，t检验，F检验，Z检验**等都是参数检验
	 * 只能用于等距数据和比例数据
		 * 非参数检验
	 * 不依赖参数进行的假设检验
	 * 当无法对总体分布形态作简单假定时
	 * 针对总体分布情况做的假设
	 * 总体分布不易确定（也就是不知道是不是正态分布）
	 * 分布呈非正态而无适当的数据转换方法
	 * 主要用于记数数据
	 * 包括**卡方检验、二项分布检验、K-S检验以及变量值随机性**检验等方法

### Other resources:
- [Introduction to mixed models with R](https://idaejin.github.io/bcam-courses/neiker-2016/material/mixed-models/)
 * AS
- [A practice guide to mixed model in R](https://ase.tufts.edu/gsc/gradresources/guidetomixedmodelsinr/mixed%20model%20guide.html)

[Choosing Between a Nonparametric Test and a Parametric Test](http://blog.minitab.com/blog/adventures-in-statistics-2/choosing-between-a-nonparametric-test-and-a-parametric-test)

|||
|   Parametric tests (means)	|   Nonparametric tests (medians)	|   
|---	|---	|
|   1-sample t test	|   1-sample Sign, 1-sample Wilcoxon	|   
|   2-sample t test	|   Mann-Whitney test|
|   One-Way ANOVA	|   	Kruskal-Wallis, Mood’s median test|  
|   Factorial DOE with one factor and one blocking variable	|   Friedman test	|  
---


# [General linear mixed model]()

### [**GLMM**  generalized linear mixed model](https://en.wikipedia.org/wiki/Generalized_linear_mixed_model)
an extension to the generalized linear model (GLM) in which the linear predictor contains __random effects__ in addition to the usual __fixed effects__

- 自变量可以是离散的，也可以是连续的。0/1
- 取消了对残差(因变量)服从正态分布的要求。

### [non-linear mixed model]()

### multivariate statistics

### non=parametric analysis 

### Bayesian statistics 




# [**BLUP**: Best linear unbiased prediction](https://en.wikipedia.org/wiki/Best_linear_unbiased_prediction)
* used in linear mixed models for the estimation of random effects
* similar to BLUEs (best linear unbiased estimates)
* This method optimising the estimated regression coefficient, and also corrects thephynotypes for systematic effects.  
* to estimate EBV (Estimated breeding value). 
* if consider pedigree in the model: PBLUP
* if consider genomic selection in the model: GBLUP
* is a linear mixed model


```
In formula it would look like this:

Y = Xb + Za + e

The Y is the phenotypic information, the Xb corrects the phenotypic superiorities for the systematic effects, and the Za links the phenotypic superiorities to the additive genetic relationships to estimate the EBV. The e indicates the error variance. In a way BLUP does follow the simple model P = E + G, but also provides estimates of G and E.

For example, if animals on one farm are fed much better than on another farm, then ranking animals based on their weight would benefit the animals from the farm with the better nutrition. However, genetically the animals on both farms may be similar. Without taking this systematic influence of farm of origin into account it is likely that the top ranking animals would mainly originate from the farm with the better feed. To be able to compare the performance of the animals more on their genetic potential it is important to take this farm effect into account, and this is what BLUP does (if you provide the information about on which farm each animal was housed). The principle of BLUP is to determine the average weight of the animals on each farm and subtract the difference from the animals on the farm with the highest weight. So if animals on farm 1 weigh 100 kg, and on farm 2 they weigh 120 kg, then you ‘punish’ the animals of farm 2 by subtracting 20 kg from their weight.

Notes:
With BLUP it is possible to estimate breeding values using information on relatives and correcting phenotypes for systematic influences.

Critical point is that sufficient genetic links between environments are required to estimate systematic effects of those environments (e.g. farms).
```


* original paper in 1991 by G K Robinson :
https://projecteuclid.org/euclid.ss/1177011926
* (Chapter 8.10: Best Linear Unbiased Prediction: )[https://wiki.groenkennisnet.nl/display/TAB/Chapter+8.10%3A+Best+Linear+Unbiased+Prediction]
* [YouTube tutorial BLUP and Heritability using R package lme4](https://www.youtube.com/watch?v=YIVY-9Jk-5c&list=PL25028B4AFDE62416)
		* [download example data](http://articles.extension.org/pages/61006/estimating-heritability-and-blups-for-traits-using-tomato-phenotypic-data)
	
	---

#  ***lme4 package*** 
Fit linear and generalized linear mixed-effects models

	https://cran.r-project.org/web/packages/lme4/index.html

* Getting Started with Mixed Effect Models in Rhttps://www.jaredknowles.com/journal/2013/11/25/getting-started-with-mixed-effect-models-in-r)

* [lmer：Fit mixed-Effects Models 中文](http://www.voidcn.com/article/p-dxqhvyei-dp.html)
* [lme4 example](http://xccds1977.blogspot.com/2011/12/blog-post_08.html)
	* 	为了判断哪一个模型更为合适，可以使用anova函数，从结果中观察到P值很小
	* 得到的模型结果还可以用各种泛型函数如summary、predict、resid进行进一步处理
	* 当响应变量不符合正态分布假设时，还可以用广义多层回归进行(glmer)建模

### non-linear mixed models
(refer [Nonlinear Mixed Effects Models: An Overview and Update](www4.stat.ncsu.edu/~davidian/nlmmtalk.pdf))

- repeat measurement (over time) for small sample size



  packages
 [Linear mixed models in R](https://www.r-bloggers.com/linear-mixed-models-in-r/)
 * [nlme](https://cran.r-project.org/web/packages/nlme/index.html)
 *it and compare Gaussian linear and nonlinear mixed-effects models.
	 * 
 * [lme4](https://cran.r-project.org/web/packages/lme4/index.html)




#### nlme vs lme4
```
Merit of nlme
1. nlme has some nice features like groupedData() and lmList() that are lacking in lme4
2. in nlme, it is possible to specify the variance-covariance matrix for the random effects (e.g. an AR(1)); it is not possible in lme4
```
```
Merit of lme4
3. lme4 extends nlme with other link functions: in nlme, you cannot fit outcomes whose distribution is not gaussian, lme4 can be used to fit mixed-effects logistic regression, for example.
4. lme4 can easily handle very huge number of random effects
5. the flexibility of lme4 is sufficient for most applications
6. 
```

 * [ASreml-R](https://www.vsni.co.uk/software/asreml/)
	 * designed for fitting linear mixed models


[More packages: **GLMM for ecologists and evolutionary biologists**](http://glmm.wikidot.com/pkg-comparison#LMMs)

**Review** [Generalized linear mixed models: a practical guide for ecology and evolution](http://www.sciencedirect.com.ezproxy2.library.arizona.edu/science/article/pii/S0169534709000196?via%3Dihub) Trends in Eco & Evo
Reml-R

-----
**Apply to PAH**:

Identifying genetically driven clinical phenotypes using linear mixed models
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4848547/#!po=29.1045

### gBLUP

	* line effect


http://nce.ads.uga.edu/wiki/lib/exe/fetch.php?media=uga_4_ssgblup.pdf
http://articles.extension.org/pages/68019/genomic-relationships-and-gblup
http://pbgworks.org/sites/pbgworks.org/files/ISIK_GBLUPwebinar2013.1.pdf

### rrBLUP

Marker effect
* **E:\GoogleDrive\My_Scripts\R学习\rrBLUP**
 
## GWAS and QTL mapping
  * PLink (tutorial)[http://zzz.bwh.harvard.edu/plink/tutorial.shtml#t6]
  * R/qtl# 
 
[a review of mixed model by Ed Buckler](https://academic.oup.com/bib/article/10/6/664/260106)


[EMMAX](https://genome.sph.umich.edu/wiki/EMMAX)

[GAPIT](http://www.maizegenetics.net/gapit)
Genome Association and Prediction Integrated Tool – is an R package that performs Genome Wide Association Study (GWAS) and genome prediction (or selection). This program uses state-of-the-art methods developed for statistical genetics, such as the unified mixed model, EMMA, the compressed mixed linear model, and P3D/EMMAx.**Machine learning** 
[**Udemy** Machine Learning A-Z](https://www.udemy.com/machinelearning/learn/v4/overview)
* [superdatascience](https://www.superdatascience.com/machine-learning/)
[*Python* DataScience Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)


## Genomic Selection



### genomic prediction and genomic selection
https://www.evernote.com/shard/s188/nl/23839285/cbd42518-808a-44fc-8f4b-323142f13521

