---
description: Noise and Error
---

# Chapter 8

 在有Noise的情况下，即数据集按照P\(y∣x\)概率分布，那么VC Dimension仍然成立，机器学习算法推导仍然有效。

 因为Noise的存在，比如在x点，有0.7的概率y=1，有0.3的概率y=0，即y是按照P\(y∣x\)分布的。数学上可以证明如果数据集按照P\(y∣x\)概率分布且是iid的，那么以前证明机器可以学习的方法依然奏效，VC Dimension有限即可推断Ein和Eout是近似的。

 机器学习cost function常用的Error有0/1 error和squared error两类。 0/1 error通常用在分类（classification）问题上，而squared error通常用在回归（regression）问题上。

 0/1 error中的mini-target是取P\(y\|x\)最大的那个类，而squared error中的mini-target是取所有类的加权平方和。

![](https://i.loli.net/2018/07/24/5b569a471a325.png)



 Error有两种：false accept和false reject。false accept意思是误把负类当成正类，false reject是误把正类当成负类。 根据不同的机器学习问题，false accept和false reject应该有不同的权重，这根实际情况是符合的，比如是超市优惠，那么false reject应该设的大一些；如果是安保系统，那么false accept应该设的大一些。

 实际问题中，对false accept和false reject应该选择不同的权重。

