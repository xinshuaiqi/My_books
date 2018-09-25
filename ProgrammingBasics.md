


## **Python**

**Python packages**
* basic
  * [Python3 迭代器与生成器](http://www.runoob.com/python3/python3-iterator-generator.html)
  * [Class](https://morvanzhou.github.io/tutorials/python-basic/basic/09-1-class/)
  * [personal module](https://morvanzhou.github.io/tutorials/python-basic/basic/12-2-personal-module/)
  * [multiprocessing and multithreads](https://morvanzhou.github.io/tutorials/python-basic/multiprocessing/2-add/)
```
import multiprocessing as mp # 这个比较快
import threading as td

def job(a,d):
    print('aaaaa')

t1 = td.Thread(target=job,args=(1,2))
p1 = mp.Process(target=job,args=(1,2))

t1.start()
p1.start()

t1.join()
p1.join()

  ```
  * [tkinter: GUI for python](https://morvanzhou.github.io/tutorials/python-basic/tkinter/)
  * [R-shiny](https://shiny.rstudio.com/) **build interactive web apps straight from R**
* scipy
* numpy
* pandas 参考[莫烦python pandas][1]

[1]: https://morvanzhou.github.io/tutorials/data-manipulation/np-pd/

* scipy
* numpy
* pandas
* matplotlib 
	* [official_website](https://matplotlib.org/)
		* [tutorials](https://matplotlib.org/tutorials/index.html#introductory)
		* [gallery](https://matplotlib.org/gallery/index.html)
* seaborn

* [莫烦python](https://morvanzhou.github.io/) (python 入门+ Machine Learning)
* [Python3 Tutorial RUNOOB](http://www.runoob.com/python3/python3-tutorial.html)
* [Python 入门指南](http://www.pythondoc.com/pythontutorial3/index.html)
* [廖雪峰的Python教程](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000)
* [用Python做科学计算](https://wizardforcel.gitbooks.io/hyry-studio-scipy/content/)
* [Python regex](https://docs.python.org/3.6/library/re.html)
* [Python 进阶（中级）](http://docs.pythontab.com/interpy/)
* [Path of data science using python](http://www.evernote.com/l/ALzgYtH566lHKZUu1l5P_uhRwn-uImxGoQg/)

* [rpy2](https://rpy2.bitbucket.io) 
