# Python Code Templates

**Table of Contents :**
1. [LCM of 2 Numbers](#1-lcm-of-2-numbers)
2. [Formulas for Consecutive Numbers](#2-formulas-for-consecutive-numbers)
3. [Generate Prime Numbers](#3-generate-prime-numbers)

## 1. LCM of 2 Numbers
```Python
import math

def lcm(a, b):
    gcd = math.gcd(a, b)
    lcm = (a * b) // gcd
    return lcm
```
## 2. Formulas for Consecutive Numbers
```Python
sum_of_numbers = (n*(n+1))//2                      # 1 + 2 + 3 + 4 + ..... + n
sum_of_square_numbers = (n*(n+1)*((2*n)+1))//6     # 1^2 + 2^2 + 3^2 + 4^2 + ..... + n^2
```
## 3. Generate Prime Numbers
```Python
def prime(x, y):
    prime_list = []
    for i in range(x, y):
        if i == 0 or i == 1:
            continue
        else:
            for j in range(2, int(i/2)+1):
                if i % j == 0:
                    break
            else:
                prime_list.append(i)
    return prime_list
```
