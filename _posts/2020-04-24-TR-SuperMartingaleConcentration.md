---
title: Hoeffding's inequality for super martingales. (Technical Review)
author: Murasashi
date: 2020-04-24 04:00:00 +0400
categories: [Probability, Concentration, Martingale] 
tags: [supermartingale, exponential markov inequality]
---



# Main Reference

>Hoeffding's inequality for super martingales.


##  Structure

- Elements
- Arguments
- Stories

## Layer 01: Elements

There are five elements
1. Supermartingale difference sequence
2. Quadratic characteristic
3. Exponential Multiplicative Martingale
4. Conjugate Probability Measure
5. Cumulant Process

### Supermartingale difference sequence

$$
\{(\xi_s. \mathcal{F}_{s})\}_{s=1}^{T}
$$

### Quadratic characteristic

$$
\langle X \rangle_{k} \equiv \sum_{s=1}^{k}E[\xi_{s}^2|\mathcal{F}_{s-1}] \hspace{20pt} k = 0,1,...., T.
$$

### Exponential Multiplicative Martingale

$$
Z_{k}(\lambda) \equiv \prod_{s=1}^{k} 
\frac{e^{\lambda \xi_{s}}
}{ E(e^{\lambda \xi_{s}}|\mathcal{F}_{s-1})
}, ~~~~~Z_0(\lambda) = 1,~~~~~\lambda \ge 0.
$$

- Martingale associate with Gibbs distribution

### Conjugate Probability Measure

Let $S$ be a random time.

$$
d\mathbb{P}_{\lambda} \equiv Z_{S\wedge T}(\lambda)d\mathbb{P}.
$$

### Cumulant Process

$$
\Psi_{k}(\lambda) = \sum_{s=1}^{k}\log E(e^{\lambda\xi_{s}}|\mathcal{F}_{s-1})~~~~~0\le k \le T.
$$



## Layer 02: Arguments

1. Bernett's lemma.
2. Hoeffiding's lemma.
3. Bounding cumulant by quadratic characteristic--general condition.
4. Bounding cumulant by quadratic characteristic--2nd order condition.

### Bernett's lemma.


### Hoeffiding's lemma.


###  Bounding cumulant by quadratic characteristic--general condition.


### Bounding cumulant by quadratic characteristic--2nd order condition.



## Layer 03: Stories

1. Exponential Markov inequality
2. Conjugate distribution technique
