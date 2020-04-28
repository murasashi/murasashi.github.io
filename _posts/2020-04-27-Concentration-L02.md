---
title: Information Content of Upper Boundary Crossing Event
author: Murasashi
date: 2020-04-28 16:00:00 +0400
categories: [Research] 
tags: [optimism, Ville's inequality]
---

# Concentration Lecture 02

> How to tame the maximal empirical process $\|\langle X_{[t]}, \epsilon_{[t]}\|_{\infty}$?

- Make a version of sub-Gaussian martingale difference.
- What is the automated holds assumptions from _supermartingale_ and _submartingale_?

## Structure

1. Sub-Gaussian Process
2. Sub-Gaussian Empirical Process
3. Sub-Gaussian Maximal Empirical Process

## Preparation: Boundary Crossing of Martingale

### Gibbs distribution

The lego is 
$$\exp(\lambda Z)/\psi_{Z}(\lambda)$$

### Sub Gaussian
$$\psi_{Z_i-\mu_i}(\lambda) \le \sigma_i^2\frac{\lambda^2}{2}$$

## Point 01: Boundary Crossing of Sub-Gaussian Process

A gentle start is to handle the __partial sum process of sub-Gaussian martingale difference__ $\{\sum_{s=1}^{t}Z_{s}\}$, which is defined as 

$$
\log E[\exp(\lambda Z_{s})| \mathcal{F}_{s-1}] \le \sigma^2_{s}\cdot \frac{\lambda^2}{2}\text{    for all   }\lambda \in \mathbb{R}.
$$


## Point 02: Boundary Crossing of Sub-Gaussian Empirical Process

The event we handle in this part is the process $\{\sum_{s=1}^{t}X_{js}\epsilon_{s}\}$.  First, its _upper deviation event_ reads as

$$
\{\sum_{s=1}^{t}X_{js}\epsilon_{s} > C_{jt}\}
$$
and our goal is to find the __confidence sequence__ $\{C_{js}\}_{s=1}^{\infty}$ based on __user-sepcified confidence level__ $\alpha$ such that the process is __never__ cross the confidence sequence at any time step with probability at least $1-\alpha$; formally, that is 

$$
\mathbb{P}(\forall t \ge 1:\sum_{s=1}^{t}X_{js}\epsilon_{s} \le C_{jt} ) \ge 1-\alpha.
$$

## Point 03: Boundary Crossing of Sub-Gaussian Process Maximal Empirical Process

The key is to note

$$
\|\langle X_{[t]}, \epsilon_{[t]}\rangle\|_{\infty} = \sup_{j \in [d]}|\sum_{s=1}^{t}X_{js}\epsilon_{s}|
$$

and hence a family of representations on upper deviation event is

$$
\{\|\langle X_{[t]}, \epsilon_{[t]}\rangle\|_{\infty}  < C\} = \cap_{j \in [d]}\{|\sum_{s=1}^{t}X_{js}\epsilon_{s}|<C_{s}\}\text{ such that } \sum_{s=1}^{d}C_{s}=C.
$$

Without further knowledge on the dependency between contexts, one can choose $C_s=C/d$ for all $s=1,...,d$.

- (Can we involve multiple testing technique in this case?)
