## Find the solution below
```Python
t = int(input().strip())
for i in range(t):
    n = int(input().strip())
    a=(n-1)//3
    b=(n-1)//5
    ab=(n-1)//15
    na=((a*(a+1))//2)*3
    nb=((b*(b+1))//2)*5
    nab=((ab*(ab+1))//2)*15
    print(na+nb-nab)
```
