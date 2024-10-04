# Uncertainty

![alt text](image-44.png)

![alt text](image-45.png)

![alt text](image-46.png)

## Probability

Possible Worlds - ω

P(ω)

* Probability will range from 0 and 1

0 <= P(ω) <=1

![alt text](image-47.png)

for example in a dice each number will have 1/6 of probability.

* What if we have two dice

All of the possible worlds are

![alt text](image-48.png)

and their sum are

![alt text](image-49.png)

P(sum to 12) = 1/36
P(sum to 7) = 6/36 = 1/6

## Unconditional Probability

degree of belief in a proposition in the absence of any other evidence.

## Conditional Probability

degree of belief in a proposition given some evidence that has already been revealed

e.g. P(a|b)
what is the probability of a given b
e.g.  
P(rain today | rain yesterday)

e.g.  
P(route change | traffic conditions)

e.g.  
P(disease | test results)

### How to calculate conditional probability

![alt text](image-50.png)

## random variable

a variable in probability theory with a domain of possible values it can take on  
e.g.  
Weather - {sun, cloud, rain, wind, snow}  
traffic - {none, light, heavy}  
Flight - {on time, delayed, cancelled}  

probability distribution  
P(Flight = on time) = 0.6  
P(Flight = delayed) = 0.3  
P(Flight = cancelled) = 0.1

This notation a little bit might be confusing  
P(Flight) = <0.6,0.3,0.1>

### independence

the knowledge that one event occurs does
not affect the probability of the other event

![alt text](image-52.png)

### Bayes' Rule
Bayes' Rule, also known as Bayes' Theorem, is a fundamental concept in probability theory that describes how to update the probability of a hypothesis based on new evidence. It provides a way to calculate the posterior probability (the updated probability of an event) given the prior probability (the initial belief) and the likelihood of observing the evidence.

Intuition
Bayes' Rule helps in understanding how new evidence affects your belief about a hypothesis. If the evidence is highly likely given the hypothesis, the posterior probability increases. Conversely, if the evidence is unlikely given the hypothesis, the posterior probability decreases.

![alt text](image-53.png)

![alt text](image-55.png)

![alt text](image-56.png)

>> knowing  
P(cloudy morning | rainy afternoon)  
We can calculate
P(rainy afternoon | cloudy morning)  

>> Knowing  
P(visible effect | unknown cause)
We can calculate  
P(unknown cause | visible effect)

```
Knowing
P(blurry text | counterfeit bill)
We can calculate
P(counterfeit bill | blurry text)
```

## Joint Probability

**Joint probability** refers to the probability of two or more events happening simultaneously. It is the likelihood that two (or more) events occur at the same time or in conjunction with one another.

For two events, A and B, the joint probability is denoted as `P(A ∩ B)`, which represents the probability that both A and B happen together.

## Formula for Joint Probability

If A and B are independent events (meaning the occurrence of one event does not affect the other), the joint probability can be calculated as:

P(A ∩ B) = P(A) × P(B)



![alt text](image-57.png)