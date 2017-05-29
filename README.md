# Decision Tree
Machine Learning: Decision Tree. Function Approximation.

## Assumptions
Grow tree just big enough to fit correct labeled data.
So short decision tree is more preferable than long.
> Occam's razor: prefer the simplest hypothesis that fit the data

## Properties
- can approximate any discrete function
- we should should choose first parameter which reduce maximum of entropy:

```
I(X,Y) = H(X) - H(X|Y)

where:
H(X) = - sum(P(X=i) * log2(P(X=i))) for i in [1, n]
H(X|Y=v) = -sum(P(X=i|Y=v) * log2(P(X=i|Y=v)) for i in [1, n]
H(X|Y) = sum(P(Y=v) * H(X|Y=v)) for v in Y
```

## Related

1. [No Free Lunch Theorem](https://en.wikipedia.org/wiki/No_free_lunch_theorem) *we can't really get a program to guess
a right function until it has seen all of examples*.

# Link

1.
