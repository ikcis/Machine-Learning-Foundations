---
description: Linear Regression
---

# Chapter 9

 令用户特征集为d维的X，加上常数项，维度为d+1，与权重w的线性组合即为Hypothesis,记为h\(x\)。线性回归的预测函数取值在整个实数空间，这跟线性分类不同。

![](https://i.loli.net/2018/07/24/5b56b82d5ee77.png)

在一维或者多维空间里，线性回归的目标是找到一条直线（对应一维）、一个平面（对应二维）或者更高维的超平面，使样本集中的点更接近它，也就是残留误差Residuals最小化。

一般最常用的错误测量方式是基于最小二乘法，其目标是计算误差的最小平方和对应的权重w，即上节课介绍的squared error：

![](https://i.loli.net/2018/07/24/5b56b842387b7.png)



![](https://i.loli.net/2018/07/24/5b56b84e8e962.png)

样本数据误差Ein​是权重w的函数，因为X和y都是已知的。我们的目标就是找出合适的w，使Ein​能够最小。

首先，运用矩阵转换的思想，将Ein​计算转换为矩阵的形式。

![](https://i.loli.net/2018/07/24/5b56b8658ec0b.png)

 然后，对于此类线性回归问题，Ein​\(w\)一般是个凸函数。凸函数的话，我们只要找到一阶导数等于零的位置，就找到了最优解。那么，求偏导，偏导为零的w​，即为最优化的权重值分布。



![](https://i.loli.net/2018/07/24/5b56b86fe52fb.png)

 根据梯度的思想，对Ew​进行矩阵话求偏导处理：

![](https://i.loli.net/2018/07/24/5b56b877cf910.png)

 令偏导为零，最终可以计算出权重向量w为：



![](https://i.loli.net/2018/07/24/5b56b88093bc5.png)

最终，我们推导得到了权重向量w，这是上文提到的closed-form解。

但是，我们注意到，伪逆矩阵中有逆矩阵的计算，逆矩阵是否一定存在？一般情况下，只要满足样本数量N远大于样本特征维度d+1，就能保证矩阵的逆是存在的，称之为非奇异矩阵。但是如果是奇异矩阵，不可逆怎么办呢？其实，大部分的计算逆矩阵的软件程序，都可以处理这个问题，也会计算出一个逆矩阵。所以，一般伪逆矩阵是可解的。

总结

![](.gitbook/assets/image%20%289%29.png)

![](.gitbook/assets/image%20%2814%29.png)

在Coursera的课程中即为Normal Equation

 The "Normal Equation" is a method of finding the optimum theta **without iteration.**

 There is **no need** to do feature scaling with the normal equation.

![](.gitbook/assets/image%20%285%29.png)

