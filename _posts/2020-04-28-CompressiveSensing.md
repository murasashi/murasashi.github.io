---
title: Coherence, Restricted Eigenvalue and Random Matrices Concentration
author: Murasashi
date: 2020-04-28 16:00:00 +0400
categories: [Harmonic Analysis] 
tags: [coherence, measurement matrix]
---

# Compressive Sensing 01

> How to measure the __suitability__ of the measurement matrix in recovery algorithms?

## Learning Objective

1. We define on the space of matrix the __coherence function__ and __$l_1$ coherence function__ that concern __the maximal absolute correlations among measurements__ from difference aspect.

## Point 01:

### Working matrix assumptions
We are working with __$l_2$-normalized__ matrix, in the sense that for a $n\times p$ real matrix $A$, all its column $a_1, ..., a_{n}$ has _unit $l_2$ norm_, i.e., $\|a_i\|_2=1$ for all $i\in [n]$.

### Coherence of a matrix.

The __coherence__ $\mu(A)$ of a $l_2$-normalized matrix $A$ is defined as __the maximal absolute correlations among its rows__; formally,

$$
\mu(A) \equiv \max_{1\le i \neq j \le n}|\langle a_i, a_j \rangle|.
$$

The range of the coherence is between 0 and 1, corresponding to extreme case of _orthogonality_ and _linear dependency_. First, orthonormal measurement system gives $\mu(A)=0$. Second, from Cauchy-Swartz inequality, $|\langle a_i, a_j \rangle| \le \|a_i\|_2\|a_j\|_2$ and we are working with $l_2$-normalized matrix, the coherence is bounded by 1,
$$
\mu(A) \le 1.
$$

### $l_1$-coherence function

The __$l_1-$coherence function $\mu_1$__ of a matrix $A$ maps __sparsity parameter $s$__ to the __maximal size-s pivotal total absolute correlations__; that is,

$$
\mu_{1}(s) \equiv\max_{i\in[n]}\max\bigg\{\sum_{j\in S}|\langle a_i, a_j \rangle| ; i\notin S, \text{card}(S)=s, S \subset [n]\bigg\}
$$

### Key lemma: Interval Approximate of _Restricted Eigen-Value_

> __Theorem__ For all __s-sparse vectors__ $x\in\mathbb{R}^{n}$, it holds
>  $$\frac{\|Ax\|_2^2}{\|x\|_2^2} \in [1-\mu_1(s-1), 1+\mu_1(s-1)].\hspace{20 pt}(\clubsuit)$$ 

- $(\clubsuit)$ is the source of studies on __Restricted Isometry Property__

## Point 02:

## Point 03:

## Summary
