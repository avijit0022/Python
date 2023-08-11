## Find the solution below

```Python
def add_time(start, duration,day=""):
  weekd={0:"Sunday",1:"Monday",2:"Tuesday",3:"Wednesday",4:"Thursday",5:"Friday",6:"Saturday"}
  weekg={"sunday":0,"monday":1,"tuesday":2,"wednesday":3,"thursday":4,"friday":5,"saturday":6}
  if day!="":
    dayn=weekg[day.lower()]
  w=""
  dl=""
  time=start.split()
  t=time[0].split(":")
  th=int(t[0])
  if len(time)==2:
    if time[1]=="PM":
      th=th+12
  tm=int(t[1])
  d=duration.split(":")
  dh=int(d[0])
  dm=int(d[1])
  nh=th+dh
  nm=tm+dm
  if nm==60:
    nh=nh+1
    nm=0
  elif nm>60:
    nh=nh+1
    nm=nm-60
  if len(str(nm))==1:
    nm="0"+str(nm)
  else:
    nm=str(nm)
  if nh>24:
    newd=nh//24
    if day!="":
      dayn=weekg[day.lower()]
      dayn=dayn+newd
      dl=", "+weekd[dayn%7]
    if newd==1:
      w=" (next day)"
    else:
      w=" ("+str(newd)+" days later)"
    nh=nh%24
    if nh>11:
      nh=nh%12
      if nh==0:
        nh=12
      apm="PM"
    else:
      apm="AM"
  else:
    if day!="":
      dayn=weekg[day.lower()]
      dl=", "+weekd[dayn%7]
    if nh>11:
      nh=nh%12
      if nh==0:
        nh=12
      apm="PM"
    else:
      apm="AM"
  if nh==0:
        nh=12
  return str(nh)+":"+nm+" "+apm+dl+w
```
