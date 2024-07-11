# DSAL
Data Structures and Algorithms - Python
## GCD
### Common Algo

```
def gcd(a,b):
    result = min(a,b)

    for _ in range(result,0,-1):
        if (a%_ == 0) and (b%_ == 0):
           break
        else:
            result  = result - 1
    return result
```
            
### Euclidean Algo
```
def GCD_eculidean(a:int,b:int):
    # a or b == 0 break recursal
    if a == 0:
        return b
    elif b == 0:
        return a
    
    # break recursal when a == b, base case
    if a == b:
        return a
    
    # recursal when a>b or b>a
    elif a > b:
        return GCD_eculidean(a - b, b)
    return GCD_eculidean(a, b-a)
```
## Birthday Paradox
*** Taylors Series ***
e^x = 1 + x + (x^2)/2! + ...
e^x ~ 1 + x (when x << 1)

P(same) = 1 - P(different)

P(different) = 1 * (364/365) * (363/365) * (362/365) .. (1-((n-1)/365))

using Taylors series,

x ==   - a / 365

e^(-1/365) ~ 1 - (a/365)

P(different) can be rearranged as ,  P(different) =1*  (1- 1/365) * (1- 2/365) * (1- 3/365) .. (1- n-1/365)

P(different) ~ 1* e^(-1/365) * e^(-2/365) * e^(-3/365) .. * e^(-(n-1)/365)

                   ~ 1 * e^-(n*(n-1)/(2*365))

P(same) ~ 1 - e^-(n*(n-1)/(2*365))

e^-(n^2/(2*365)) ~ 1- P(same)

(n^2)/(2*365) ~ ln (1/ (1 - P(same))) 

approx formula for finding least number of people need to have  P(same) of handshakes
n ~ sqrt( (2*365) *ln(1/(1- P(same)))

```
#n ~ sqrt( (2*365) *ln(1/(1- P(same)))
from math import log as ln
from math import sqrt,ceil
def handshakes(prob:float):
    if prob == 1:
        return 367
    return ceil(sqrt((2*365)* ln(1/(1-prob))))

```

## Fibanocci Series
0,1,1,2,3,5,8,13,21,34
series follows as, even, odd, odd, even, odd, odd, even, ...

*** Even numbers ***
a,b=0,2
a,b=b,a+4*b

** all numbers **
a,b = 0,1
a,b = b,a+b

** recursive method (not good resource-wise) **
```
def fibanocci(n:int):
    if n<=1:
        return n
    else:
        return fibanocci(n-1) + fibanocci(n-2)

for i in range(10):
    print(fibanocci(i))

```

![image](https://github.com/Vipinkthomas/DSAL/assets/63467577/88d30964-f4b1-4cfd-811f-d4ed9e203f70)

calculating Fibonacci(5) : 
it computes the value of Fibonacci(2) three times, and the value of Fibonacci(1) five times. That just gets worse and worse the higher the number you want to compute.

## Prime Factorisation
### Inefficient method (Brute Force)
use 1..n 
### Pollard’s Rho Algorithm
improvised brute force algorithm 
use 1..sqrt(n)

### Sieve O(log n) for multiple queries
