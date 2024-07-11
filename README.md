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

## Prime Factorisation
### Inefficient method (Brute Force)
use 1..n 
### Pollard’s Rho Algorithm
improvised brute force algorithm 
use 1..sqrt(n)

### Sieve O(log n) for multiple queries
