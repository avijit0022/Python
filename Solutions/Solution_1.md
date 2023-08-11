## Find the solution below
<br>

```Python
def arithmetic_arranger(problems,b=False):
    if len(problems)>5:
      i="Error: Too many problems."
      return i
    else:
      c=0
      s1=""
      s2=""
      s3=""
      s4="\n"
      num1=[]
      num2=[]
      op=[]
      m=[]
      for j in problems:
        l=j.split()
        if l[1] != "+" and l[1] != "-":
          p="Error: Operator must be '+' or '-'."
          return p
          break
        num1.append(l[0])
        num2.append(l[2])
        op.append(l[1])
        m.append(max(len(l[0]),len(l[2])))
      test=num1+num2
      for k in test:
        if k.isdigit()==False:
          p="Error: Numbers must only contain digits."
          return p
          break
        if len(k)>4:
          p="Error: Numbers cannot be more than four digits."
          return p
          break
      for r in range(len(problems)):
        s1=s1+" "*2+" "*(m[r]-len(num1[r]))+num1[r]
        s2=s2+op[r]+" "+" "*(m[r]-len(num2[r]))+num2[r]
        s3=s3+"-"*(m[r]+2)
        if b==True:
          ans=eval(num1[r]+op[r]+num2[r])
          n=len(str(ans))
          if ans<0:
            s4=s4+" "*(abs(n-m[r]))+str(ans)
          elif n>m[r]:
            s4=s4+" "*(n-m[r])+str(ans)
          else:
            s4=s4+" "+" "*(abs(n-m[r]+1))+str(ans)
        if r<len(problems)-1:
          s1=s1+" "*4
          s2=s2+" "*4
          s3=s3+" "*4
          if b==True:
            s4=s4+" "*4
        if r==len(problems)-1:
          s1=s1+"\n"
          s2=s2+"\n" 
      s=s1+s2+s3
      if b==True:
        s=s+s4
      return s  
    
