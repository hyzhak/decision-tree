# Decision Tree
Machine Learning: Decision Tree. Function Approximation.

## Assumptions
Grow tree just big enough to fit correct labeled data.
So short decision tree is more preferable than long.
> Occam's razor: prefer the simplest hypothesis that fit the data

## Properties
- can approximate any discrete function
- we should should choose first parameter which reduce maximum of entropy (ID3)

```
I(X,Y) = H(X) - H(X|Y)

where:
H(X) = - sum(P(X=i) * log2(P(X=i))) for i in [1, n]
H(X|Y=v) = -sum(P(X=i|Y=v) * log2(P(X=i|Y=v)) for i in [1, n]
H(X|Y) = sum(P(Y=v) * H(X|Y=v)) for v in Y
```

We shouldn't use error rate criteria (what we care about) because 
we can get stuck in local minimal
- C4.5


## Reduced-Error Pruning (Overfitting)

Split data into training and validation set
Create tree that classifies training set correctly
Do until further pruning is harmful:
1. Evaluate impact on validation set of pruning each possible node (plus those below it)
2. Greedily remove the one that most improves validation set accuracy

* produces smallest version of most accurate subtree

## Related

1. [No Free Lunch Theorem](https://en.wikipedia.org/wiki/No_free_lunch_theorem) *we can't really get a program to guess
a right function until it has seen all of examples*.
2. Kearns-Mansour’96 [On the Boosting Ability of Top-Down Decision Tree Learning Algorithms](https://www.cis.upenn.edu/~mkearns/papers/topdown.pdf)

# Link

1. [10-601, Spring 2015 by Tom Mitchell and Maria-Florina Balcan](http://www.cs.cmu.edu/~ninamf/courses/601sp15/lectures.shtml)
