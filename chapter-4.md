---
description: Feasibility of Learning
---

# Chapter 4

**小球容器模型**

样本概率的分布近似于整体分布概率（独立同分布—i.i.d.）

![](.gitbook/assets/screen-shot-2018-11-03-at-10.24.19.png)

Hoeffding’s Inequality**（**霍夫丁不等式**）**

 ****$$\epsilon$$ 为误差

**联系到学习**

![](.gitbook/assets/screen-shot-2018-11-03-at-10.42.46.png)

E为误差

根据sample（in/P）中h与y不相等的概率来推算总体（out）中h与f不相等的概率

![](.gitbook/assets/screen-shot-2018-11-03-at-10.47.51.png)

![](.gitbook/assets/screen-shot-2018-11-03-at-10.52.56.png)

这个过程的作用在于验证我们选择的h好不好

学习到的模型的可行的依据是：

① $$E_{in}(h)$$ 是否足够小 ② $$E_{in}(h)\approx E_{out}(h)$$ 是否成立

h为多个hypothesis中的一个，g才是我们需要的模型



