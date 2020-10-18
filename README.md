# 1. Fibonacci Numbers

### 1.1 Naive

```pseudocode
Function FibRecurs(n)
if n ≤ 1: return n
else:
return FibRecurs(n−1) + FibRecurs(n−2)
```

### 1.2 Improved Method

```pseudocode
Function FibList(n)
create an array F[0...n] F[0] ← 0
F[1] ← 1
for i from 2 to n: 
	F [i] ← F [i − 1] + F [i − 2] 
return F[n]
```

- Big-O：

<img src="https://s1.ax1x.com/2020/10/18/0XrOGq.png" width="500">

Note: Normally additions are **constant time**, but now these are larger numbers. The n-th Fibonacci number has about over 5 digits to it, they often won't fit in the machine word. If you think about what happens if you add two very big numbers together, you sort of add the tens of digit and then carry, so on and so forth. We should have to do work for each digits place. And so the amount of work we should do is proportional to the number of digits. And in this case, the number of digits is proportional to n, so `F[i] <- F[i-1] + F[i-2]` should take `O(n)` time.



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



