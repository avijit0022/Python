# Python Code Templates

**Table of Contents :**
1. LCM of 2 Numbers

## 1. LCM of 2 Numbers
```Python
import math

def lcm(a, b):
    gcd = math.gcd(a, b)
    lcm = (a * b) // gcd
    return lcm
```
