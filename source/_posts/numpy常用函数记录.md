---
title: numpy常用函数记录
date: 2017-12-19 01:18:23
tags: [numpy, Python]
categories: numpy
mathjax: true
---
## random模块
np.random.random

> Return random floats in the half-open interval [0.0, 1.0).产生随机矩阵，如random.random([2,3])产生一个2x3维的随机数
<!-- more -->
## np.flatzero()
> 该函数输入一个矩阵，返回扁平化后矩阵中非零元素的位置（index）
```
1 >>> x = np.arange(-2, 3)
2 >>> x
3 array([-2, -1,  0,  1,  2])
4 >>> np.flatnonzero(x)
5 array([0, 1, 3, 4])
```
这是在作业中给出的用法：不走寻常路，用来返回某个特定元素的位置

对向量元素的判断d==3返回了一个和向量等长的由0/1组成的矩阵，然后调用函数，返回的位置，就是对应要找的元素的位置。

## np.random.choice()
可以从一个int数字或1维array里随机选取内容，并将选取结果放入n维array中返回。
>numpy.random.choice(a, size=None, replace=True, p=None)  
replace 表示是否重复选取
```
a : 1-D array-like or int
    If an ndarray, a random sample is generated from its elements. 
    If an int, the random sample is generated as if a was np.arange(n)

size : int or tuple of ints, optional 

replace : boolean, optional
    Whether the sample is with or without replacement

p : 1-D array-like, optional
    The probabilities associated with each entry in a. If not given the sample assumes a uniform distribution over all entries in a.
```
```
>>> np.random.choice(5, 3)
array([0, 3, 4])

>>> np.random.choice(5, 3, p=[0.1, 0, 0.3, 0.6, 0])
array([3, 3, 0])

>>> np.random.choice(5, 3, replace=False)
array([3,1,0])

>>> np.random.choice(5, 3, replace=False, p=[0.1, 0, 0.3, 0.6, 0])
array([2, 3, 0])

>>> aa_milne_arr = ['pooh', 'rabbit', 'piglet', 'Christopher']

>>> np.random.choice(aa_milne_arr, 5, p=[0.5, 0.1, 0.1, 0.3])
array(['pooh', 'pooh', 'pooh', 'Christopher', 'piglet'],
```
## np.maxmium()
```
>> np.maximum([-2, -1, 0, 1, 2], 0)
array([0, 0, 0, 1, 2])

# 当然 np.maximum 接受的两个参数，也可以大小一致
# 或者更为准确地说，第二个参数只是一个单独的值时，其实是用到了维度的 broadcast 机制；
```