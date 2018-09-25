# **Mathematical  Statistics**


## Rresources
* [**Zhang Zhiwu CROPS 545**](http://www.zzlab.net/)
* [HarvardX Biomedical Data Science Open Online Training](http://rafalab.github.io/pages/harvardx.html)
  * [PH525x series - Biomedical Data Science](http://genomicsclass.github.io/book/)
  * [Bioconductor for Genomic Data Science](http://kasperdanielhansen.github.io/genbioconductor/) [fiveMinuteStats](http://stephens999.github.io/fiveMinuteStats/index.html)
* [kaggle](https://www.kaggle.com/datasets)
* 生物统计学课件（2014） - 李欣海 （见Mega folder）

* [**Basic Statistics in R**](https://www.statmethods.net/stats/index.html)
* [PennState STAT 897D](https://onlinecourses.science.psu.edu/stat857/)
* [An Introduction to Statistical Learning](http://www-bcf.usc.edu/~gareth/ISL/)

*  [**Statistics in Action with R**](http://sia.webpopix.org/index.html) with _**example code**_nice
* [**R Tutorial： An R Introduction to Statistics**](http://www.r-tutor.com/)
 ```
Show how statistics may be efficiently used in practice
;
Topics covered in the current version of the course are:
	- hypothesis testing (single and multiple comparisons) 
	- regression
	- mixed effects models (linear  and nonlinear models) 
	- mixture models 
	- detection of change points 
	- image restoration
``` 
  





  
	* 


## lm

1. 模型显著度: F-stat P-value 
3. whether the intercept and slope are sign? *** t -test
4. PVE explained by the model, 决定系数 R^2 and adjusted R^2 （考虑了参数和观测值的数量）越接近1越好
5. residual 区间越小越好

```
dffits(m0) # remove this data and its impact on Y prediction  杠杆点 impact on R^2
 
dfbetas(m0) # remove the data impact on the slope. 影响点
```

#### 多重共线性问题
一般多元线性回归假设变量之间独立。但事实上他们往往是相关的。
使用VIF function (within faraway package) to remove all variables with value larger than 10
然后对剩下来的变量进行lm

####



 


