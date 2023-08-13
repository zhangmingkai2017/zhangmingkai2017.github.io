---
title: 污水处理Lawrence-McCarty方程
date: 2023-08-13 10:40:14
categories: 污水处理
tags:
- monod
- 模拟仿真
katex: true
---

# Lawrence-McCarty 模型

## 公式
Lawrence-McCarty模型的两个基本方程式如下。

$$
\frac{1}{\theta_c} = Y U_s - K_d
$$


$$
U_s = v = \frac{v_{max} S_e}{K_s + S_e} 
$$

并由此可导出下面两个方程。后者的突出之点是强调了细胞平均停留时间$\theta_c$这一参数的重要性及其在设计、运行中的意义。

$$
S_e = \frac{K_s (1 + K_d \theta_c)}{\theta_c (Y v_{max} - K_d) - 1}
$$

$$
X = \frac{\theta_c}{\theta} \cdot \dfrac{Y (S_0 - S_e)}{1 + K_d \theta_c}
$$


式中：
$S_0$, $S_e$——反应器进水、出水的基质浓度，mg/L，如存在不可生物降解物质，则应考虑$S_n$的问题；
$\theta_c$ —— 细胞平均停留时间(MCRT)，即细胞平均停留在处理系统内的时间，d；
$\theta$ ——水力停留时间，d，有时也用t表示； 
$X$ —— 微生物浓度，mg/L，在活性污泥法中可以MLVSS表示； 
$U_s$ —— 以基质去除量为基础的污泥负荷，此时等于基质比去除速度$v$，$\rm d^{-1}$； 
$v_{max}$ —— 基质最大比去除速度，$\rm d^{-1}$；
$K_s$ —— 饱和常数，mg/L；
$K_d$ ——衰减常数，$\rm d^{-1}$；
$Y$ —— 理论产率系数，mg微生物/mg基质。


## 推导

推导： Lawrence-McCarty模型是以微生物生理学为基础，根据微生物增长与基质利用的关系推导出来的。

$$
\frac{d X}{d t}=Y \frac{d F}{d t}-K_d X
$$



式中：
$\displaystyle\frac{d F}{d t}$——基质利用速度，$\rm mg/(L \cdot d)$；
$Y$——理论产率系数，mg微生物/mg基质；
$\displaystyle\frac{d X}{d t}$ ——微生物净增长速度，$\rm mg/(L \cdot d)$；
$K_d$——衰减常数，即微生物自身氧化率，$\rm d^{-1}$；
$X$——微生物的浓度，mg/L。



上式中各项均除以$X$，得：
$$
\frac{d X / d t}{X}=Y \frac{d F / d t}{X}-K_d  
$$


而
$$
\begin{gathered}
    \frac{d F}{d t}=\frac{d\left(S_0-S\right)}{d t}=-\frac{d S}{d t} \\
    U_s=-\frac{d S / d t}{X} \\
    \mu=\frac{d X / d t}{X}=\frac{1}{\theta_c}
\end{gathered}
$$

得：
$$
\frac{1}{\theta_c}=Y U_s-K_d
$$


因为
$$
U_s=v=\frac{v_{\max } S_e}{K_s+S_e}=K_2 S_e
$$

所以
$$
\begin{aligned}
    S_e & =\frac{K_s\left(1+K_d \theta_c\right)}{\theta_c\left(Y v_{\max }-K_d\right)-1} \\
        & =\frac{1 / \theta_c+K_d}{Y K_2}
\end{aligned}    
$$

因为	
$$
U_s=\frac{S_0-S_e}{X t}=\frac{S_0-S_e}{X \theta}
$$	 

所以	
$$
X=\frac{\theta_c}{\theta} \cdot \frac{Y\left(S_0-S_e\right)}{1+K_d \theta_c}
$$	    