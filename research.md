---
layout: default
---

# Research

<br>

## Multi-armed bayesian bandit for Email Send Time Optimization

The objective of building a reliable Send Time Optimization (STO) engine is the following: send emails to each of the customers with the best possible timing when the customers are the most receptive. Some subscribers prefer to receive newsletters early in the morning, others take the time to scan their inboxes in the evening.  From the sender’s point of view, it is desirable to always deliver at the right time.

Deciding which time slot to send promotional emails is a huge challenge for many companies.

One common approach is to choose different send times and measure the Open Rate (OR) of the emails for each time slot. At some point, when the measured OR for one specific slot exceeds that of the other slots, we will switch to the one with the highest for all customers. Algorithms for solving this problem are called bandit algorithms. For my analysis I implemented a **Multi-Armed Bayesian Bandit Algorithm**.
<br>


### math (start with bayesian) stucchio all the sections in general and priors + mathematical approach in STO (priors): APPROACH

The goal of the bandit algorithm is to do the following: display all possible time slots to a random selection of users, and measure in which time slots the emails are opened more frequently. Over time, it will use these observations to infer which send times have the higher OR. Then, once the estimation of the OR becomes more precise, it will preferentially display the time slots with the higher OR.

In our model, we have \\( N \\) possible time slots, each of which has an email open rate \\( \theta_i \\). Unfortunately we do not know what \\( \theta_i \\) is, but we can construct a probability distribution which represents our belief about what the actual value of \\( \theta_i \\) is. This is called a Bayesian Approach.

In Bayesian reasoning, the fundamental goal is to compute a posterior distribution on \\( \theta_i \\). This means we want to find a function \\( f(x) \\) with the property that:

\\[ P(a < \theta_i < b) = \int_a^b f(x) dx \\]

In graphical terms, the probability that \\( a < \theta_i < b \\) can be interpreted as the area under the curve of the graph of \\( f(\theta) \\):

![image](https://www.chrisstucchio.com/blog_media/2013/bayesian_analysis_conversion_rates/posterior_distribution.png)

The function \\( f(x) \\) represents our beliefs about \\( \theta_i \\) - it is an inherently subjective matter. It depends on our beliefs about what typical values of \\( \theta_i \\) might be as well as the evidence we have seen. What Bayesian analysis provides us with is an objective method of altering \\( f(x) \\) based on the evidence we have about it.

The basic idea behind Bayesian methods is to update our beliefs based on evidence. As we gather more data by sending emails in different time slots to other users and observing the open rates, we can incrementally narrow the width of the probability distribution.

As in all Bayesian inference, we need to choose a prior. The prior is something we believe to be true before we have any evidence. This is just a starting point - after enough evidence is gathered, our prior will play a very minimal role in what we actually believe. Choosing a good prior is important both for mathematical simplicity, and because if your prior is accurate, you don't need as much evidence to get the correct answer.

If the prior probability distributions are in the same family as the posterior distributions, then they are known as conjugate distributions, and the prior is known as the conjugate prior to the likelihood function. In simpler terms, if we know the distribution of the likelihood function, we can determine the distribution of the posterior and prior.

In our case, since we are measuring a binary outcome (did somebody open or not the email), we know that we are dealing with the Bernoulli distribution, making our likelihood:

\\[ \large P(X \mid\theta) = \prod_{i=1}^N \theta^{x_i}(1-\theta)^{1-x_i} \\]

The conjugate prior to the Bernoulli distribution is the Beta distribution:

\\[  P(\theta_i=x) = \frac{ x^{\alpha_i-1}(1-x)^{\beta_i-1} }{B(\alpha_i, \beta_i)} \equiv f_{\alpha_i,\beta_i}(x) \\]


The parameters \\( \alpha_i, \beta_i > 1 \\) are the prior parameters.





Incorporating priors:

 in my model we have information from each contact for one year.
One reasonable choice is αi=βi=1, which amounts to the uniform distribution on [0,1]. What this means is that we are assuming that all possible values of θi are equally likely. Depending on the circumstances (which I'll explain shortly), we might want to choose other possible values.

Hi, we started with priors based on all the users with past data for a given client. The priors depend on the aggregated open rate of all relevant contacts. We use these priors for each bandit.


Updating our beliefs

Optimizing click throughs





block:
\\[ \frac{1}{n^{2}} \\]
<br>
<br>

inline
\\( 1/x^{2} \\)

inline
\\( 1/x^{2} \\)

Block:
\\[ P(a < \theta_i < b) = \int_a^b f(x) dx \\]

Block:
\\[ P(a < \theta_i < b) = \int_a^b f(x) dx \\]

### steps algorithm to sum up (Sto)
### application to email campaign (STO)
### results (Pulls and OR)



<br>
<br>
