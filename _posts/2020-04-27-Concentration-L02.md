---
title: Information Content of Upper Boundary Crossing Event
author: Murasashi
date: 2020-04-27 16:00:00 +0400
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


### Ville's inequality

> __Lemma__. Given a non-negative supermartingale $\{L_{t}\}_{t=0}^{\infty}$.  Then, 
> $$\mathbb{P}(\exists t \ge 1: L_{t} \ge x) \le x^{-1}E[L_0].$$

- Two inequalities contributes the proof of Ville's inequality: (1) supermartingale definition and (2) The case of _never_ cross the level $x$. 
	- (1)From the definition of supermartingale, we always have $E[L_0] \ge E[L_{t}]$.
	- In particular, for any stopping time $N$, one has $E[L_0] \ge E[L_{N}]$.
	- Consider the stopping time $N$ that the supermartingale $\{L_{t}\}$ __hits__ the boundary (level x); formally $N\equiv\inf\{t\ge 0: L_{t} \ge x\}$.
	- Then the event $\{N=\infty\}$ means the supermartingale _never_ hits the boundary; by the same token, the event  $\{N<\infty\}$ means the the supermartingale hits the boundary _at some point_.
	- (2) The expected value of supermartingale at stopping time $N$ now has decomposition $E[L_{N}]=E[L_{N}|N<\infty]P(N<\infty)+E[L_{N}|N=\infty]P(N=\infty)$.
	- Since the supermartingale is required to be __non-negative__, we further have $E[L_{N}]\ge E[L_{N}|N<\infty]P(N<\infty)=E[x^{-1}L_{N}|N<\infty]\cdot xP(N<\infty)$
	- By the definition of stopping time, $E[x^{-1}L_{N}|N<\infty]$ is at least greater than $1$, thus we further have $E[L_{N}]\ge xP(N<\infty)$. 
- Therefore, we have proved the Ville's inequality, stated as $$\mathbb{P}(\exists t \ge 1: L_{t} \ge x) =P(N<\infty)\le x^{-1}E[L_{N}]\le x^{-1}E[L_{0}].$$

### Working supermartingale from Cumulant Generating Function.

Suppose we have a __mean zero__ noise sequence $\{\epsilon_{s}\}_{s=1}^{\infty}$ such that each noise $\epsilon_{s}$ has __sub-$\psi$__ cumulant generating function(CGF) $\psi_{\epsilon_{s}}(\lambda)$; namely, for all $\lambda$ in the _effective domain_ of  $$\psi_{\epsilon_{s}}(\lambda)\equiv\log E[\exp(\lambda \epsilon_{s})]\le \psi_{s}(\lambda).$$
Then, it associated a __product supermartingale ratio sequence__ $Q M_{s}$  defined as $$Q M_{s} = \exp( [\lambda\epsilon_{s}-\psi_{s}(\lambda)]),$$
where $Q$ is the __ratio operator__ such that $Q x_{t} = x_{t}/x_{t-1}$.

> Note: $\Delta$ is the __difference operator__ such that $\Delta x_{t} = x_{t}-x_{t-1}$. 

Then, the product supermartingale sequence is $$M_{t} = \prod_{s=1}^{t}QM_{s} = \exp(\sum_{s=1}^{t} [\lambda\epsilon_{s}-\psi_{s}(\lambda)]) = \exp(\lambda [\sum_{s=1}^{t}\epsilon_{s} - \sum_{s=1}^{t}\psi_{s}(\lambda)]).$$

In particular, the Ville's inequality in this case says for given __confidence budget__ $\alpha$, we have argument $$\alpha \ge P(\exists t \ge 1: M_{t} \ge \alpha^{-1}),$$
which resulting a __confidence sequence__ of the noise process $\{\epsilon_{s}\}_{s=1}^{\infty}$.

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
