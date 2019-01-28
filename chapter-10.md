---
description: Logistic Regression
---

# Chapter 10

 软性二分类问题（’soft’ binary classification）。这个值越接近1，表示正类的可能性越大；越接近0，表示负类的可能性越大。

![](https://i.loli.net/2018/07/24/5b56f0175db69.png)

 对于软性二分类问题，理想的数据是分布在\[0,1\]之间的具体值，但是实际中的数据只可能是0或者1，我们可以把实际中的数据看成是理想数据加上了噪声的影响。

![](https://i.loli.net/2018/07/24/5b56f17a4d52b.png)

![](.gitbook/assets/image%20%2818%29.png)

![](.gitbook/assets/image%20%283%29.png)

![](.gitbook/assets/image%20%287%29.png)

![](https://i.loli.net/2018/07/24/5b56f30945a5e.png)

![](https://i.loli.net/2018/07/24/5b56f31d078ef.png)

 如果将w代入的话：

![](https://i.loli.net/2018/07/24/5b56f32ab9269.png)

 为了把连乘问题简化计算，我们可以引入ln操作，让连乘转化为连加：

![](https://i.loli.net/2018/07/24/5b56f3361f39d.png)

接着，我们将maximize问题转化为minimize问题，添加一个负号就行，并引入平均数操作

![](https://i.loli.net/2018/07/24/5b56f33fd0093.png)

 将logistic function的表达式带入，那么minimize问题就会转化为如下形式：

![](https://i.loli.net/2018/07/24/5b56f34f16d27.png)

 至此，我们得到了logistic regression的err function，称之为cross-entropy error交叉熵误差：

![](https://i.loli.net/2018/07/24/5b56f36578da9.png)

![](.gitbook/assets/image%20%2815%29.png)

![](.gitbook/assets/image%20%2817%29.png)

