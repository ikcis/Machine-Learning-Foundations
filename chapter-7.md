---
description: The VC Dimension
---

# Chapter 7

机器能够学习必须满足两个条件：

1、假设空间H的Size M是有限的，当N足够大的时候，那么对于假设空间中的任意一个假设g，Ein≈Eout（只要break point存在，则M有上界，一定存在Eout​≈Ein​）

2、利用算法A从假设空间H中挑选出一个g，使得Ein≈0，那么Eout≈0

如果一个假设空间H有break point k，那么它的成长函数是有界的，它的上界称为Bound function。根据数学归纳法，Bound function也是有界的，且上界为N^\(k−1\)。从下面的表格可以看出，N^\(k−1\)比B\(N,k\)松弛很多。

![](.gitbook/assets/image.png)

所以我们只要求的上限的上限的上限，即N^\(k−1\)

根据Chapter6的推导，VC Bound可以转换为：

![](.gitbook/assets/image%20%2811%29.png)

这样不等式只与k和N相关，一般情况下样本N足够大，所以我们只考虑k值。有如下结论：

1、若假设空间H有break point k，且N足够大，则根据VC bound理论，算法有良好的泛化能力

2、在假设空间中选择一个g，使Ein​≈0，则其在全集数据中的错误率会较低

![](.gitbook/assets/image%20%283%29.png)

**VC Dimension**

VC Dimension就是某假设集H能够shatter的最多inputs的个数，即最大完全正确的分类能力。（注意，只要存在一种分布的inputs能够正确分类也满足）。

根据之前break point的定义：假设集不能被shatter任何分布类型的inputs的最少个数。则VC Dimension等于break point的个数减一，即k-1。

![](.gitbook/assets/image%20%282%29.png)

用dvc代替k，那么VC bound的问题也就转换为与dvc和N相关了。同时，如果一个假设集H的dvc​确定了，则就能满足机器能够学习的第一个条件Eout≈Ein，与算法、样本数据分布和目标函数都没有关系。

![](.gitbook/assets/image%20%287%29.png)

可证：dvc=d+1

VC Dimension代表了假设空间的分类能力，即反映了H的自由度，产生dichotomy的数量，也就等于features的个数，但也不是绝对的。

![](.gitbook/assets/5b56967869fe3.png)

 

![](.gitbook/assets/screen-shot-2018-12-09-at-19.06.27.png)

所以，为了得到最小的Eout，不能一味地增大dvc以减小Ein，因为Ein太小的时候，模型复杂度会增加，造成Eout变大。也就是说，选择合适的dvc​，选择的features个数要合适。

VC Bound是比较宽松的，而如何收紧它却不是那么容易，这也是机器学习的一大难题。但是，令人欣慰的一点是，VC Bound基本上对所有模型的宽松程度是基本一致的，所以，不同模型之间还是可以横向比较。从而，VC Bound宽松对机器学习的可行性还是没有太大影响。

