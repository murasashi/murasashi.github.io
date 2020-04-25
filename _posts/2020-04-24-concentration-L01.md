---
title: Information Content, Upper Deviation, and Chernoff Argument.
author: Murasashi
date: 2020-04-26 16:00:00 +0400
categories: [Probability, Concentration] 
tags: [information_content, information_entropy]
---

# Concentration Lecture 01

## Learning Objective

1. Information Content
2. Upper Deviation Event
3. Chernoff Argument for batch setting concentration


## Point 01: Information Content

### Intuitive Definition
We start from a basic concept in [information theory](https://en.wikipedia.org/wiki/Information_theory "Information theory"),  the [Information Content](https://en.wikipedia.org/wiki/Information_content) (also known as **Shannon information**).  The **_information content_** is to 
quantify the level of __"surprise"__ of a particular event occurring from a __random variable__ or a __stochastic process__. The **_expected information content_** is termed as [information theoretic entropy](https://en.wikipedia.org/wiki/Entropy_(information_theory) "Entropy (information theory)") and hence is to quantified __''how surprising''__ of that particular event __''on average"__ with respective to the uncertainty modeled by the random variable or the stochastic process. 

> __Information Content__ measures how surprising an event is.

>__Information Entropy__ summarizes "how surprising an event is" on average.

### Formal Definition

Formally, given a particular event $A$ occurring from probability measure $\mathbb{P}$, the __''surprise''__ is believed to be inversely proportional to its probability ; that is 

$$\textbf{''surprise''}\text{of the event } A \text{ under probability} \mathbb{P} \propto \frac{1}{\mathbb{P}(A)}.$$

If you pray for such belief, then the intuitive definition of **_information content_** $\text{IC}_{\mathbb{P}}(A)$ suggests its ~~one possible~~  formal definition by the __log-reciprocal of the probability__:

$$
\text{IC}_{\mathbb{P}}(A)\equiv \log \frac{1}{\mathbb{P}(A)}  \hspace{20pt} (\clubsuit).
$$

In the language of Statistics, $(\clubsuit)$ is named __negative log-likelihood__ of event $A$ under probability measure $\mathbb{P}$.

### Explanation



## Point 02: Upper Deviation Event

## Point 03: Chernoff Argument for batch setting concentration



## Wrap-up and Next step

- Extend from Information Content
	+ Relative entropy
		+ Bregman Divergence
