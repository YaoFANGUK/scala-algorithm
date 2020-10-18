# 1. Fibonacci Numbers

### 1.1 Naive

```pseudocode
Function FibRecurs(n)
if n ≤ 1: return n
else:
return FibRecurs(n−1)+FibRecurs(n−2)
```

### 1.2 Improved Mehod

```pseudocode
Function FibList(n)
create an array F[0...n] F[0] ← 0
F[1] ← 1
for i from 2 to n:
F [i ] ← F [i − 1] + F [i − 2] return F[n]
```



# 2. Greatest Common Divisors

### 2.1 Naive

```pseudocode
Function NaiveGCD(a,b)
best ← 0
for d from 1 to a+b:
if d|a and d|b: best ← d
return best
```

### 2.2 Euclidean Algorithm

```pseudocode
Function EuclidGCD(a,b)
if b = 0: return a
a′ ← the remainder when a is divided by b
return EuclidGCD(b,a′)
```



