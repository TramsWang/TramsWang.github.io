---
title: (待解决)Horn Clause的语义等价性问题
usemathjax: true
tags: [Horn Clause, 语义, 等价性, 待解决]
---

在进行Inductive KB Summarization的时候发现了一个Horn Clause等价性问题。这个问题来源于对重复构造的Horn Rule的重复性剪枝判断。这个问题我目前还没有在已有文献中找到相关研究。

## 1. 定义

> *Def #1 **Horn Clause语义等价***
> 
> 对于两条Horn Clause $$r_1$$和$$r_2$$，如果存在一种变量的重写操作$$\theta$$，使得$$r_1$$和$$r_2\theta$$在形式上完全一致，那么称$$r_1$$和$$r_2$$是语义等价的。

例如：

$$
\begin{equation}
h(X, Y) \gets p(X, Y)\label{eq:first}
\end{equation}
$$

$$
\begin{equation}
h(Y, X) \gets p(Y, X)\label{eq:second}
\end{equation}
$$

存在一个变量重写的操作：$$\theta = \{X \mapsto Y, Y \mapsto X\}$$使得\eqref{eq:second}和\eqref{eq:first}完全一致，则两者语义等价。

> *Def #2 **Horn Clause语义等价性判定问题***
> 
> 对于两条Horn Clause $$r_1$$和$$r_2$$，如果存在变量的重写操作$$\theta$$，使得$$r_1$$和$$r_2\theta$$语义等价，那么返回$$\theta$$，否则返回$$False$$。

## 2. 分析

（待解决）