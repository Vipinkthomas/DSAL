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

## Prime Factorisation
### Inefficient method (Brute Force)
use 1..n 
### Pollard’s Rho Algorithm
improvised brute force algorithm 
use 1..sqrt(n)

### Sieve O(log n) for multiple queries
