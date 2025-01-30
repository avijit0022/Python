# Python Code Templates

**Table of Contents :**
1. LCM of 2 Numbers
2. Formulas for Consecutive Numbers

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
