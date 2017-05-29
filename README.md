# Decision Tree
Machine Learning: Decision Tree 

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

# Link

1.
