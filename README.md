# DSAL
Data Structures and Algorithms - Python

## Data Structure Complexity

<table> 
    <thead>
        <tr>
        <th rowspan="2">Data Structure</th>
        <th colspan="4">Average Time Complexity</th>
        <th colspan="4">Worst Time Complexity</th>
        <th colspan="2">Space Complexity</th>
        <th rowspan="2">Desc</th>
        </tr>
        <tr>
        <th>nth element acess</th>
        <th>Search</th>
        <th>Insertion</th>
        <th>Deletion</th>
        <th>nth element acess</th>
        <th>Search</th>
        <th>Insertion</th>
        <th>Deletion</th>
        <th>Intrinsic</th>
        <th>Auxilary</th>
        </tr>
    </thead>
    <tbody>
    <tr>
        <td>Arrays</td>
        <td>O(1)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>Intrinsic space complexity-> storage for elements, auxilary -> space need to run operations like insert, delete and search (recursive/iterative)</td>
    </tr>
    <tr>
        <td>Stacks</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>O(1)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>O(1)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td></td>
    </tr>
    <tr>
        <td>Queues</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>O(1)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>O(1)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td></td>
    </tr>
    <tr>
        <td>Binary Tree</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)-iterative or O(n)-recursive</td>
        <td></td>
    </tr>
    <tr>
        <td>Binary Search Tree (BST)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(1)-iterative or O(n)-recursive</td>
        <td></td>
    </tr>
    <tr>
        <td>Balanced BST</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(logn)</td>
        <td>O(n)</td>
        <td>O(1)-iterative or O(logn)-recursive</td>
        <td></td>
    </tr>
    <tr>
        <td>Hash Table</td>
        <td>N/A</td>
        <td>O(1)</td>
        <td>O(1)</td>
        <td>O(1)</td>
        <td>N/A</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>bucket+elements O(m+n)-> O(n)</td>
        <td>O(1)-iterative</td>
        <td>to maintain efficiency load factor(a=n/m) sould be less than 0.7, in practice n/m is usually kept as 1. recursive data structure to store elements is uncommon</td>
    </tr>
    </tbody>
</table>

## Sorting Algo

<table> 
    <thead>
        <tr>
        <th rowspan="2">Sorting Algorithm</th>
        <th colspan="3">Time Complexity</th>
        <th colspan="2">Space Complexity</th>
        <th rowspan="2">Stable</th>
        <th rowspan="2">Sorting Class</th>
        <th rowspan="2">Remarks</th>
        </tr>
        <tr>
        <th>Best Case</th>
        <th>Average Case</th>
        <th>Worst Case</th>
        <th>Intrinsic</th>
        <th>Auxilary</th>
        </tr>
    </thead>
    <tbody>
    <tr>
        <td>Bubble Sort</td>
        <td>O(n)</td>
        <td>O(n^2)</td>
        <td>O(n^2)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>Yes</td>
        <td>Comparison</td>
        <td>Not preferred</td>
    </tr>
    <tr>
        <td>Insertion Sort</td>
        <td>O(n)</td>
        <td>O(n^2)</td>
        <td>O(n^2)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>Yes</td>
        <td>Comparison</td>
        <td>stable sort: it preserve relative order of equal elements. efficient for small or nearly ordered lists.  works as part of Timesort : Merge sort and insertion sort. In best case, every insert takes constant time</td>
    </tr>
    <tr>
        <td>Selection Sort</td>
        <td>O(n^2)</td>
        <td>O(n^2)</td>
        <td>O(n^2)</td>
        <td>O(n)</td>
        <td>O(1)</td>
        <td>No</td>
        <td>Comparison</td>
        <td> it even takes ~ n^2 times to processe sorted array.</td>
    </tr>
    <tr>
        <td>Merge Sort</td>
        <td>O(nlogn)</td>
        <td>O(nlogn)</td>
        <td>O(nlogn)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>Yes</td>
        <td>Comparison</td>
        <td>stable sort. part of timesort</td>
    </tr>
    <tr>
        <td>Quick Sort</td>
        <td>O(nlogn)</td>
        <td>O(nlogn)</td>
        <td>O(nlogn)</td>
        <td>O(n)</td>
        <td>O(n)</td>
        <td>Yes</td>
        <td>Comparison</td>
        <td>stable sort: it preserve relative order of equal elements. efficient for small or nearly ordered lists.  works as part of Timesort : Merge sort and insertion sort. In best case, every insert takes constant time</td>
    </tr>
    </tbody>
</table>

# bubble sort
```
# bubble sort
def BubbleSort(arr):
    times_ran=0
    for i in range(len(arr)-1,0,-1):
        swapped=False
        for j in range(0,i):
            if arr[j]>arr[j+1]:
                temp=arr[j]
                arr[j]=arr[j+1]
                arr[j+1]=temp
                swapped=True
            times_ran+=1
            print(j,arr)
        if not swapped:
            break
    return arr,times_ran

BubbleSort([1,2,3,4,5,6])

```
Insertion Sort
```
# Insertion sort
def InsertionSort(arr):
    times_ran=0
    for i in range(1,len(arr)):
        key = arr[i]
        j= i-1
        times_ran+=1
        while j>=0 and arr[j]>key:
            arr[j+1]=arr[j]
            j-=1
            times_ran+=1
        arr[j+1]=key

    return arr,times_ran

InsertionSort([1,2,3,4,5,6])

```
Selection Sort

```
# Selection Sort
def selectionSort(arr):
    times_ran=0
    for i in range(0,len(arr)):
        times_ran+=1
        min_index=i
        for j in range(i+1,len(arr)):
            times_ran+=1
            if arr[min_index]>arr[j]:
                min_index=j
        arr[i],arr[min_index]=arr[min_index],arr[i]
        print(arr)

    return arr,times_ran
selectionSort([6,5,4,3,2,1])
```
Merge Sort

```
# Merge Sort
def mergeSort(arr,times_ran=0):
    times_ran+=1
    if len(arr)<=1:
        return arr
    
    mid = len(arr)//2

    left = mergeSort(arr[:mid],times_ran)
    right = mergeSort(arr[mid:],times_ran)
    
    return merge(left,right,times_ran)

def merge(left,right,times_ran=0):
    sorted_list = []
    i=j=0

    while i<len(left) and j<len(right):
        times_ran+=1
        if left[i]<right[j]:
            sorted_list.append(left[i])
            i+=1
        else:
            sorted_list.append(right[j])
            j+=1
    sorted_list.extend(left[i:])
    sorted_list.extend(right[j:])
    print(times_ran,left,right,sorted_list)
    return sorted_list

mergeSort([6,5,4,3,2,1])       

```




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

**Taylors Series**

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

**Even numbers**

a,b=0,2
a,b=b,a+4*b

**all numbers**

a,b = 0,1
a,b = b,a+b

**recursive method (not good resource-wise)**

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
