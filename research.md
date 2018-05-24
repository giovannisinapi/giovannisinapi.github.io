---
layout: default
---

# Research

<br>

## Multi-armed bayesian bandit for Email Send Time Optimization

The objective of building a reliable Send Time Optimization (STO) engine is the following: send emails to each of the customers with the best possible timing when the customers are the most receptive. Some subscribers prefer to receive newsletters early in the morning, others take the time to scan their inboxes in the evening.  From the sender’s point of view, it is desirable to always deliver at the right time.

Deciding which time slot is the the most effective one to send promotional emails is a huge challenge for many companies.

One common approach is to choose different send times and measure the Open Rate (OR) of the emails for each time slot. At some point, when the measured OR for one specific slot exceeds that of the other slots, we will switch to the one with the highest for all users. Algorithms for solving this problem are called bandit algorithms. For my analysis I chose a **Multi-Armed Bayesian Bandit Algorithm**.
<br>

The new equations is:

$$T =\frac{a}{c} $$


![alt text](https://cdn-images-1.medium.com/max/1600/1*Tt8A6mP98ibBlrlFD5UJxg.png)

<br>
<br>



### math (start with bayesian) stucchio
### steps algorithm (Sto)
### application to email campaign (STO)
### math (STO)
### results (Pulls and OR)



<br>
<br>




## Syntax

The syntax to specify an equation uses dollar signs `$`. If you want to
literally display a dollar sign you can use `\$`.

1.  **Displayed equations** are delimited by `$$`. Here is an example:

    ````
    ... Here she comes to wreck the day. it's because i'm green isn't it! hey,
    maybe i will give you a call sometime. your number still 911?

    $$
    R_{\mu \nu} - {1 \over 2}g_{\mu \nu}\,R + g_{\mu \nu} \Lambda
    = {8 \pi G \over c^4} T_{\mu \nu}
    $$

    kinda hot in these rhinos. look at that, it's exactly three seconds before i
    honk your nose and pull your underwear over your head ...
    ````

    You can also use the delimiters `\[ ... \]` for display equations. Here is
    an example:

    ````
    ... Here she comes to wreck the day. it's because i'm green isn't it! hey,
    maybe i will give you a call sometime. your number still 911?

    \[
    R_{\mu \nu}- {1 \over 2}g_{\mu \nu}\,R + g_{\mu \nu} \Lambda
    = {8 \pi G \over c^4} T_{\mu \nu}
    \]

    kinda hot in these rhinos. look at that, it's exactly three seconds before i
    honk your nose and pull your underwear over your head ...
    ````

    You do not have to separate a displayed equation block from other blocks
    with blank lines. You can also include content on the same lines as the
    delimiters with the restriction that the opening delimiter must be placed at
    the beginning of its line and the closing delimiter must be placed at the
    end of its line:

    ````
    ... Here she comes to wreck the day. it's because i'm green isn't it! hey,
    maybe i will give you a call sometime. your number still 911?
    $$ R_{\mu \nu} - {1 \over 2}g_{\mu \nu}\,R + g_{\mu \nu} \Lambda
    = {8 \pi G \over c^4} T_{\mu \nu} $$
    kinda hot in these rhinos. look at that, it's exactly three seconds before i
    honk your nose and pull your underwear over your head ...
    ````

2.  **Inline equations** are delimited by `$`. Here is an example:

    ````
    ... Here she comes to wreck the day. $\int -xe^{x^2} dx$ it's because i'm
    green isn't it! hey, maybe i will give you a call sometime. your number
    still 911? kinda hot in $\int -xe^{x^2} dx$ these rhinos. look at that,
    it's exactly three seconds before i honk your $\int -xe^{x^2} dx$ nose and
    pull your underwear over your head ...
    ````

    You can also use the delimiters `\( ... \)` for inline equations. Here is
    an example:

    ````
    ... Here she comes to wreck the day. \(\int -xe^{x^2} dx\) it's because i'm
    green isn't it! hey, maybe i will give you a call sometime. your number
    still 911? kinda hot in \(\int -xe^{x^2} dx\) these rhinos. look at that,
    it's exactly three seconds before i honk your \(\int -xe^{x^2} dx\) nose and
    pull your underwear over your head ...
