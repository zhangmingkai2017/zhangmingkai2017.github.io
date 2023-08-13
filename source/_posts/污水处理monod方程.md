---
title: 污水处理monod方程
date: 2023-08-12 11:03:56
categories: 污水处理
tags: 
- monod
- 模拟仿真
mathjax: true
---


# monod 方程 

此方程是20世纪40年代初J. Monod研究了利用单纯基质培养纯菌种后提出的。Monod方程类似于以酶促反应为基础的米-门关系式。式\eqref{eq:monod-mu}即Monod方程。
\begin{equation}
    \mu=\frac{\mu_{\max } S}{K_s+S}
    \label{eq:monod-mu}
\end{equation}

式中，
$\mu$——微生物比增长速度，$\rm d^{-1} $，即单位微生物量的增长速度$\displaystyle \frac{d X / d t}{X}$，$X$为微生物浓度；
$\mu_{\max}$ ——在饱和浓度中微生物的最大比增长速度，$\rm d^{-1} $ ；
$K_S$ ——饱和常数，其值为 $\displaystyle\mu=\frac{\mu_{max}}{2}$ 时的基质浓度， $\rm mg/L $；
$S$ ——基质浓度，$\rm mg/L $。


由
$$
\begin{gathered}
    \frac{d X / d t}{X}=-Y_0 \frac{d S / d t}{X} \\
    \mu=\frac{d X / d t}{X} \\
    -\frac{d S / d t}{X}=U_s=v
\end{gathered}
$$

得
$$
\mu=Y_0 v
$$

或
$$
\mu_{\max }=Y_0 v_{\max }
$$

式中，
$v$——基质比去除速度，$\rm d^{-1}$；
$v_{max}$——基质的最大比去除速度，$\rm d^{-1}$;
$Y_0$——表观产率系数，mg微生物/mg基质。

代入式\eqref{eq:monod-mu}得，
\begin{equation}
    v=\frac{v_{\max } S}{K_s+S}
    \label{eq:monod-v}
\end{equation}

式中，
$S$——基质浓度，mg/L；
$K_s$——饱和常数，mg/L。

在废水生物处理中，基质的去除是主要的任务，而微生物的增长只是基质去除的结果，所以式\eqref{eq:monod-v}更有意义。