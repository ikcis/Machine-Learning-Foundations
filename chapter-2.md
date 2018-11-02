---
description: Learning to Answer Yes/No
---

# Chapter 2

**Perceptron Learning Algorithm**

![](.gitbook/assets/screen-shot-2018-11-02-at-13.12.14.png)

$$w$$ 为分割线的法向量，指向 $$y=1$$ 的方向。

找到的错误的 $$x$$ 和法向量 $$w$$ 的夹角大于90度，因此需要 $$w_{t+1}\leftarrow w_{t}+y_{n}x_{n}$$ 来进行修正。

经过若干次的修正， $$w_{t}$$ 与理想中的 $$w_{f}$$ 越来越接近，夹角越来越小。

 **PLA可行性的证明**

**1、**$$w_{t}$$随着迭代次数 $$t$$ 的增加而逐渐向 $$w_{f}$$ 靠拢

![](.gitbook/assets/screen-shot-2018-11-02-at-16.27.54.png)

$$min$$ 项可理解为距离 $$w_{f}$$ 最近的  

