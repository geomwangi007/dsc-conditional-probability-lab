# Conditional Probability - Lab

## Introduction

In order to be ready for real-world applications of probability, it is important to understand what happens when probabilities are not independent. Very often, the probability of a certain event depends on other events happening! Let's see how this all works in this lab.

## Objectives

You will be able to:

* Differentiate between independent and dependent events
* Use the multiplication rule to find the probability of the intersection of two events

## Exercise 1
A coin is tossed and a single 6-sided die is rolled. Find the probability of landing on the head side of the coin and rolling a 3 on the die.


```python
head_on_coin = 1/2
three_on_a_dice = 3/6

head_on_coin_and_three_on_a_dice = 1/2 * 1/6

head_on_coin_and_three_on_a_dice = 0.08333333333333333
```

## Exercise 2


After conducting a survey, one of the outcomes was that 8 out of 10 of the survey subjects liked chocolate chip cookies. If three survey subjects are chosen at random **with replacement**, what is the probability that all three like chocolate chip cookies?


```python
prob_of_liking_choc_cookies = 8/10
prob_of_three_liking_choc_cookies = 0.8*0.8*0.8 

prob_of_three_liking_choc_cookies = 0.5120000000000001
```

## Exercise 3
70% of your friends like chocolate flavored ice cream, and 35% like chocolate AND like strawberry flavors.

What percent of those who like chocolate also like strawberry?


```python
choc_and_strawberry = 0.35 / 0.7
choc_and_strawberry = 0.5
```

50% of your friends who like chocolate also like strawberry

## Exercise 4
What is the probability of drawing 2 consecutive aces from a deck of cards. 


```python
first = 4/52
second = 3/51

two_consecutive = first * second

two_consecutive = 0.004524886877828055
```

## Exercise 5
In a manufacturing factory that produces a certain product, there are 100 units of the product, 5 of which are defective. We pick three units from the 100 units at random. 

What is the probability that none of them are defective?
Hint: Use the chain rule here!


```python
first_pick = 95/100
second_pick = 94/99
third_pick = 93/98

prob_of_none_being_defective = first_pick*second_pick*third_pick
prob_of_none_being_defective = 0.8559987631416203
```

## Exercise 6

Let's consider the example where 2 dice are thrown. Given that **at least one** of the die has come up on a number higher than 4, what is the probability that the sum is 8?

Let $i,j$ be the numbers shown on the dice. The events $A$ and $B$ are described below:

* **Event $A$ is when either $i$ or $j$ is 5 or 6** (keep an eye on either - or)
* **Event $B$ is when $i + j = 8$**


* What is the size of sample space $\Omega$ ?
* What is $P(A \cap B)$ ?
* What is $P(A)$ ?
* Use above to calculate $P(B \mid A)$


```python
#The total number of possible outcomes (size of the sample space 6*6 = 36
# P(at least 1 die is greater than 4) = P(A) = 20/36
Probab_of_B_given_A = (4/36)/(20/36) 
Probab_of_B_given_A = 0.19999999999999998

```

## Exercise 7

Let's consider a credit card example. At a supermarket, customers are selected randomly, the store owner recorded whether costumers owned a Visa card (event A) or an Amex credit card (event B). Some customers own both cards.
You can assume that:

- $P(A)$ = 0.5
- $P(B)$ = 0.4
- both $A$ and $B$ = 0.25.


With the knowledge we have about conditional probabilities, compute and interpret the following probabilities:

- $P(B \mid A)$
- $P(B' \mid A)$
- $P(A \mid B)$
- $P(A' \mid B)$



```python
Probab_of_B_given_A = 0.25/0.5  
Probab_of_B_prime_given_A = 1 - 0.5
Probab_of_A_given_B = 0.25/0.4
Probab_of_A_prime_given_B = 1 - 0.625


print('The Probab_of_B_given_A is' , Probab_of_B_given_A)
print('The Probab_of_B_prime_given_A is ' , Probab_of_B_prime_given_A)
print('The Probab_of_A_given_B is' ,Probab_of_A_given_B)
print('The Probab_of_A_prime_given_B is' , Probab_of_A_prime_given_B)


The Probab_of_B_given_A is 0.5
The Probab_of_B_prime_given_A is  0.5
The Probab_of_A_given_B is 0.625
The Probab_of_A_prime_given_B is 0.375
```

## Summary 

In this lab, you practiced conditional probability and its theorem with some simple problems. The key takeaway from this lab is to be able to identify random events as dependent or independent and calculating the probability of their occurrence using appropriate methods. Next, you'll learn about some more conditional probability axioms, building on the knowledge we have so far. 
