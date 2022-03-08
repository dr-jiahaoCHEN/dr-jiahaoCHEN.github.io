---
layout: post
title: The Elements of Statistical Learning notes 2.1-2.2
date: 2022-03-08 23:18 +0800
last_modified_at: 2022-03-08 23:18 +0800
tags: [ESL, EN]
math: true
toc:  true
---

# The Elements of Statistical Learning notes 2.1-2.2

*Augest大魔王 2022-03-08*

This article is about the notes of [《The Elements of Statistical Learning learning》](https://github.com/dr-jiahaoCHEN/Mathematics-and-Statistics/blob/main/book%26notes/The%20Elements%20of%20Statistical%20Learning/(Springer%20Series%20in%20Statistics)%20Trevor%20Hastie%2C%20%20Robert%20Tibshirani%2C%20Jerome%20Friedman%20-%20The%20Elements%20of%20%20Statistical%20Learning_%20%20Data%20Mining%2C%20Inference%2C%20and%20Prediction.-Springer%20(2013).pdf), which mainly involves part of the first two chapters. This part is mainly for introduction and basic concepts.

## 1.Introduction
**inputs**, which can be measured or preset. These variables affect one or more **outputs**. It is to use the input variables to predict the output value. Such a process is called supervised learning. In statistics, **inputs** are often called **predictors**, and may also be called **independent variables**. In pattern recognition, they are called**features**. **outputs** are called **responses** and can also be called **dependent variables**.


## 2.Variable and Terminology

The type of output variable can be divided into quantitative variable and qualitative variable, according to the different measurements. Qualitative variables are also called **categories** or **discrete variables**, also known as **factors**.

For both types of output variables, it makes sense to consider using the input variables to predict the output variables. When we predict quantitative output it is called **regression**, when we predict qualitative output it is called **classification**. We will see that these two tasks have a lot in common, in particular, both can be viewed as **function approximation**.

There are also various types of input variables. In addition to quantitative variable and qualitative variable, there is a third type named  **ordered categorical**, such as small, medium and large. Among these values. There is an order between, but there is no proper notion of measurement (the difference between medium and small need not be equal to the difference between large and medium).

Qualitative variables are often represented by numerical codes. In the simplest case there are only two categories, such as "success" and "failure", "survival" and "death". These are often represented by a single binary number, such as 0 or 1, or by -1 and 1. These codes are sometimes called **targets**. When there are more than two categories, there are other feasible options. The most useful and commonly used encoding is **dummy variables**. There are K levels of qualitative variables represented by a K-bit binary variable, only one of which is on at a time. The dummy variables are symmetric in the hierarchy of factors, although more compact coding schemes are possible.

We will often denote input variables by the notation \\\(X\\\). If \\\(X\\\) is a vector, its components can be subscripted \\\(X_{j }\\\) to remove .

Quantitative output variables are represented by \\\(Y\\\), and qualitative output variables are represented by \\\(G\\\).

We use capital letters \\\(X, Y, G\\\) to denote variables, and we denote observations of variables in lowercase letters; thus the first observation of \\\(X\\\) are written as \\\(x_{i}\\\)

For example, \\\(N \times p\\\) matrix \\\(\mathbf{X}\\\) can be written as:

$$
\mathbf{X}=\left[
\begin{matrix}
 x_{11}      &  x_{12}      & \cdots &  x_{1p}      \\
 x_{21}      &  x_{22}      & \cdots &  x_{2p}      \\
 \vdots & \vdots & \ddots & \vdots \\
  x_{N1}      & x_{N2}      & \cdots & x_{Np}      \\
\end{matrix}
\right]
$$

Usually we represent dimensions as columns and observations as rows. So, according to the above matrix, each row is an input vector and each column is a dimension.

We simply define statistical learning as follows: Given an input vector \\\(X\\\), make a good estimate of the output \\\(Y\\\), denoted as \\\(\hat{Y} \\\). And if \\\(Y\\\) evaluates to the real number \\\(\mathbf{R}\\\), then \\\(\hat{Y}\\\) evaluates to Also a real number \\\(\mathbf{R}\\\); Similarly, for categorical output, \\\(\hat{G}\\\) takes the value corresponding to \\\(G\\\) A set of values \\\(\mathcal{G}\\\).